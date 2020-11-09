---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 4953e914cc52784cd815be80307babfe05f3b63c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316192"
---
# <span data-ttu-id="fee9f-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fee9f-101">New-AzVmss</span></span>

## <span data-ttu-id="fee9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fee9f-102">SYNOPSIS</span></span>
<span data-ttu-id="fee9f-103">Создает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="fee9f-103">Creates a VMSS.</span></span>

## <span data-ttu-id="fee9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fee9f-104">SYNTAX</span></span>

### <span data-ttu-id="fee9f-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fee9f-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee9f-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee9f-106">SimpleParameterSet</span></span>
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

## <span data-ttu-id="fee9f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fee9f-107">DESCRIPTION</span></span>
<span data-ttu-id="fee9f-108">Командлет **New-AzVmss** создает набор масштабов виртуальных машин (VMSS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="fee9f-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="fee9f-109">Используйте простой набор параметров ( `SimpleParameterSet` ), чтобы быстро создать предварительно заданные VMSS и связанные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="fee9f-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="fee9f-110">Используйте набор параметров по умолчанию ( `DefaultParameter` ) для более сложных сценариев, если вам нужно точно настроить каждый компонент VMSS и каждый связанный ресурс перед его созданием.</span><span class="sxs-lookup"><span data-stu-id="fee9f-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="fee9f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fee9f-111">EXAMPLES</span></span>

### <span data-ttu-id="fee9f-112">Пример 1: создание VMSS с помощью **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="fee9f-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="fee9f-113">В приведенной выше команде создаются следующие элементы с именем `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="fee9f-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="fee9f-114">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="fee9f-114">A Resource Group</span></span>
* <span data-ttu-id="fee9f-115">Виртуальная сеть</span><span class="sxs-lookup"><span data-stu-id="fee9f-115">A virtual network</span></span>
* <span data-ttu-id="fee9f-116">Подсистема балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="fee9f-116">A load balancer</span></span>
* <span data-ttu-id="fee9f-117">Общедоступный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="fee9f-117">A public IP</span></span>
* <span data-ttu-id="fee9f-118">VMSS с 2 экземплярами</span><span class="sxs-lookup"><span data-stu-id="fee9f-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="fee9f-119">Изображение по умолчанию, выбранное для виртуальных машин в VMSS, `2016-Datacenter Windows Server` и SKU `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="fee9f-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="fee9f-120">Пример 2: создание VMSS с помощью **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="fee9f-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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

<span data-ttu-id="fee9f-121">В сложном примере выше создается VMSS, а далее показано, что происходит:</span><span class="sxs-lookup"><span data-stu-id="fee9f-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="fee9f-122">Первая команда создает группу ресурсов с указанным именем и расположением.</span><span class="sxs-lookup"><span data-stu-id="fee9f-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="fee9f-123">Вторая команда использует командлет **New-AzStorageAccount** для создания учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fee9f-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="fee9f-124">Третья команда затем использует командлет **Get-AzStorageAccount** для получения учетной записи хранения, созданной во второй команде, и сохраняет результат в переменной $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="fee9f-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="fee9f-125">Пятая команда использует командлет **New-AzVirtualNetworkSubnetConfig** для создания подсети и сохраняет результат в переменной с именем $SubNet.</span><span class="sxs-lookup"><span data-stu-id="fee9f-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="fee9f-126">Шестая команда использует командлет **New-AzVirtualNetwork** для создания виртуальной сети и сохраняет результат в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="fee9f-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="fee9f-127">Седьмая команда использует **Get-AzVirtualNetwork** для получения сведений о виртуальной сети, созданной в шестой команде, и сохраняет данные в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="fee9f-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="fee9f-128">В восьмом девятом — команда **New-AzPublicIpAddress** и **Get-AzureRmPublicIpAddress** используется для создания и получения сведений об общедоступном IP-адресе.</span><span class="sxs-lookup"><span data-stu-id="fee9f-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="fee9f-129">Команды хранят данные в переменной с именем $PubIP.</span><span class="sxs-lookup"><span data-stu-id="fee9f-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="fee9f-130">Десятая команда использует командлет **New-AzureRmLoadBalancerFrontendIpConfig** для создания балансировщика интерфейсной балансировки нагрузки и сохраняет результат в переменной с именем $frontend.</span><span class="sxs-lookup"><span data-stu-id="fee9f-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="fee9f-131">Одиннадцатая команда использует **New-AzLoadBalancerBackendAddressPoolConfig** для создания конфигурации пула адресов сервера и сохраняет результат в переменной с именем $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="fee9f-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="fee9f-132">Двенадцати команда использует **New-AzLoadBalancerProbeConfig** для создания пробной проверки и сохраняет данные пробы в переменной с именем $Probe.</span><span class="sxs-lookup"><span data-stu-id="fee9f-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="fee9f-133">В команде thirteenth с помощью командлета **New-AzLoadBalancerInboundNatPoolConfig** можно создать конфигурацию пула NAT для подсистемы балансировки нагрузки входящих сетевых адресов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="fee9f-134">Команда fourteenth использует **New-AzLoadBalancerRuleConfig** для создания конфигурации правила подсистемы балансировки нагрузки и сохраняет результат в переменной с именем $LBRule.</span><span class="sxs-lookup"><span data-stu-id="fee9f-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="fee9f-135">В команде пятнадцати используется командлет **New-AzLoadBalancer** для создания подсистемы балансировки нагрузки и сохранения результата в переменной с именем $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="fee9f-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="fee9f-136">В шестнадцатой команде используется **Get-AzLoadBalancer** для получения сведений о подсистеме балансировки нагрузки, созданной в команде пятнадцати, и сохраняет данные в переменной с именем $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="fee9f-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="fee9f-137">В команде Seventeenth используется командлет **New-AzVmssIPConfig** для создания конфигурации IP VMSS и сохранения сведений в переменной с именем $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="fee9f-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="fee9f-138">Команда восемнадцатым месяцами эксплуатации использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="fee9f-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="fee9f-139">В команде XIX для создания VMSS используется командлет **New-AzVmss** .</span><span class="sxs-lookup"><span data-stu-id="fee9f-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="fee9f-140">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fee9f-140">PARAMETERS</span></span>

### <span data-ttu-id="fee9f-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="fee9f-141">-AllocationMethod</span></span>
<span data-ttu-id="fee9f-142">Метод выделения для общедоступного IP-адреса набора шкал (static или Dynamic).</span><span class="sxs-lookup"><span data-stu-id="fee9f-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="fee9f-143">Если значение не указано, выделение будет статическим.</span><span class="sxs-lookup"><span data-stu-id="fee9f-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="fee9f-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fee9f-144">-AsJob</span></span>
<span data-ttu-id="fee9f-145">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="fee9f-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fee9f-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="fee9f-146">-BackendPoolName</span></span>
<span data-ttu-id="fee9f-147">Имя пула адресных адресов серверной платформы, который будет использоваться в подсистеме балансировки нагрузки для этого набора масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="fee9f-148">Если значение не задано, будет создана новая группа серверной базы данных с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="fee9f-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fee9f-149">-BackendPort</span></span>
<span data-ttu-id="fee9f-150">Номера внутренних портов, используемые подсистемой балансировки нагрузки для связи с виртуальными машинами в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="fee9f-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="fee9f-151">Если значения не указаны, для виртуальных компьютеров Windows будут использоваться порты 3389 и 5985, а для виртуальных машин Linux будет использоваться порт 22.</span><span class="sxs-lookup"><span data-stu-id="fee9f-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="fee9f-152">-Credential</span><span class="sxs-lookup"><span data-stu-id="fee9f-152">-Credential</span></span>
<span data-ttu-id="fee9f-153">Учетные данные администратора (имя пользователя и пароль) для виртуальных машин в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="fee9f-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="fee9f-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="fee9f-155">Задает размеры дисков данных в ГБ.</span><span class="sxs-lookup"><span data-stu-id="fee9f-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="fee9f-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee9f-156">-DefaultProfile</span></span>
<span data-ttu-id="fee9f-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fee9f-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fee9f-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="fee9f-158">-DomainNameLabel</span></span>
<span data-ttu-id="fee9f-159">Метка доменного имени для общедоступного доменного имени Fully-Qualified (FQDN) для данного множества масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="fee9f-160">Это первый компонент доменного имени, которое автоматически назначается набору масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="fee9f-161">Автоматически назначаемые доменные имена используют форму ( <DomainNameLabel> ..). <Location> cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="fee9f-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="fee9f-162">Если значение не задано, по умолчанию будет использоваться метка доменного имени для объединения <ScaleSetName> и <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="fee9f-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="fee9f-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="fee9f-163">-EnableUltraSSD</span></span>
<span data-ttu-id="fee9f-164">Используйте диски UltraSSD для виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="fee9f-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="fee9f-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="fee9f-165">-EncryptionAtHost</span></span>
<span data-ttu-id="fee9f-166">Этот параметр включит шифрование для всех дисков, включая ресурс/временный диск на узле.</span><span class="sxs-lookup"><span data-stu-id="fee9f-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="fee9f-167">По умолчанию: шифрование на узле будет отключено, если это свойство не имеет значение true для ресурса.</span><span class="sxs-lookup"><span data-stu-id="fee9f-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="fee9f-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="fee9f-168">-EvictionPolicy</span></span>
<span data-ttu-id="fee9f-169">Политика вытеснения для установленного количества виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="fee9f-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="fee9f-170">Поддерживаются только значения "освободить" и "Удалить".</span><span class="sxs-lookup"><span data-stu-id="fee9f-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="fee9f-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="fee9f-171">-FrontendPoolName</span></span>
<span data-ttu-id="fee9f-172">Имя пула адресных интерфейсов, который будет использоваться в подсистеме балансировки нагрузки для набора масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="fee9f-173">Если значение не задано, будет создан новый пул адресных веб-интерфейсов с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="fee9f-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="fee9f-174">-HostGroupId</span></span>
<span data-ttu-id="fee9f-175">Указывает выделенную группу узлов, в которой будет находиться установленный наборы масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="fee9f-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

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

### <span data-ttu-id="fee9f-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="fee9f-176">-ImageName</span></span>
<span data-ttu-id="fee9f-177">Имя образа для виртуальных машин в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="fee9f-178">Если значение не указано, будет использоваться изображение "центр обработки данных Windows Server 2016".</span><span class="sxs-lookup"><span data-stu-id="fee9f-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="fee9f-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="fee9f-179">-InstanceCount</span></span>
<span data-ttu-id="fee9f-180">Количество образов виртуальных машин в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="fee9f-181">Если значение не задано, будет создано 2 экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fee9f-181">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="fee9f-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="fee9f-182">-LoadBalancerName</span></span>
<span data-ttu-id="fee9f-183">Имя подсистемы балансировки нагрузки, используемой с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="fee9f-184">Если значение не задано, будет создаваться новая служба подсистемы балансировки нагрузки с тем же именем, что и набор масштабирования.</span><span class="sxs-lookup"><span data-stu-id="fee9f-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="fee9f-185">-Location</span><span class="sxs-lookup"><span data-stu-id="fee9f-185">-Location</span></span>
<span data-ttu-id="fee9f-186">Место Azure, в котором будет создан этот параметр масштабирования.</span><span class="sxs-lookup"><span data-stu-id="fee9f-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="fee9f-187">Если значение не задано, расположение будет выводиться из расположения других ресурсов, указанных в параметрах.</span><span class="sxs-lookup"><span data-stu-id="fee9f-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="fee9f-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="fee9f-188">-MaxPrice</span></span>
<span data-ttu-id="fee9f-189">Максимальная стоимость выставления счетов в наборе масштабов виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="fee9f-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="fee9f-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="fee9f-190">-NatBackendPort</span></span>
<span data-ttu-id="fee9f-191">Внутренний порт для преобразования входящего сетевого адреса.</span><span class="sxs-lookup"><span data-stu-id="fee9f-191">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="fee9f-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="fee9f-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="fee9f-193">Количество доменов сбоев для каждой группы размещения.</span><span class="sxs-lookup"><span data-stu-id="fee9f-193">Fault Domain count for each placement group.</span></span>

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

### <span data-ttu-id="fee9f-194">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="fee9f-194">-Priority</span></span>
<span data-ttu-id="fee9f-195">Приоритет виртуальной машины в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="fee9f-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="fee9f-196">Поддерживаются только значения "Regular", "плашка" и "низкий".</span><span class="sxs-lookup"><span data-stu-id="fee9f-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="fee9f-197">"Regular" предназначен для обычной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fee9f-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="fee9f-198">"Плашка" — для точечной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fee9f-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="fee9f-199">"Low" также используется для точечной виртуальной машины, но заменяется на "плашка".</span><span class="sxs-lookup"><span data-stu-id="fee9f-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="fee9f-200">Вместо "низкая" используйте "смесевых".</span><span class="sxs-lookup"><span data-stu-id="fee9f-200">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="fee9f-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="fee9f-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="fee9f-202">Идентификатор ресурса группы размещения близкого взаимодействия для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="fee9f-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="fee9f-203">-PublicIpAddressName</span></span>
<span data-ttu-id="fee9f-204">Имя общедоступного IP-адреса для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="fee9f-205">Новый общедоступный IP-адрес с тем же именем, что и у множества масштабирования, будет создан, если значение не указано.</span><span class="sxs-lookup"><span data-stu-id="fee9f-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="fee9f-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee9f-206">-ResourceGroupName</span></span>
<span data-ttu-id="fee9f-207">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="fee9f-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="fee9f-208">Если значение не задано, будет создана новая группа ресурсов с тем же именем, что и у множества.</span><span class="sxs-lookup"><span data-stu-id="fee9f-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="fee9f-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="fee9f-209">-ScaleInPolicy</span></span>
<span data-ttu-id="fee9f-210">Правила, которые следует выполнить при масштабировании, в наборе масштабов виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="fee9f-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="fee9f-211">Возможные значения: "по умолчанию", "OldestVM" и "NewestVM".</span><span class="sxs-lookup"><span data-stu-id="fee9f-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="fee9f-212">"По умолчанию" при масштабировании множества виртуальных машин, набор масштабов сначала распределяется между зонами, если он является набором масштабов Zonal.</span><span class="sxs-lookup"><span data-stu-id="fee9f-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="fee9f-213">Затем он будет надежно распределен между доменами сбоя.</span><span class="sxs-lookup"><span data-stu-id="fee9f-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="fee9f-214">В каждом домене сбоя виртуальные компьютеры, выбранные для удаления, будут новыми, не защищенными от масштабирования.</span><span class="sxs-lookup"><span data-stu-id="fee9f-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="fee9f-215">"OldestVM". при масштабировании множества масштабов виртуальной машины, для удаления будут выбраны самые старые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="fee9f-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fee9f-216">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="fee9f-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fee9f-217">В каждой зоне для удаления будут выбраны самые старые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="fee9f-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="fee9f-218">"NewestVM" при масштабировании множества виртуальных машин с масштабированием для удаления будут выбраны самые новые виртуальные машины, не защищенные с помощью масштаба.</span><span class="sxs-lookup"><span data-stu-id="fee9f-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fee9f-219">Для наборов масштабов виртуальных машин Zonal набор масштабов сначала распределяется между зонами.</span><span class="sxs-lookup"><span data-stu-id="fee9f-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fee9f-220">В каждой зоне для удаления будут выбраны новые виртуальные машины, которые не защищены.</span><span class="sxs-lookup"><span data-stu-id="fee9f-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="fee9f-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="fee9f-221">-SecurityGroupName</span></span>
<span data-ttu-id="fee9f-222">Имя группы безопасности сети, применяемой к этому набору масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="fee9f-223">Если значение не задано, будет создана группа безопасности сети по умолчанию с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="fee9f-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fee9f-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="fee9f-225">Используйте этот параметр, чтобы создать набор масштабов в одной группе размещения, по умолчанию — по нескольким группам.</span><span class="sxs-lookup"><span data-stu-id="fee9f-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="fee9f-226">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="fee9f-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="fee9f-227">Указывает, что расширения не выполняются на дополнительных переподготовленных виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="fee9f-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="fee9f-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fee9f-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="fee9f-229">Префикс адреса подсети, используемой этим набором элементов масштабирования.</span><span class="sxs-lookup"><span data-stu-id="fee9f-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="fee9f-230">Параметры подсети по умолчанию (192.168.1.0/24) будут применены, если не задано значение.</span><span class="sxs-lookup"><span data-stu-id="fee9f-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="fee9f-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="fee9f-231">-SubnetName</span></span>
<span data-ttu-id="fee9f-232">Имя подсети, используемой в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="fee9f-233">Новая подсеть будет создана с тем же именем, что и в наборе масштабирования, если значение не указано.</span><span class="sxs-lookup"><span data-stu-id="fee9f-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="fee9f-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fee9f-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="fee9f-235">Если параметр присутствует, ВМ (-ы) в наборе Scale (—) назначается (-а) управляемому системному удостоверению, которое создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="fee9f-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="fee9f-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="fee9f-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="fee9f-237">Режим политики обновления для экземпляров виртуальных машин в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="fee9f-238">Политика обновления может определять автоматические, ручные и чередующиеся обновления.</span><span class="sxs-lookup"><span data-stu-id="fee9f-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="fee9f-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fee9f-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="fee9f-240">Имя удостоверения управляемой службы, которое должно быть назначено для ВМ (ов) в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="fee9f-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fee9f-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fee9f-242">Указывает объект **VirtualMachineScaleSet** , СОДЕРЖАЩИЙ свойства VMSS, создаваемые этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fee9f-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fee9f-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fee9f-243">-VirtualNetworkName</span></span>
<span data-ttu-id="fee9f-244">Имя виртуальной сети, используемой в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="fee9f-245">Если значение не задано, будет создана новая виртуальная сеть с тем же именем, что и у множества.</span><span class="sxs-lookup"><span data-stu-id="fee9f-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="fee9f-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fee9f-246">-VMScaleSetName</span></span>
<span data-ttu-id="fee9f-247">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fee9f-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fee9f-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="fee9f-248">-VmSize</span></span>
<span data-ttu-id="fee9f-249">Размер экземпляров виртуальных машин в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="fee9f-250">Если размер не указан, будет использоваться размер по умолчанию (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="fee9f-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="fee9f-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fee9f-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="fee9f-252">Префикс адреса для виртуальной сети, используемой в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="fee9f-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="fee9f-253">Значения префиксов виртуальных сетевых адресов по умолчанию (192.168.0.0/16) будут использоваться, если не задано значение.</span><span class="sxs-lookup"><span data-stu-id="fee9f-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="fee9f-254">-Zone</span><span class="sxs-lookup"><span data-stu-id="fee9f-254">-Zone</span></span>
<span data-ttu-id="fee9f-255">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="fee9f-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="fee9f-256">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fee9f-256">-Confirm</span></span>
<span data-ttu-id="fee9f-257">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fee9f-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee9f-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee9f-258">-WhatIf</span></span>
<span data-ttu-id="fee9f-259">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fee9f-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee9f-260">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fee9f-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee9f-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee9f-261">CommonParameters</span></span>
<span data-ttu-id="fee9f-262">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fee9f-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee9f-263">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fee9f-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee9f-264">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fee9f-264">INPUTS</span></span>

### <span data-ttu-id="fee9f-265">System. String</span><span class="sxs-lookup"><span data-stu-id="fee9f-265">System.String</span></span>

### <span data-ttu-id="fee9f-266">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fee9f-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fee9f-267">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fee9f-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fee9f-268">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fee9f-268">OUTPUTS</span></span>

### <span data-ttu-id="fee9f-269">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fee9f-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fee9f-270">Пуск</span><span class="sxs-lookup"><span data-stu-id="fee9f-270">NOTES</span></span>

## <span data-ttu-id="fee9f-271">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fee9f-271">RELATED LINKS</span></span>

[<span data-ttu-id="fee9f-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fee9f-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="fee9f-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fee9f-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="fee9f-274">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fee9f-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="fee9f-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fee9f-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="fee9f-276">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fee9f-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="fee9f-277">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fee9f-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="fee9f-278">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fee9f-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


