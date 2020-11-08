---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 914d942620eea7517b2bac635399fd7d1b3c1307
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073675"
---
# <span data-ttu-id="aca70-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aca70-101">New-AzVmss</span></span>

## <span data-ttu-id="aca70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aca70-102">SYNOPSIS</span></span>
<span data-ttu-id="aca70-103">Создает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="aca70-103">Creates a VMSS.</span></span>

## <span data-ttu-id="aca70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aca70-104">SYNTAX</span></span>

### <span data-ttu-id="aca70-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aca70-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aca70-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="aca70-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-Priority <String>]
 [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aca70-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aca70-107">DESCRIPTION</span></span>
<span data-ttu-id="aca70-108">Командлет **New-AzVmss** создает набор масштабов виртуальных машин (VMSS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="aca70-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="aca70-109">Используйте простой набор параметров ( `SimpleParameterSet` ), чтобы быстро создать предварительно заданные VMSS и связанные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aca70-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="aca70-110">Используйте набор параметров по умолчанию ( `DefaultParameter` ) для более сложных сценариев, если вам нужно точно настроить каждый компонент VMSS и каждый связанный ресурс перед его созданием.</span><span class="sxs-lookup"><span data-stu-id="aca70-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="aca70-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aca70-111">EXAMPLES</span></span>

### <span data-ttu-id="aca70-112">Пример 1: создание VMSS с помощью **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="aca70-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="aca70-113">В приведенной выше команде создаются следующие элементы с именем `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="aca70-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="aca70-114">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="aca70-114">A Resource Group</span></span>
* <span data-ttu-id="aca70-115">Виртуальная сеть</span><span class="sxs-lookup"><span data-stu-id="aca70-115">A virtual network</span></span>
* <span data-ttu-id="aca70-116">Подсистема балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="aca70-116">A load balancer</span></span>
* <span data-ttu-id="aca70-117">Общедоступный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="aca70-117">A public IP</span></span>
* <span data-ttu-id="aca70-118">VMSS с 2 экземплярами</span><span class="sxs-lookup"><span data-stu-id="aca70-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="aca70-119">Изображение по умолчанию, выбранное для виртуальных машин в VMSS, `2016-Datacenter Windows Server` и SKU `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="aca70-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="aca70-120">Пример 2: создание VMSS с помощью **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="aca70-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
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

<span data-ttu-id="aca70-121">В сложном примере выше создается VMSS, а далее показано, что происходит:</span><span class="sxs-lookup"><span data-stu-id="aca70-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="aca70-122">Первая команда создает группу ресурсов с указанным именем и расположением.</span><span class="sxs-lookup"><span data-stu-id="aca70-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="aca70-123">Вторая команда использует командлет **New-AzStorageAccount** для создания учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="aca70-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="aca70-124">Третья команда затем использует командлет **Get-AzStorageAccount** для получения учетной записи хранения, созданной во второй команде, и сохраняет результат в переменной $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="aca70-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="aca70-125">Пятая команда использует командлет **New-AzVirtualNetworkSubnetConfig** для создания подсети и сохраняет результат в переменной с именем $SubNet.</span><span class="sxs-lookup"><span data-stu-id="aca70-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="aca70-126">Шестая команда использует командлет **New-AzVirtualNetwork** для создания виртуальной сети и сохраняет результат в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="aca70-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="aca70-127">Седьмая команда использует **Get-AzVirtualNetwork** для получения сведений о виртуальной сети, созданной в шестой команде, и сохраняет данные в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="aca70-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="aca70-128">В восьмом девятом — команда **New-AzPublicIpAddress** и **Get-AzureRmPublicIpAddress** используется для создания и получения сведений об общедоступном IP-адресе.</span><span class="sxs-lookup"><span data-stu-id="aca70-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="aca70-129">Команды хранят данные в переменной с именем $PubIP.</span><span class="sxs-lookup"><span data-stu-id="aca70-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="aca70-130">Десятая команда использует командлет **New-AzureRmLoadBalancerFrontendIpConfig** для создания балансировщика интерфейсной балансировки нагрузки и сохраняет результат в переменной с именем $frontend.</span><span class="sxs-lookup"><span data-stu-id="aca70-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="aca70-131">Одиннадцатая команда использует **New-AzLoadBalancerBackendAddressPoolConfig** для создания конфигурации пула адресов сервера и сохраняет результат в переменной с именем $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="aca70-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="aca70-132">Двенадцати команда использует **New-AzLoadBalancerProbeConfig** для создания пробной проверки и сохраняет данные пробы в переменной с именем $Probe.</span><span class="sxs-lookup"><span data-stu-id="aca70-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="aca70-133">В команде thirteenth с помощью командлета **New-AzLoadBalancerInboundNatPoolConfig** можно создать конфигурацию пула NAT для подсистемы балансировки нагрузки входящих сетевых адресов.</span><span class="sxs-lookup"><span data-stu-id="aca70-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="aca70-134">Команда fourteenth использует **New-AzLoadBalancerRuleConfig** для создания конфигурации правила подсистемы балансировки нагрузки и сохраняет результат в переменной с именем $LBRule.</span><span class="sxs-lookup"><span data-stu-id="aca70-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="aca70-135">В команде пятнадцати используется командлет **New-AzLoadBalancer** для создания подсистемы балансировки нагрузки и сохранения результата в переменной с именем $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="aca70-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="aca70-136">В шестнадцатой команде используется **Get-AzLoadBalancer** для получения сведений о подсистеме балансировки нагрузки, созданной в команде пятнадцати, и сохраняет данные в переменной с именем $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="aca70-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="aca70-137">В команде Seventeenth используется командлет **New-AzVmssIPConfig** для создания конфигурации IP VMSS и сохранения сведений в переменной с именем $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="aca70-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="aca70-138">Команда восемнадцатым месяцами эксплуатации использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="aca70-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="aca70-139">В команде XIX для создания VMSS используется командлет **New-AzVmss** .</span><span class="sxs-lookup"><span data-stu-id="aca70-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="aca70-140">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aca70-140">PARAMETERS</span></span>

### <span data-ttu-id="aca70-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="aca70-141">-AllocationMethod</span></span>
<span data-ttu-id="aca70-142">Метод выделения для общедоступного IP-адреса набора шкал (static или Dynamic).</span><span class="sxs-lookup"><span data-stu-id="aca70-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="aca70-143">Если значение не указано, выделение будет статическим.</span><span class="sxs-lookup"><span data-stu-id="aca70-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="aca70-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aca70-144">-AsJob</span></span>
<span data-ttu-id="aca70-145">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="aca70-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aca70-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="aca70-146">-BackendPoolName</span></span>
<span data-ttu-id="aca70-147">Имя пула адресных адресов серверной платформы, который будет использоваться в подсистеме балансировки нагрузки для этого набора масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="aca70-148">Если значение не задано, будет создана новая группа серверной базы данных с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="aca70-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="aca70-149">-BackendPort</span></span>
<span data-ttu-id="aca70-150">Номера внутренних портов, используемые подсистемой балансировки нагрузки для связи с виртуальными машинами в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="aca70-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="aca70-151">Если значения не указаны, для виртуальных компьютеров Windows будут использоваться порты 3389 и 5985, а для виртуальных машин Linux будет использоваться порт 22.</span><span class="sxs-lookup"><span data-stu-id="aca70-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="aca70-152">-Credential</span><span class="sxs-lookup"><span data-stu-id="aca70-152">-Credential</span></span>
<span data-ttu-id="aca70-153">Учетные данные администратора (имя пользователя и пароль) для виртуальных машин в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="aca70-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="aca70-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="aca70-155">Задает размеры дисков данных в ГБ.</span><span class="sxs-lookup"><span data-stu-id="aca70-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="aca70-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca70-156">-DefaultProfile</span></span>
<span data-ttu-id="aca70-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aca70-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aca70-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="aca70-158">-DomainNameLabel</span></span>
<span data-ttu-id="aca70-159">Метка доменного имени для общедоступного доменного имени Fully-Qualified (FQDN) для данного множества масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="aca70-160">Это первый компонент доменного имени, которое автоматически назначается набору масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="aca70-161">Автоматически назначаемые доменные имена используют форму ( <DomainNameLabel> ..). <Location> cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="aca70-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="aca70-162">Если значение не задано, по умолчанию будет использоваться метка доменного имени для объединения <ScaleSetName> и <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="aca70-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="aca70-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="aca70-163">-EnableUltraSSD</span></span>
<span data-ttu-id="aca70-164">Используйте диски UltraSSD для виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="aca70-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="aca70-165">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="aca70-165">-EvictionPolicy</span></span>
<span data-ttu-id="aca70-166">Политика вытеснения для установленного количества виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="aca70-166">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="aca70-167">Поддерживаются только значения "освободить" и "Удалить".</span><span class="sxs-lookup"><span data-stu-id="aca70-167">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="aca70-168">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="aca70-168">-FrontendPoolName</span></span>
<span data-ttu-id="aca70-169">Имя пула адресных интерфейсов, который будет использоваться в подсистеме балансировки нагрузки для набора масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-169">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="aca70-170">Если значение не задано, будет создан новый пул адресных веб-интерфейсов с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-170">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="aca70-171">-ImageName</span><span class="sxs-lookup"><span data-stu-id="aca70-171">-ImageName</span></span>
<span data-ttu-id="aca70-172">Имя образа для виртуальных машин в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-172">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="aca70-173">Если значение не указано, будет использоваться изображение "центр обработки данных Windows Server 2016".</span><span class="sxs-lookup"><span data-stu-id="aca70-173">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="aca70-174">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="aca70-174">-InstanceCount</span></span>
<span data-ttu-id="aca70-175">Количество образов виртуальных машин в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-175">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="aca70-176">Если значение не задано, будет создано 2 экземпляра.</span><span class="sxs-lookup"><span data-stu-id="aca70-176">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="aca70-177">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="aca70-177">-LoadBalancerName</span></span>
<span data-ttu-id="aca70-178">Имя подсистемы балансировки нагрузки, используемой с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-178">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="aca70-179">Если значение не задано, будет создаваться новая служба подсистемы балансировки нагрузки с тем же именем, что и набор масштабирования.</span><span class="sxs-lookup"><span data-stu-id="aca70-179">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="aca70-180">-Location</span><span class="sxs-lookup"><span data-stu-id="aca70-180">-Location</span></span>
<span data-ttu-id="aca70-181">Место Azure, в котором будет создан этот параметр масштабирования.</span><span class="sxs-lookup"><span data-stu-id="aca70-181">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="aca70-182">Если значение не задано, расположение будет выводиться из расположения других ресурсов, указанных в параметрах.</span><span class="sxs-lookup"><span data-stu-id="aca70-182">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="aca70-183">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="aca70-183">-MaxPrice</span></span>
<span data-ttu-id="aca70-184">Максимальная стоимость выставления счетов в наборе масштабов виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="aca70-184">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="aca70-185">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="aca70-185">-NatBackendPort</span></span>
<span data-ttu-id="aca70-186">Внутренний порт для преобразования входящего сетевого адреса.</span><span class="sxs-lookup"><span data-stu-id="aca70-186">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="aca70-187">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="aca70-187">-Priority</span></span>
<span data-ttu-id="aca70-188">Приоритет виртуальной машины в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="aca70-188">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="aca70-189">Поддерживаются только значения "Regular", "плашка" и "низкий".</span><span class="sxs-lookup"><span data-stu-id="aca70-189">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="aca70-190">"Regular" предназначен для обычной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aca70-190">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="aca70-191">"Плашка" — для точечной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="aca70-191">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="aca70-192">"Low" также используется для точечной виртуальной машины, но заменяется на "плашка".</span><span class="sxs-lookup"><span data-stu-id="aca70-192">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="aca70-193">Вместо "низкая" используйте "смесевых".</span><span class="sxs-lookup"><span data-stu-id="aca70-193">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="aca70-194">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="aca70-194">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="aca70-195">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-195">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="aca70-196">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="aca70-196">-PublicIpAddressName</span></span>
<span data-ttu-id="aca70-197">Имя общедоступного IP-адреса для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-197">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="aca70-198">Новый общедоступный IP-адрес с тем же именем, что и у множества масштабирования, будет создан, если значение не указано.</span><span class="sxs-lookup"><span data-stu-id="aca70-198">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="aca70-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca70-199">-ResourceGroupName</span></span>
<span data-ttu-id="aca70-200">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="aca70-200">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="aca70-201">Если значение не задано, будет создана новая группа ресурсов с тем же именем, что и у множества.</span><span class="sxs-lookup"><span data-stu-id="aca70-201">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="aca70-202">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="aca70-202">-ScaleInPolicy</span></span>
<span data-ttu-id="aca70-203">Правила, которые следует выполнить при масштабировании, в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="aca70-203">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="aca70-204">Возможные значения: "по умолчанию", "OldestVM" и "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="aca70-204">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="aca70-205">"По умолчанию" при масштабировании множества виртуальных машин, набор масштабов сначала распределяется между зонами, если он является набором масштабов Zonal.</span><span class="sxs-lookup"><span data-stu-id="aca70-205">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="aca70-206">Затем он будет надежно распределен между доменами сбоя.</span><span class="sxs-lookup"><span data-stu-id="aca70-206">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="aca70-207">В каждом домене сбоя виртуальные компьютеры, выбранные для удаления, будут новыми, не защищенными от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="aca70-207">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="aca70-208">"OldestVM". при масштабировании множества масштабов виртуальной машины, для удаления будут выбраны самые старые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="aca70-208">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="aca70-209">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="aca70-209">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="aca70-210">В каждой зоне для удаления будут выбраны самые старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="aca70-210">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="aca70-211">"NewestVM" при масштабировании множества виртуальных машин с масштабированием для удаления будут выбраны самые новые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="aca70-211">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="aca70-212">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="aca70-212">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="aca70-213">В каждой зоне для удаления будут выбраны новые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="aca70-213">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="aca70-214">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="aca70-214">-SecurityGroupName</span></span>
<span data-ttu-id="aca70-215">Имя группы безопасности сети, применяемой к этому набору масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-215">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="aca70-216">Если значение не задано, будет создана группа безопасности сети по умолчанию с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-216">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="aca70-217">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="aca70-217">-SinglePlacementGroup</span></span>
<span data-ttu-id="aca70-218">Используйте этот параметр, чтобы создать набор масштабов в одной группе размещения, по умолчанию — по нескольким группам.</span><span class="sxs-lookup"><span data-stu-id="aca70-218">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="aca70-219">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="aca70-219">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="aca70-220">Указывает, что расширения не выполняются на дополнительных переподготовленных виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="aca70-220">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="aca70-221">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="aca70-221">-SubnetAddressPrefix</span></span>
<span data-ttu-id="aca70-222">Префикс адреса подсети, используемой этим набором элементов масштабирования.</span><span class="sxs-lookup"><span data-stu-id="aca70-222">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="aca70-223">Параметры подсети по умолчанию (192.168.1.0/24) будут применены, если не задано значение.</span><span class="sxs-lookup"><span data-stu-id="aca70-223">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="aca70-224">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="aca70-224">-SubnetName</span></span>
<span data-ttu-id="aca70-225">Имя подсети, используемой в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-225">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="aca70-226">Новая подсеть будет создана с тем же именем, что и в наборе масштабирования, если значение не указано.</span><span class="sxs-lookup"><span data-stu-id="aca70-226">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="aca70-227">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="aca70-227">-SystemAssignedIdentity</span></span>
<span data-ttu-id="aca70-228">Если параметр присутствует, ВМ (-ы) в наборе Scale (—) назначается (-а) управляемому системному удостоверению, которое создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="aca70-228">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="aca70-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="aca70-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="aca70-230">Режим политики обновления для экземпляров виртуальных машин в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-230">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="aca70-231">Политика обновления может определять автоматические, ручные и чередующиеся обновления.</span><span class="sxs-lookup"><span data-stu-id="aca70-231">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="aca70-232">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="aca70-232">-UserAssignedIdentity</span></span>
<span data-ttu-id="aca70-233">Имя удостоверения управляемой службы, которое должно быть назначено для ВМ (ов) в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-233">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="aca70-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aca70-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="aca70-235">Указывает объект **VirtualMachineScaleSet** , СОДЕРЖАЩИЙ свойства VMSS, создаваемые этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="aca70-235">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="aca70-236">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="aca70-236">-VirtualNetworkName</span></span>
<span data-ttu-id="aca70-237">Имя виртуальной сети, используемой в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-237">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="aca70-238">Если значение не задано, будет создана новая виртуальная сеть с тем же именем, что и у множества.</span><span class="sxs-lookup"><span data-stu-id="aca70-238">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="aca70-239">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="aca70-239">-VMScaleSetName</span></span>
<span data-ttu-id="aca70-240">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="aca70-240">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="aca70-241">-VmSize</span><span class="sxs-lookup"><span data-stu-id="aca70-241">-VmSize</span></span>
<span data-ttu-id="aca70-242">Размер экземпляров виртуальных машин в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-242">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="aca70-243">Если размер не указан, будет использоваться размер по умолчанию (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="aca70-243">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="aca70-244">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="aca70-244">-VnetAddressPrefix</span></span>
<span data-ttu-id="aca70-245">Префикс адреса для виртуальной сети, используемой в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="aca70-245">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="aca70-246">Значения префиксов виртуальных сетевых адресов по умолчанию (192.168.0.0/16) будут использоваться, если не задано значение.</span><span class="sxs-lookup"><span data-stu-id="aca70-246">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="aca70-247">-Zone</span><span class="sxs-lookup"><span data-stu-id="aca70-247">-Zone</span></span>
<span data-ttu-id="aca70-248">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="aca70-248">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="aca70-249">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aca70-249">-Confirm</span></span>
<span data-ttu-id="aca70-250">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aca70-250">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aca70-251">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aca70-251">-WhatIf</span></span>
<span data-ttu-id="aca70-252">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aca70-252">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aca70-253">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aca70-253">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aca70-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca70-254">CommonParameters</span></span>
<span data-ttu-id="aca70-255">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aca70-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca70-256">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aca70-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca70-257">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aca70-257">INPUTS</span></span>

### <span data-ttu-id="aca70-258">System. String</span><span class="sxs-lookup"><span data-stu-id="aca70-258">System.String</span></span>

### <span data-ttu-id="aca70-259">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aca70-259">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="aca70-260">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aca70-260">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aca70-261">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aca70-261">OUTPUTS</span></span>

### <span data-ttu-id="aca70-262">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="aca70-262">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="aca70-263">Пуск</span><span class="sxs-lookup"><span data-stu-id="aca70-263">NOTES</span></span>

## <span data-ttu-id="aca70-264">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aca70-264">RELATED LINKS</span></span>

[<span data-ttu-id="aca70-265">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aca70-265">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="aca70-266">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aca70-266">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="aca70-267">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aca70-267">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="aca70-268">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aca70-268">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="aca70-269">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aca70-269">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="aca70-270">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aca70-270">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="aca70-271">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aca70-271">Update-AzVmss</span></span>](./Update-AzVmss.md)


