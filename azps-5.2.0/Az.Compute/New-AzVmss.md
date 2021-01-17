---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417999"
---
# <span data-ttu-id="57c82-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57c82-101">New-AzVmss</span></span>

## <span data-ttu-id="57c82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57c82-102">SYNOPSIS</span></span>
<span data-ttu-id="57c82-103">Создает VMSS.</span><span class="sxs-lookup"><span data-stu-id="57c82-103">Creates a VMSS.</span></span>

## <span data-ttu-id="57c82-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57c82-104">SYNTAX</span></span>

### <span data-ttu-id="57c82-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57c82-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57c82-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="57c82-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57c82-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57c82-107">DESCRIPTION</span></span>
<span data-ttu-id="57c82-108">С **его использованием** в Azure создается набор масштаба виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="57c82-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="57c82-109">Используйте простой набор параметров (), чтобы быстро создать предварительно заданную `SimpleParameterSet` VMSS и связанные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="57c82-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="57c82-110">Используйте набор параметров по умолчанию () для более сложных сценариев, когда нужно точно настроить каждый компонент VMSS и каждый связанный ресурс `DefaultParameter` перед созданием.</span><span class="sxs-lookup"><span data-stu-id="57c82-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="57c82-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57c82-111">EXAMPLES</span></span>

### <span data-ttu-id="57c82-112">Пример 1. Создание VMSS с помощью **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="57c82-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="57c82-113">Следующая команда создается с `$vmssName` именем:</span><span class="sxs-lookup"><span data-stu-id="57c82-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="57c82-114">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="57c82-114">A Resource Group</span></span>
* <span data-ttu-id="57c82-115">Виртуальная сеть</span><span class="sxs-lookup"><span data-stu-id="57c82-115">A virtual network</span></span>
* <span data-ttu-id="57c82-116">Баланс загрузки</span><span class="sxs-lookup"><span data-stu-id="57c82-116">A load balancer</span></span>
* <span data-ttu-id="57c82-117">Общедоступный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="57c82-117">A public IP</span></span>
* <span data-ttu-id="57c82-118">VMSS с 2 экземплярами</span><span class="sxs-lookup"><span data-stu-id="57c82-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="57c82-119">Изображение по умолчанию, выбранное для ВМ-м в VMSS, и `2016-Datacenter Windows Server` SKU `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="57c82-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="57c82-120">Пример 2. Создайте VMSS с помощью **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="57c82-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="57c82-121">В сложном примере выше создается система VMSS, а далее объясняется, что происходит:</span><span class="sxs-lookup"><span data-stu-id="57c82-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="57c82-122">Первая команда создает группу ресурсов с указанным именем и расположением.</span><span class="sxs-lookup"><span data-stu-id="57c82-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="57c82-123">Вторая команда использует командлет **New-AzStorageAccount** для создания учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="57c82-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="57c82-124">Затем третья команда использует командлет **Get-AzStorageAccount** для получения учетной записи хранения, созданной во второй команде, и сохраняет результат в переменной $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="57c82-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="57c82-125">Пятая команда использует командлет **New-AzVirtualNetworkSubnetConfig** для создания подсети, в результате чего результат сохраняется в переменной с именем $SubNet.</span><span class="sxs-lookup"><span data-stu-id="57c82-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="57c82-126">Шестая команда использует командлет **New-AzVirtualNetwork** для создания виртуальной сети и сохраняет результат в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="57c82-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="57c82-127">В седьмой команде используется командная команда **Get-AzVirtualNetwork,** которая используется для получения сведений о виртуальной сети, созданной при шестой команде, и ее хранилища в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="57c82-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="57c82-128">Для создания и получения информации с этого общераспозитного IP-адреса используется частью **New-AzPublicIpAddress** и **Get-AzureRmPublicIpAddress.**</span><span class="sxs-lookup"><span data-stu-id="57c82-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="57c82-129">Команды сохраняют данные в переменной с именем $PubIP.</span><span class="sxs-lookup"><span data-stu-id="57c82-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="57c82-130">Десятая команда использует командлет **New-AzureRmLoadBalancerFrontendIpConfig** для создания переднего балансира нагрузки и сохраняет результат в переменной с именем $Frontend.</span><span class="sxs-lookup"><span data-stu-id="57c82-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="57c82-131">Одиннадцатая команда использует **new-AzLoadBalancerBackendAddressPoolConfig** для создания конфигурации пула адресов дополнительных адресов и сохраняет результат в переменной с именем $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="57c82-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="57c82-132">Двенадцатая команда использует **New-AzLoadBalancerProbeConfig** для создания загона и сохраняет сведения о нем в переменной с именем $Probe.</span><span class="sxs-lookup"><span data-stu-id="57c82-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="57c82-133">Тринадцатая команда использует командлет **New-AzLoadBalancerInboundNatPoolConfig** для создания конфигурации пула перевода сетевых адресов (NAT) для балансиента нагрузки.</span><span class="sxs-lookup"><span data-stu-id="57c82-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="57c82-134">В 14-й команде используется **new-AzLoadBalancerRuleConfig,** чтобы создать конфигурацию правила балансиров нагрузки и получить результат в переменной с именем $LBRule.</span><span class="sxs-lookup"><span data-stu-id="57c82-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="57c82-135">Пятнадцатая команда использует командлет **New-AzLoadBalancer** для создания балансиров нагрузки и сохраняет результат в переменной с именем $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="57c82-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="57c82-136">Шестнадцатая команда использует **командлет Get-AzLoadBalancer** для получения сведений о балансире нагрузки, созданном с помощью пятнадцатой команды, и сохраняет их в переменной с именем $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="57c82-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="57c82-137">Для создания конфигурации IP-адреса VMSS используется командлет **New-AzVmssIPConfig,** который хранит сведения в переменной с именем $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="57c82-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="57c82-138">Восемнадцатая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="57c82-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="57c82-139">Для создания VMSS используется командлет **New-AzVmss.**</span><span class="sxs-lookup"><span data-stu-id="57c82-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="57c82-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57c82-140">PARAMETERS</span></span>

