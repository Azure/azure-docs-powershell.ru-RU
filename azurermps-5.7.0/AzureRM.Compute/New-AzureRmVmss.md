---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: e94cc565c2f22134f6bd4092247fbfa1f5a98b8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561900"
---
# <span data-ttu-id="156d1-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="156d1-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="156d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="156d1-102">SYNOPSIS</span></span>
<span data-ttu-id="156d1-103">Создает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="156d1-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="156d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="156d1-104">SYNTAX</span></span>

```
New-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="156d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="156d1-105">DESCRIPTION</span></span>
<span data-ttu-id="156d1-106">Командлет **New-AzureRmVmss** создает набор масштабов виртуальных машин (VMSS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="156d1-106">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="156d1-107">Этот командлет принимает объект **VirtualMachineScaleSet** в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="156d1-107">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="156d1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="156d1-108">EXAMPLES</span></span>

### <span data-ttu-id="156d1-109">Пример 1: создание VMSS</span><span class="sxs-lookup"><span data-stu-id="156d1-109">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="156d1-110">В следующем сложном примере создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="156d1-110">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="156d1-111">Первая команда создает группу ресурсов с указанным именем и расположением.</span><span class="sxs-lookup"><span data-stu-id="156d1-111">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="156d1-112">Вторая команда использует командлет **New-AzureRmStorageAccount** для создания учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="156d1-112">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="156d1-113">Третья команда затем использует командлет **Get-AzureRmStorageAccount** для получения учетной записи хранения, созданной во второй команде, и сохраняет результат в переменной $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="156d1-113">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="156d1-114">Пятая команда использует командлет **New-AzureRmVirtualNetworkSubnetConfig** для создания подсети и сохраняет результат в переменной с именем $SubNet.</span><span class="sxs-lookup"><span data-stu-id="156d1-114">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="156d1-115">Шестая команда использует командлет **New-AzureRmVirtualNetwork** для создания виртуальной сети и сохраняет результат в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="156d1-115">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="156d1-116">Седьмая команда использует **Get-AzureRmVirtualNetwork** для получения сведений о виртуальной сети, созданной в шестой команде, и сохраняет данные в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="156d1-116">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="156d1-117">В восьмом девятом — команда **New-AzureRmPublicIpAddress** и **Get-AzureRmPublicIpAddress** используется для создания и получения сведений об общедоступном IP-адресе.</span><span class="sxs-lookup"><span data-stu-id="156d1-117">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="156d1-118">Команды хранят данные в переменной с именем $PubIP.</span><span class="sxs-lookup"><span data-stu-id="156d1-118">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="156d1-119">Десятая команда использует командлет **New-AzureRmLoadBalancerFrontendIpConfig** для создания балансировщика интерфейсной балансировки нагрузки и сохраняет результат в переменной с именем $frontend.</span><span class="sxs-lookup"><span data-stu-id="156d1-119">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="156d1-120">Одиннадцатая команда использует **New-AzureRmLoadBalancerBackendAddressPoolConfig** для создания конфигурации пула адресов сервера и сохраняет результат в переменной с именем $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="156d1-120">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="156d1-121">Двенадцати команда использует **New-AzureRmLoadBalancerProbeConfig** для создания пробной проверки и сохраняет данные пробы в переменной с именем $Probe.</span><span class="sxs-lookup"><span data-stu-id="156d1-121">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="156d1-122">В команде thirteenth с помощью командлета **New-AzureRmLoadBalancerInboundNatPoolConfig** можно создать конфигурацию пула NAT для подсистемы балансировки нагрузки входящих сетевых адресов.</span><span class="sxs-lookup"><span data-stu-id="156d1-122">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="156d1-123">Команда fourteenth использует **New-AzureRmLoadBalancerRuleConfig** для создания конфигурации правила подсистемы балансировки нагрузки и сохраняет результат в переменной с именем $LBRule.</span><span class="sxs-lookup"><span data-stu-id="156d1-123">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="156d1-124">В команде пятнадцати используется командлет **New-AzureRmLoadBalancer** для создания подсистемы балансировки нагрузки и сохранения результата в переменной с именем $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="156d1-124">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="156d1-125">В шестнадцатой команде используется **Get-AzureRmLoadBalancer** для получения сведений о подсистеме балансировки нагрузки, созданной в команде пятнадцати, и сохраняет данные в переменной с именем $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="156d1-125">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="156d1-126">В команде Seventeenth используется командлет **New-AzureRmVmssIPConfig** для создания конфигурации IP VMSS и сохранения сведений в переменной с именем $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="156d1-126">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="156d1-127">Команда восемнадцатым месяцами эксплуатации использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="156d1-127">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="156d1-128">В команде XIX для создания VMSS используется командлет **New-AzureRmVmss** .</span><span class="sxs-lookup"><span data-stu-id="156d1-128">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="156d1-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="156d1-129">PARAMETERS</span></span>

### <span data-ttu-id="156d1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="156d1-130">-ResourceGroupName</span></span>
<span data-ttu-id="156d1-131">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="156d1-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156d1-132">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="156d1-132">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="156d1-133">Указывает объект **VirtualMachineScaleSet** , СОДЕРЖАЩИЙ свойства VMSS, создаваемые этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="156d1-133">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="156d1-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="156d1-134">-VMScaleSetName</span></span>
<span data-ttu-id="156d1-135">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="156d1-135">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156d1-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="156d1-136">-Confirm</span></span>
<span data-ttu-id="156d1-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="156d1-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="156d1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="156d1-138">-WhatIf</span></span>
<span data-ttu-id="156d1-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="156d1-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="156d1-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="156d1-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="156d1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156d1-141">CommonParameters</span></span>
<span data-ttu-id="156d1-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="156d1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156d1-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="156d1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156d1-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="156d1-144">INPUTS</span></span>

### <span data-ttu-id="156d1-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="156d1-145">None</span></span>
<span data-ttu-id="156d1-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="156d1-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="156d1-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="156d1-147">OUTPUTS</span></span>

### <span data-ttu-id="156d1-148">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="156d1-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="156d1-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="156d1-149">NOTES</span></span>

## <span data-ttu-id="156d1-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="156d1-150">RELATED LINKS</span></span>

[<span data-ttu-id="156d1-151">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="156d1-151">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="156d1-152">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="156d1-152">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="156d1-153">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="156d1-153">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="156d1-154">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="156d1-154">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="156d1-155">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="156d1-155">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="156d1-156">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="156d1-156">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="156d1-157">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="156d1-157">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


