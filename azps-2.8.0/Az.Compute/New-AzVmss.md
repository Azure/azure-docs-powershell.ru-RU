---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 780e2f9e222ec173fcce6bca88fb85f37dda1450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721818"
---
# <span data-ttu-id="cf15c-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cf15c-101">New-AzVmss</span></span>

## <span data-ttu-id="cf15c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf15c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf15c-103">Создает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf15c-103">Creates a VMSS.</span></span>

## <span data-ttu-id="cf15c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf15c-104">SYNTAX</span></span>

### <span data-ttu-id="cf15c-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf15c-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf15c-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf15c-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroup <String>] [-Priority <String>]
 [-EvictionPolicy <String>] [-MaxPrice <Double>] [-DefaultProfile <IAzureContextContainer>]
 [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf15c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf15c-107">DESCRIPTION</span></span>
<span data-ttu-id="cf15c-108">Командлет **New-AzVmss** создает набор масштабов виртуальных машин (VMSS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="cf15c-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="cf15c-109">Используйте простой набор параметров ( `SimpleParameterSet` ), чтобы быстро создать предварительно заданные VMSS и связанные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="cf15c-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="cf15c-110">Используйте набор параметров по умолчанию ( `DefaultParameter` ) для более сложных сценариев, если вам нужно точно настроить каждый компонент VMSS и каждый связанный ресурс перед его созданием.</span><span class="sxs-lookup"><span data-stu-id="cf15c-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="cf15c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf15c-111">EXAMPLES</span></span>

### <span data-ttu-id="cf15c-112">Пример 1: создание VMSS с помощью **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="cf15c-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="cf15c-113">В приведенной выше команде создаются следующие элементы с именем `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="cf15c-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="cf15c-114">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="cf15c-114">A Resource Group</span></span>
* <span data-ttu-id="cf15c-115">Виртуальная сеть</span><span class="sxs-lookup"><span data-stu-id="cf15c-115">A virtual network</span></span>
* <span data-ttu-id="cf15c-116">Подсистема балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="cf15c-116">A load balancer</span></span>
* <span data-ttu-id="cf15c-117">Общедоступный IP-адрес</span><span class="sxs-lookup"><span data-stu-id="cf15c-117">A public IP</span></span>
* <span data-ttu-id="cf15c-118">VMSS с 2 экземплярами</span><span class="sxs-lookup"><span data-stu-id="cf15c-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="cf15c-119">Изображение по умолчанию, выбранное для виртуальных машин в VMSS, `2016-Datacenter Windows Server` и SKU `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="cf15c-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="cf15c-120">Пример 2: создание VMSS с помощью **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="cf15c-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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

<span data-ttu-id="cf15c-121">В сложном примере выше создается VMSS, а далее показано, что происходит:</span><span class="sxs-lookup"><span data-stu-id="cf15c-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="cf15c-122">Первая команда создает группу ресурсов с указанным именем и расположением.</span><span class="sxs-lookup"><span data-stu-id="cf15c-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="cf15c-123">Вторая команда использует командлет **New-AzStorageAccount** для создания учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cf15c-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="cf15c-124">Третья команда затем использует командлет **Get-AzStorageAccount** для получения учетной записи хранения, созданной во второй команде, и сохраняет результат в переменной $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="cf15c-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="cf15c-125">Пятая команда использует командлет **New-AzVirtualNetworkSubnetConfig** для создания подсети и сохраняет результат в переменной с именем $SubNet.</span><span class="sxs-lookup"><span data-stu-id="cf15c-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="cf15c-126">Шестая команда использует командлет **New-AzVirtualNetwork** для создания виртуальной сети и сохраняет результат в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="cf15c-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="cf15c-127">Седьмая команда использует **Get-AzVirtualNetwork** для получения сведений о виртуальной сети, созданной в шестой команде, и сохраняет данные в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="cf15c-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="cf15c-128">В восьмом девятом — команда **New-AzPublicIpAddress** и **Get-AzureRmPublicIpAddress** используется для создания и получения сведений об общедоступном IP-адресе.</span><span class="sxs-lookup"><span data-stu-id="cf15c-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="cf15c-129">Команды хранят данные в переменной с именем $PubIP.</span><span class="sxs-lookup"><span data-stu-id="cf15c-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="cf15c-130">Десятая команда использует командлет **New-AzureRmLoadBalancerFrontendIpConfig** для создания балансировщика интерфейсной балансировки нагрузки и сохраняет результат в переменной с именем $frontend.</span><span class="sxs-lookup"><span data-stu-id="cf15c-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="cf15c-131">Одиннадцатая команда использует **New-AzLoadBalancerBackendAddressPoolConfig** для создания конфигурации пула адресов сервера и сохраняет результат в переменной с именем $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="cf15c-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="cf15c-132">Двенадцати команда использует **New-AzLoadBalancerProbeConfig** для создания пробной проверки и сохраняет данные пробы в переменной с именем $Probe.</span><span class="sxs-lookup"><span data-stu-id="cf15c-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="cf15c-133">В команде thirteenth с помощью командлета **New-AzLoadBalancerInboundNatPoolConfig** можно создать конфигурацию пула NAT для подсистемы балансировки нагрузки входящих сетевых адресов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="cf15c-134">Команда fourteenth использует **New-AzLoadBalancerRuleConfig** для создания конфигурации правила подсистемы балансировки нагрузки и сохраняет результат в переменной с именем $LBRule.</span><span class="sxs-lookup"><span data-stu-id="cf15c-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="cf15c-135">В команде пятнадцати используется командлет **New-AzLoadBalancer** для создания подсистемы балансировки нагрузки и сохранения результата в переменной с именем $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="cf15c-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="cf15c-136">В шестнадцатой команде используется **Get-AzLoadBalancer** для получения сведений о подсистеме балансировки нагрузки, созданной в команде пятнадцати, и сохраняет данные в переменной с именем $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="cf15c-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="cf15c-137">В команде Seventeenth используется командлет **New-AzVmssIPConfig** для создания конфигурации IP VMSS и сохранения сведений в переменной с именем $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="cf15c-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="cf15c-138">Команда восемнадцатым месяцами эксплуатации использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf15c-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="cf15c-139">В команде XIX для создания VMSS используется командлет **New-AzVmss** .</span><span class="sxs-lookup"><span data-stu-id="cf15c-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="cf15c-140">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf15c-140">PARAMETERS</span></span>

### <span data-ttu-id="cf15c-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="cf15c-141">-AllocationMethod</span></span>
<span data-ttu-id="cf15c-142">Метод выделения для общедоступного IP-адреса набора шкал (static или Dynamic).</span><span class="sxs-lookup"><span data-stu-id="cf15c-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="cf15c-143">Если значение не указано, выделение будет статическим.</span><span class="sxs-lookup"><span data-stu-id="cf15c-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="cf15c-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf15c-144">-AsJob</span></span>
<span data-ttu-id="cf15c-145">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="cf15c-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cf15c-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="cf15c-146">-BackendPoolName</span></span>
<span data-ttu-id="cf15c-147">Имя пула адресных адресов серверной платформы, который будет использоваться в подсистеме балансировки нагрузки для этого набора масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="cf15c-148">Если значение не задано, будет создана новая группа серверной базы данных с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="cf15c-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="cf15c-149">-BackendPort</span></span>
<span data-ttu-id="cf15c-150">Номера внутренних портов, используемые подсистемой балансировки нагрузки для связи с виртуальными машинами в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="cf15c-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="cf15c-151">Если значения не указаны, для виртуальных компьютеров Windows будут использоваться порты 3389 и 5985, а для виртуальных машин Linux будет использоваться порт 22.</span><span class="sxs-lookup"><span data-stu-id="cf15c-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="cf15c-152">-Credential</span><span class="sxs-lookup"><span data-stu-id="cf15c-152">-Credential</span></span>
<span data-ttu-id="cf15c-153">Учетные данные администратора (имя пользователя и пароль) для виртуальных машин в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="cf15c-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="cf15c-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="cf15c-155">Задает размеры дисков данных в ГБ.</span><span class="sxs-lookup"><span data-stu-id="cf15c-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="cf15c-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf15c-156">-DefaultProfile</span></span>
<span data-ttu-id="cf15c-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf15c-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf15c-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="cf15c-158">-DomainNameLabel</span></span>
<span data-ttu-id="cf15c-159">Метка доменного имени для общедоступного доменного имени Fully-Qualified (FQDN) для данного множества масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="cf15c-160">Это первый компонент доменного имени, которое автоматически назначается набору масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="cf15c-161">Автоматически назначаемые доменные имена используют форму ( <DomainNameLabel> ..). <Location> cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="cf15c-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="cf15c-162">Если значение не задано, по умолчанию будет использоваться метка доменного имени для объединения <ScaleSetName> и <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="cf15c-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="cf15c-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="cf15c-163">-EnableUltraSSD</span></span>
<span data-ttu-id="cf15c-164">Используйте диски UltraSSD для виртуальных машин в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="cf15c-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="cf15c-165">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="cf15c-165">-EvictionPolicy</span></span>
<span data-ttu-id="cf15c-166">Политика вытеснения для установленного количества виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cf15c-166">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="cf15c-167">Поддерживаются только значения "освободить" и "Удалить".</span><span class="sxs-lookup"><span data-stu-id="cf15c-167">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="cf15c-168">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="cf15c-168">-FrontendPoolName</span></span>
<span data-ttu-id="cf15c-169">Имя пула адресных интерфейсов, который будет использоваться в подсистеме балансировки нагрузки для набора масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-169">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="cf15c-170">Если значение не задано, будет создан новый пул адресных веб-интерфейсов с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-170">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="cf15c-171">-ImageName</span><span class="sxs-lookup"><span data-stu-id="cf15c-171">-ImageName</span></span>
<span data-ttu-id="cf15c-172">Имя образа для виртуальных машин в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-172">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="cf15c-173">Если значение не указано, будет использоваться изображение "центр обработки данных Windows Server 2016".</span><span class="sxs-lookup"><span data-stu-id="cf15c-173">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="cf15c-174">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="cf15c-174">-InstanceCount</span></span>
<span data-ttu-id="cf15c-175">Количество образов виртуальных машин в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-175">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="cf15c-176">Если значение не задано, будет создано 2 экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cf15c-176">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="cf15c-177">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="cf15c-177">-LoadBalancerName</span></span>
<span data-ttu-id="cf15c-178">Имя подсистемы балансировки нагрузки, используемой с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-178">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="cf15c-179">Если значение не задано, будет создаваться новая служба подсистемы балансировки нагрузки с тем же именем, что и набор масштабирования.</span><span class="sxs-lookup"><span data-stu-id="cf15c-179">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="cf15c-180">-Location</span><span class="sxs-lookup"><span data-stu-id="cf15c-180">-Location</span></span>
<span data-ttu-id="cf15c-181">Место Azure, в котором будет создан этот параметр масштабирования.</span><span class="sxs-lookup"><span data-stu-id="cf15c-181">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="cf15c-182">Если значение не задано, расположение будет выводиться из расположения других ресурсов, указанных в параметрах.</span><span class="sxs-lookup"><span data-stu-id="cf15c-182">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="cf15c-183">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="cf15c-183">-MaxPrice</span></span>
<span data-ttu-id="cf15c-184">Максимальная стоимость выставления счетов в наборе масштабов виртуальных машин с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="cf15c-184">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="cf15c-185">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="cf15c-185">-NatBackendPort</span></span>
<span data-ttu-id="cf15c-186">Внутренний порт для преобразования входящего сетевого адреса.</span><span class="sxs-lookup"><span data-stu-id="cf15c-186">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="cf15c-187">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="cf15c-187">-Priority</span></span>
<span data-ttu-id="cf15c-188">Приоритет для установленной шкалы виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="cf15c-188">The priority for the virtual machine scale set.</span></span>  <span data-ttu-id="cf15c-189">Поддерживаются только значения "Regular" и "Low".</span><span class="sxs-lookup"><span data-stu-id="cf15c-189">Only supported values are 'Regular' and 'Low'.</span></span>

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

### <span data-ttu-id="cf15c-190">-ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cf15c-190">-ProximityPlacementGroup</span></span>
<span data-ttu-id="cf15c-191">Имя или идентификатор ресурса группы размещения близкого взаимодействия, используемой с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-191">The name or resource id of the Proximity Placement Group to use with this Scale Set.</span></span>

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

### <span data-ttu-id="cf15c-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="cf15c-192">-PublicIpAddressName</span></span>
<span data-ttu-id="cf15c-193">Имя общедоступного IP-адреса для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-193">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="cf15c-194">Новый общедоступный IP-адрес с тем же именем, что и у множества масштабирования, будет создан, если значение не указано.</span><span class="sxs-lookup"><span data-stu-id="cf15c-194">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="cf15c-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf15c-195">-ResourceGroupName</span></span>
<span data-ttu-id="cf15c-196">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="cf15c-196">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="cf15c-197">Если значение не задано, будет создана новая группа ресурсов с тем же именем, что и у множества.</span><span class="sxs-lookup"><span data-stu-id="cf15c-197">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="cf15c-198">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="cf15c-198">-SecurityGroupName</span></span>
<span data-ttu-id="cf15c-199">Имя группы безопасности сети, применяемой к этому набору масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-199">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="cf15c-200">Если значение не задано, будет создана группа безопасности сети по умолчанию с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-200">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="cf15c-201">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cf15c-201">-SinglePlacementGroup</span></span>
<span data-ttu-id="cf15c-202">Используйте этот параметр, чтобы создать набор масштабов в одной группе размещения, по умолчанию — по нескольким группам.</span><span class="sxs-lookup"><span data-stu-id="cf15c-202">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="cf15c-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cf15c-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="cf15c-204">Префикс адреса подсети, используемой этим набором элементов масштабирования.</span><span class="sxs-lookup"><span data-stu-id="cf15c-204">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="cf15c-205">Параметры подсети по умолчанию (192.168.1.0/24) будут применены, если не задано значение.</span><span class="sxs-lookup"><span data-stu-id="cf15c-205">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="cf15c-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="cf15c-206">-SubnetName</span></span>
<span data-ttu-id="cf15c-207">Имя подсети, используемой в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-207">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="cf15c-208">Новая подсеть будет создана с тем же именем, что и в наборе масштабирования, если значение не указано.</span><span class="sxs-lookup"><span data-stu-id="cf15c-208">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="cf15c-209">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cf15c-209">-SystemAssignedIdentity</span></span>
<span data-ttu-id="cf15c-210">Если параметр присутствует, ВМ (-ы) в наборе Scale (—) назначается (-а) управляемому системному удостоверению, которое создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="cf15c-210">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="cf15c-211">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="cf15c-211">-UpgradePolicyMode</span></span>
<span data-ttu-id="cf15c-212">Режим политики обновления для экземпляров виртуальных машин в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-212">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="cf15c-213">Политика обновления может определять автоматические, ручные и чередующиеся обновления.</span><span class="sxs-lookup"><span data-stu-id="cf15c-213">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="cf15c-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cf15c-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="cf15c-215">Имя удостоверения управляемой службы, которое должно быть назначено для ВМ (ов) в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-215">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="cf15c-216">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf15c-216">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cf15c-217">Указывает объект **VirtualMachineScaleSet** , СОДЕРЖАЩИЙ свойства VMSS, создаваемые этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="cf15c-217">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cf15c-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="cf15c-218">-VirtualNetworkName</span></span>
<span data-ttu-id="cf15c-219">Имя виртуальной сети, используемой в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-219">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="cf15c-220">Если значение не задано, будет создана новая виртуальная сеть с тем же именем, что и у множества.</span><span class="sxs-lookup"><span data-stu-id="cf15c-220">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="cf15c-221">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cf15c-221">-VMScaleSetName</span></span>
<span data-ttu-id="cf15c-222">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="cf15c-222">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cf15c-223">-VmSize</span><span class="sxs-lookup"><span data-stu-id="cf15c-223">-VmSize</span></span>
<span data-ttu-id="cf15c-224">Размер экземпляров виртуальных машин в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-224">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="cf15c-225">Если размер не указан, будет использоваться размер по умолчанию (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="cf15c-225">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="cf15c-226">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cf15c-226">-VnetAddressPrefix</span></span>
<span data-ttu-id="cf15c-227">Префикс адреса для виртуальной сети, используемой в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="cf15c-227">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="cf15c-228">Значения префиксов виртуальных сетевых адресов по умолчанию (192.168.0.0/16) будут использоваться, если не задано значение.</span><span class="sxs-lookup"><span data-stu-id="cf15c-228">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="cf15c-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="cf15c-229">-Zone</span></span>
<span data-ttu-id="cf15c-230">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="cf15c-230">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="cf15c-231">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf15c-231">-Confirm</span></span>
<span data-ttu-id="cf15c-232">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf15c-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf15c-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf15c-233">-WhatIf</span></span>
<span data-ttu-id="cf15c-234">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf15c-234">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf15c-235">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf15c-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf15c-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf15c-236">CommonParameters</span></span>
<span data-ttu-id="cf15c-237">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf15c-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf15c-238">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf15c-238">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf15c-239">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf15c-239">INPUTS</span></span>

### <span data-ttu-id="cf15c-240">System. String</span><span class="sxs-lookup"><span data-stu-id="cf15c-240">System.String</span></span>

### <span data-ttu-id="cf15c-241">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf15c-241">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="cf15c-242">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf15c-242">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cf15c-243">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf15c-243">OUTPUTS</span></span>

### <span data-ttu-id="cf15c-244">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf15c-244">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cf15c-245">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf15c-245">NOTES</span></span>

## <span data-ttu-id="cf15c-246">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf15c-246">RELATED LINKS</span></span>

[<span data-ttu-id="cf15c-247">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cf15c-247">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="cf15c-248">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cf15c-248">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="cf15c-249">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cf15c-249">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="cf15c-250">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cf15c-250">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="cf15c-251">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cf15c-251">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="cf15c-252">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cf15c-252">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="cf15c-253">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cf15c-253">Update-AzVmss</span></span>](./Update-AzVmss.md)