### <span data-ttu-id="57c82-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="57c82-141">-AllocationMethod</span></span>
<span data-ttu-id="57c82-142">Способ выделения для общего IP-адреса набора масштабирования (статический или динамический).</span><span class="sxs-lookup"><span data-stu-id="57c82-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="57c82-143">Если значение не задается, выделение будет статическим.</span><span class="sxs-lookup"><span data-stu-id="57c82-143">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57c82-144">-AsJob</span></span>
<span data-ttu-id="57c82-145">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="57c82-145">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="57c82-146">-BackendPoolName</span></span>
<span data-ttu-id="57c82-147">Имя пула адресов для загрузки, используемого в балансе нагрузки для этого набора.</span><span class="sxs-lookup"><span data-stu-id="57c82-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="57c82-148">Если значение не задано, создается новый пул с тем же именем, что и у набора масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="57c82-149">-BackendPort</span></span>
<span data-ttu-id="57c82-150">Номера портов, используемые средством балансиирования нагрузки "Масштаб", для связи с ВМ-данными в масштабе набора.</span><span class="sxs-lookup"><span data-stu-id="57c82-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="57c82-151">Если значения не указаны, порты 3389 и 5985 будут использоваться для VMS Windows, а порт 22 — для linux VMs.</span><span class="sxs-lookup"><span data-stu-id="57c82-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-152">-Credential</span><span class="sxs-lookup"><span data-stu-id="57c82-152">-Credential</span></span>
<span data-ttu-id="57c82-153">Учетные данные администратора (имя пользователя и пароль) для ВМ-документов в этом наборе масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="57c82-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="57c82-155">Определяет размер дисков данных в ГБ.</span><span class="sxs-lookup"><span data-stu-id="57c82-155">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c82-156">-DefaultProfile</span></span>
<span data-ttu-id="57c82-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57c82-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="57c82-158">-DomainNameLabel</span></span>
<span data-ttu-id="57c82-159">Метка доменного имени для public Fully-Qualified (FQDN) для этого набора масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="57c82-160">Это первый компонент доменного имени, автоматически назначенного набору масштабов.</span><span class="sxs-lookup"><span data-stu-id="57c82-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="57c82-161">Для автоматического присвоения доменных имен используется форма ( <DomainNameLabel> <Location> . . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="57c82-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="57c82-162">Если значение не задается, по умолчанию метка доменного имени является совмещением <ScaleSetName> <ResourceGroupName> и.</span><span class="sxs-lookup"><span data-stu-id="57c82-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-163">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="57c82-163">-EnableUltraSSD</span></span>
<span data-ttu-id="57c82-164">Используйте диски UltraSSD для ВМ-карт в наборе масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="57c82-165">-EncryptionAtHost</span></span>
<span data-ttu-id="57c82-166">Этот параметр включает шифрование для всех дисков, включая диск Resource/Temp на самом хосте.</span><span class="sxs-lookup"><span data-stu-id="57c82-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="57c82-167">По умолчанию: шифрование на хосте будет отключено, если для этого свойства не установлено значение true для ресурса.</span><span class="sxs-lookup"><span data-stu-id="57c82-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-168">-ВехионПолиция</span><span class="sxs-lookup"><span data-stu-id="57c82-168">-EvictionPolicy</span></span>
<span data-ttu-id="57c82-169">Политика присоединения к компьютеру с низким приоритетом для набора виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="57c82-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="57c82-170">Поддерживаются только значения "Deallocate" и "Delete".</span><span class="sxs-lookup"><span data-stu-id="57c82-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="57c82-171">-FrontendPoolName</span></span>
<span data-ttu-id="57c82-172">Имя пула адресов для использования в балансе "Масштаб".</span><span class="sxs-lookup"><span data-stu-id="57c82-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="57c82-173">Если значение не задается, будет создан новый пул адресов переднего уровня с тем же именем, что и у набора шкал.</span><span class="sxs-lookup"><span data-stu-id="57c82-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="57c82-174">-HostGroupId</span></span>
<span data-ttu-id="57c82-175">Указывает выделенную группу хостов, в которые будет находиться набор виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="57c82-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="57c82-176">-ImageName</span></span>
<span data-ttu-id="57c82-177">Имя изображения ВМ-карт в этом наборе масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="57c82-178">Если значение не затеряется, будет использоваться изображение Центра обработки данных Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="57c82-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="57c82-179">-InstanceCount</span></span>
<span data-ttu-id="57c82-180">Количество изображений ВМ в наборе масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="57c82-181">Если значение не за создано, создается 2 экземпляра.</span><span class="sxs-lookup"><span data-stu-id="57c82-181">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="57c82-182">-LoadBalancerName</span></span>
<span data-ttu-id="57c82-183">Имя балансира нагрузки, используемого для этого набора масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="57c82-184">Если значение не указано, создается новый баланс балансиры нагрузки с тем же именем, что и у набора масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-185">-Location</span><span class="sxs-lookup"><span data-stu-id="57c82-185">-Location</span></span>
<span data-ttu-id="57c82-186">Расположение Azure, в котором будет создан этот набор масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="57c82-187">Если значение не указано, расположение будет выявилось из расположения других ресурсов, на которые ссылается параметр.</span><span class="sxs-lookup"><span data-stu-id="57c82-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="57c82-188">-MaxPrice</span></span>
<span data-ttu-id="57c82-189">Максимальная цена выставить счет для набора виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="57c82-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="57c82-190">-NatBackendPort</span></span>
<span data-ttu-id="57c82-191">Backend port for inbound network address translation.</span><span class="sxs-lookup"><span data-stu-id="57c82-191">Backend port for inbound network address translation.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="57c82-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="57c82-193">Количество ошибок домена для каждой группы размещения.</span><span class="sxs-lookup"><span data-stu-id="57c82-193">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-194">-Priority</span><span class="sxs-lookup"><span data-stu-id="57c82-194">-Priority</span></span>
<span data-ttu-id="57c82-195">Приоритет виртуальной машины в наборе масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="57c82-196">Поддерживаются только такие значения, как "Обычный", "Spot" и "Низкий".</span><span class="sxs-lookup"><span data-stu-id="57c82-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="57c82-197">"Обычный" — для обычных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="57c82-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="57c82-198">Spot — для spot virtual machine.</span><span class="sxs-lookup"><span data-stu-id="57c82-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="57c82-199">"Низкая" также для spot virtual machine, но заменяется spot.</span><span class="sxs-lookup"><span data-stu-id="57c82-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="57c82-200">Используйте "Spot" вместо "Низкий".</span><span class="sxs-lookup"><span data-stu-id="57c82-200">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="57c82-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="57c82-202">The resource id of the Proximity Placement Group to use with this scale set.</span><span class="sxs-lookup"><span data-stu-id="57c82-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="57c82-203">-PublicIpAddressName</span></span>
<span data-ttu-id="57c82-204">Имя открытого IP-адреса, который будет использовать с этим набором масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="57c82-205">Если не предоставлено значение, создается новый общедоступный IPAddress с тем же именем, что и у набора масштабов.</span><span class="sxs-lookup"><span data-stu-id="57c82-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c82-206">-ResourceGroupName</span></span>
<span data-ttu-id="57c82-207">Имя группы ресурсов VMSS.</span><span class="sxs-lookup"><span data-stu-id="57c82-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="57c82-208">Если значение не задано, будет создана новая группа ресурсов с тем же именем, что и у набора масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="57c82-209">-ScaleInPolicy</span></span>
<span data-ttu-id="57c82-210">Правила, за которыми нужно следовать при масштабирования в наборе масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="57c82-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="57c82-211">Возможные значения: Default, 'OldestVM' и 'NewestVM'.</span><span class="sxs-lookup"><span data-stu-id="57c82-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="57c82-212">При масштабе набора виртуальных машин набор "По умолчанию" сначала будет балансироваться в разных зонах, если он является набором золонного масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="57c82-213">Затем он будет как можно остаток на балансе по всем доменам fault Domains.</span><span class="sxs-lookup"><span data-stu-id="57c82-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="57c82-214">В каждом домене ошибок будут выбраны новые виртуальные машины, которые не защищены от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="57c82-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="57c82-215">При масштабе масштабирования в виртуальной машине выбирается "OldestVM", для удаления будут выбраны старые виртуальные машины, которые не защищены от масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="57c82-216">Для наборов шкалы виртуальной машины в зоальбовом масштабе сначала нужно найти баланс между зонами.</span><span class="sxs-lookup"><span data-stu-id="57c82-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="57c82-217">В каждой зоне выбираются старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="57c82-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="57c82-218">При масштабе масштабирования набора виртуальных машин будут выбраны новые виртуальные машины, которые не защищены от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="57c82-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="57c82-219">Для наборов шкалы виртуальной машины в зоальбовом масштабе сначала нужно найти баланс между зонами.</span><span class="sxs-lookup"><span data-stu-id="57c82-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="57c82-220">В каждой зоне для удаления будут выбраны новые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="57c82-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="57c82-221">-SecurityGroupName</span></span>
<span data-ttu-id="57c82-222">Имя группы безопасности сети, которая будет применяться к данному набору масштабов.</span><span class="sxs-lookup"><span data-stu-id="57c82-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="57c82-223">Если значение не затеряется, будет создана и применена к набору масштабов стандартная группа безопасности с тем же именем, что и у набора.</span><span class="sxs-lookup"><span data-stu-id="57c82-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="57c82-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="57c82-225">Используется для создания набора "Масштаб" в одной группе (по умолчанию используется несколько групп).</span><span class="sxs-lookup"><span data-stu-id="57c82-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="57c82-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="57c82-227">Указывает на то, что расширения не запускаются для лишних перезапроизводиных VMs.</span><span class="sxs-lookup"><span data-stu-id="57c82-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57c82-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="57c82-229">Префикс адреса подсеть, который будет использовать этот Набор ScaleSet.</span><span class="sxs-lookup"><span data-stu-id="57c82-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="57c82-230">Параметры подсети по умолчанию (192.168.1.0/24) будут применены, если значение не предоставлено.</span><span class="sxs-lookup"><span data-stu-id="57c82-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="57c82-231">-SubnetName</span></span>
<span data-ttu-id="57c82-232">Имя подсети, используемой для этого набора масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="57c82-233">Если значение не за создано, будет создана новая подсеть с тем же именем, что и у набора масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="57c82-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="57c82-235">Если параметр присутствует, то VM-системам в наборе шкалы назначено удостоверение управляемой системы, которое генерируется автоматически.</span><span class="sxs-lookup"><span data-stu-id="57c82-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="57c82-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="57c82-237">Режим политики обновления для экземпляров VM в этом наборе масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="57c82-238">В политике обновления можно указать автоматическое, ручное обновление или развертывание.</span><span class="sxs-lookup"><span data-stu-id="57c82-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="57c82-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="57c82-240">Имя управляемого удостоверения службы, которое должно быть назначено VM-службам в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="57c82-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="57c82-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="57c82-242">Определяет объект **VirtualMachineScaleSet,** содержащий свойства VMSS, которые создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c82-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="57c82-243">-VirtualNetworkName</span></span>
<span data-ttu-id="57c82-244">Имя виртуальной сети, используемой для этого набора масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="57c82-245">Если значение не задается, создается новая виртуальная сеть с тем же именем, что и у набора.</span><span class="sxs-lookup"><span data-stu-id="57c82-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="57c82-246">-VMScaleSetName</span></span>
<span data-ttu-id="57c82-247">Указывает имя службы VMSS, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c82-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="57c82-248">-VmSize</span></span>
<span data-ttu-id="57c82-249">Размер экземпляров VM в этом наборе масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="57c82-250">Если не указан Standard_DS1_v2, будет использоваться стандартный размер (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="57c82-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57c82-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="57c82-252">Префикс адреса для виртуальной сети, используемой с этим набором масштаба.</span><span class="sxs-lookup"><span data-stu-id="57c82-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="57c82-253">Если значение не задается, будут использоваться стандартные параметры виртуального сетевого адреса (192.168.0.0/16).</span><span class="sxs-lookup"><span data-stu-id="57c82-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-254">-Zone</span><span class="sxs-lookup"><span data-stu-id="57c82-254">-Zone</span></span>
<span data-ttu-id="57c82-255">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="57c82-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-256">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57c82-256">-Confirm</span></span>
<span data-ttu-id="57c82-257">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="57c82-257">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c82-258">-WhatIf</span></span>
<span data-ttu-id="57c82-259">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c82-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c82-260">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57c82-260">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c82-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c82-261">CommonParameters</span></span>
<span data-ttu-id="57c82-262">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c82-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c82-263">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57c82-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c82-264">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57c82-264">INPUTS</span></span>

### <span data-ttu-id="57c82-265">System.String</span><span class="sxs-lookup"><span data-stu-id="57c82-265">System.String</span></span>

### <span data-ttu-id="57c82-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="57c82-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="57c82-267">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="57c82-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="57c82-268">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57c82-268">OUTPUTS</span></span>

### <span data-ttu-id="57c82-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="57c82-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="57c82-270">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57c82-270">NOTES</span></span>

## <span data-ttu-id="57c82-271">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57c82-271">RELATED LINKS</span></span>

[<span data-ttu-id="57c82-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57c82-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="57c82-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57c82-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="57c82-274">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57c82-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="57c82-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57c82-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="57c82-276">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57c82-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="57c82-277">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57c82-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="57c82-278">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="57c82-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


