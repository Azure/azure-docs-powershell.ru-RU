---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: fc788d40cbcd807ef05be4ab43fcda4371aaa084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911455"
---
# <span data-ttu-id="30f21-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30f21-101">New-AzVmss</span></span>

## <span data-ttu-id="30f21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30f21-102">SYNOPSIS</span></span>
<span data-ttu-id="30f21-103">Создает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="30f21-103">Creates a VMSS.</span></span>

## <span data-ttu-id="30f21-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30f21-104">SYNTAX</span></span>

### <span data-ttu-id="30f21-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="30f21-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30f21-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="30f21-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30f21-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30f21-107">DESCRIPTION</span></span>
<span data-ttu-id="30f21-108">Командлет **New-AzVmss** создает набор масштабов виртуальных машин (VMSS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="30f21-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="30f21-109">Этот командлет принимает объект **VirtualMachineScaleSet** в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="30f21-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="30f21-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30f21-110">EXAMPLES</span></span>

### <span data-ttu-id="30f21-111">Пример 1: создание VMSS</span><span class="sxs-lookup"><span data-stu-id="30f21-111">Example 1: Create a VMSS</span></span>
```
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

<span data-ttu-id="30f21-112">В следующем сложном примере создается VMSS.</span><span class="sxs-lookup"><span data-stu-id="30f21-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="30f21-113">Первая команда создает группу ресурсов с указанным именем и расположением.</span><span class="sxs-lookup"><span data-stu-id="30f21-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="30f21-114">Вторая команда использует командлет **New-AzStorageAccount** для создания учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="30f21-114">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="30f21-115">Третья команда затем использует командлет **Get-AzStorageAccount** для получения учетной записи хранения, созданной во второй команде, и сохраняет результат в переменной $STOAccount.</span><span class="sxs-lookup"><span data-stu-id="30f21-115">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="30f21-116">Пятая команда использует командлет **New-AzVirtualNetworkSubnetConfig** для создания подсети и сохраняет результат в переменной с именем $SubNet.</span><span class="sxs-lookup"><span data-stu-id="30f21-116">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="30f21-117">Шестая команда использует командлет **New-AzVirtualNetwork** для создания виртуальной сети и сохраняет результат в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="30f21-117">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="30f21-118">Седьмая команда использует **Get-AzVirtualNetwork** для получения сведений о виртуальной сети, созданной в шестой команде, и сохраняет данные в переменной с именем $VNet.</span><span class="sxs-lookup"><span data-stu-id="30f21-118">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="30f21-119">В восьмом девятом — команда **New-AzPublicIpAddress** и **Get-AzureRmPublicIpAddress** используется для создания и получения сведений об общедоступном IP-адресе.</span><span class="sxs-lookup"><span data-stu-id="30f21-119">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="30f21-120">Команды хранят данные в переменной с именем $PubIP.</span><span class="sxs-lookup"><span data-stu-id="30f21-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="30f21-121">Десятая команда использует командлет **New-AzureRmLoadBalancerFrontendIpConfig** для создания балансировщика интерфейсной балансировки нагрузки и сохраняет результат в переменной с именем $frontend.</span><span class="sxs-lookup"><span data-stu-id="30f21-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="30f21-122">Одиннадцатая команда использует **New-AzLoadBalancerBackendAddressPoolConfig** для создания конфигурации пула адресов сервера и сохраняет результат в переменной с именем $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="30f21-122">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="30f21-123">Двенадцати команда использует **New-AzLoadBalancerProbeConfig** для создания пробной проверки и сохраняет данные пробы в переменной с именем $Probe.</span><span class="sxs-lookup"><span data-stu-id="30f21-123">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="30f21-124">В команде thirteenth с помощью командлета **New-AzLoadBalancerInboundNatPoolConfig** можно создать конфигурацию пула NAT для подсистемы балансировки нагрузки входящих сетевых адресов.</span><span class="sxs-lookup"><span data-stu-id="30f21-124">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="30f21-125">Команда fourteenth использует **New-AzLoadBalancerRuleConfig** для создания конфигурации правила подсистемы балансировки нагрузки и сохраняет результат в переменной с именем $LBRule.</span><span class="sxs-lookup"><span data-stu-id="30f21-125">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="30f21-126">В команде пятнадцати используется командлет **New-AzLoadBalancer** для создания подсистемы балансировки нагрузки и сохранения результата в переменной с именем $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="30f21-126">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="30f21-127">В шестнадцатой команде используется **Get-AzLoadBalancer** для получения сведений о подсистеме балансировки нагрузки, созданной в команде пятнадцати, и сохраняет данные в переменной с именем $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="30f21-127">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="30f21-128">В команде Seventeenth используется командлет **New-AzVmssIPConfig** для создания конфигурации IP VMSS и сохранения сведений в переменной с именем $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="30f21-128">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="30f21-129">Команда восемнадцатым месяцами эксплуатации использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="30f21-129">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="30f21-130">В команде XIX для создания VMSS используется командлет **New-AzVmss** .</span><span class="sxs-lookup"><span data-stu-id="30f21-130">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="30f21-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30f21-131">PARAMETERS</span></span>

### <span data-ttu-id="30f21-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="30f21-132">-AllocationMethod</span></span>
<span data-ttu-id="30f21-133">Метод выделения для общедоступного IP-адреса набора шкал (static или Dynamic).</span><span class="sxs-lookup"><span data-stu-id="30f21-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="30f21-134">Если значение не указано, выделение будет статическим.</span><span class="sxs-lookup"><span data-stu-id="30f21-134">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30f21-135">-AsJob</span></span>
<span data-ttu-id="30f21-136">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="30f21-136">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="30f21-137">-BackendPoolName</span></span>
<span data-ttu-id="30f21-138">Имя пула адресных адресов серверной платформы, который будет использоваться в подсистеме балансировки нагрузки для этого набора масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="30f21-139">Если значение не задано, будет создана новая группа серверной базы данных с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="30f21-140">-BackendPort</span></span>
<span data-ttu-id="30f21-141">Номера внутренних портов, используемые подсистемой балансировки нагрузки для связи с виртуальными машинами в установленном масштабе.</span><span class="sxs-lookup"><span data-stu-id="30f21-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="30f21-142">Если значения не указаны, для виртуальных компьютеров Windows будут использоваться порты 3389 и 5985, а для виртуальных машин Linux будет использоваться порт 22.</span><span class="sxs-lookup"><span data-stu-id="30f21-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-143">-Credential</span><span class="sxs-lookup"><span data-stu-id="30f21-143">-Credential</span></span>
<span data-ttu-id="30f21-144">Учетные данные администратора (имя пользователя и пароль) для виртуальных машин в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f21-145">-DefaultProfile</span></span>
<span data-ttu-id="30f21-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30f21-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="30f21-147">-DomainNameLabel</span></span>
<span data-ttu-id="30f21-148">Метка доменного имени для общедоступного доменного имени Fully-Qualified (FQDN) для данного множества масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="30f21-149">Это первый компонент доменного имени, который автоматически assiged с набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-149">This is the first component of the domain name that is automatically assiged to the Scale Set.</span></span> <span data-ttu-id="30f21-150">Автоматически назначаемые доменные имена используют форму ( <DomainNameLabel> ..). <Location> cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="30f21-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="30f21-151">Если значение не задано, по умолчанию будет использоваться метка доменного имени для объединения <ScaleSetName> и <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="30f21-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="30f21-152">-FrontendPoolName</span></span>
<span data-ttu-id="30f21-153">Имя пула адресных интерфейсов, usein locad подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="30f21-153">The name of the frontend address pool to usein the Scale Set locad balancer.</span></span>  <span data-ttu-id="30f21-154">Если значение не задано, будет создан новый пул адресных веб-интерфейсов с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-155">-ImageName</span><span class="sxs-lookup"><span data-stu-id="30f21-155">-ImageName</span></span>
<span data-ttu-id="30f21-156">Имя образа для виртуальных машин в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="30f21-157">Если значение не указано, будет использоваться изображение "центр обработки данных Windows Server 2016".</span><span class="sxs-lookup"><span data-stu-id="30f21-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="30f21-158">-InstanceCount</span></span>
<span data-ttu-id="30f21-159">Количество образов виртуальных машин в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="30f21-160">Если значение не задано, будет создано 2 экземпляра.</span><span class="sxs-lookup"><span data-stu-id="30f21-160">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="30f21-161">-LoadBalancerName</span></span>
<span data-ttu-id="30f21-162">Имя подсистемы балансировки нагрузки, используемой с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="30f21-163">Если значение не задано, будет создаваться новая служба подсистемы балансировки нагрузки с тем же именем, что и набор масштабирования.</span><span class="sxs-lookup"><span data-stu-id="30f21-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-164">-Location</span><span class="sxs-lookup"><span data-stu-id="30f21-164">-Location</span></span>
<span data-ttu-id="30f21-165">Место Azure, в котором будет создан этот параметр масштабирования.</span><span class="sxs-lookup"><span data-stu-id="30f21-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="30f21-166">Если значение не задано, расположение будет выводиться из расположения других ресурсов, указанных в параметрах.</span><span class="sxs-lookup"><span data-stu-id="30f21-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="30f21-167">-NatBackendPort</span></span>
<span data-ttu-id="30f21-168">Внутренний порт для преобразования входящего сетевого адреса.</span><span class="sxs-lookup"><span data-stu-id="30f21-168">Backend port for inbound network address translation.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="30f21-169">-PublicIpAddressName</span></span>
<span data-ttu-id="30f21-170">Имя общедоступного IP-адреса для использования с этим набором масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="30f21-171">Новый общедоступный IP-адрес с тем же именем, что и у множества масштабирования, будет создан, если значение не указано.</span><span class="sxs-lookup"><span data-stu-id="30f21-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f21-172">-ResourceGroupName</span></span>
<span data-ttu-id="30f21-173">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="30f21-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="30f21-174">Если значение не задано, будет создана новая группа ресурсов с тем же именем, что и у множества.</span><span class="sxs-lookup"><span data-stu-id="30f21-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="30f21-175">-SecurityGroupName</span></span>
<span data-ttu-id="30f21-176">Имя группы безопасности сети, применяемой к этому набору масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="30f21-177">Если значение не задано, будет создана группа безопасности сети по умолчанию с тем же именем, что и в наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="30f21-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="30f21-179">Префикс адреса подсети, используемой этим набором элементов масштабирования.</span><span class="sxs-lookup"><span data-stu-id="30f21-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="30f21-180">Параметры подсети по умолчанию (192.168.1.0/24) будут применены, если не задано значение.</span><span class="sxs-lookup"><span data-stu-id="30f21-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="30f21-181">-SubnetName</span></span>
<span data-ttu-id="30f21-182">Имя подсети, используемой в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="30f21-183">Новая подсеть будет создана с тем же именем, что и в наборе масштабирования, если значение не указано.</span><span class="sxs-lookup"><span data-stu-id="30f21-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="30f21-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="30f21-185">Режим политики обновления для экземпляров виртуальных машин в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="30f21-186">Политика обновления может определять автоматические, ручные и чередующиеся обновления.</span><span class="sxs-lookup"><span data-stu-id="30f21-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="30f21-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="30f21-188">Указывает объект **VirtualMachineScaleSet** , СОДЕРЖАЩИЙ свойства VMSS, создаваемые этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="30f21-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="30f21-189">-VirtualNetworkName</span></span>
<span data-ttu-id="30f21-190">Имя виртуальной сети, используемой в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="30f21-191">Если значение не задано, будет создана новая виртуальная сеть с тем же именем, что и у множества.</span><span class="sxs-lookup"><span data-stu-id="30f21-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="30f21-192">-VMScaleSetName</span></span>
<span data-ttu-id="30f21-193">Указывает имя VMSS, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="30f21-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="30f21-194">-VmSize</span></span>
<span data-ttu-id="30f21-195">Размер экземпляров виртуальных машин в этом наборе масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="30f21-196">Если размер не указан, будет использоваться размер по умолчанию (Standard_DS1_v2).</span><span class="sxs-lookup"><span data-stu-id="30f21-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="30f21-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="30f21-198">Префикс адреса для виртуальной сети, используемой в этом множестве масштабов.</span><span class="sxs-lookup"><span data-stu-id="30f21-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="30f21-199">Значения префиксов виртуальных сетевых адресов по умолчанию (192.168.0.0/16) будут использоваться, если не задано значение.</span><span class="sxs-lookup"><span data-stu-id="30f21-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f21-200">-Zone</span><span class="sxs-lookup"><span data-stu-id="30f21-200">-Zone</span></span>
<span data-ttu-id="30f21-201">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="30f21-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="30f21-202">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30f21-202">-Confirm</span></span>
<span data-ttu-id="30f21-203">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30f21-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f21-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f21-204">-WhatIf</span></span>
<span data-ttu-id="30f21-205">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30f21-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="30f21-206">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30f21-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f21-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f21-207">CommonParameters</span></span>
<span data-ttu-id="30f21-208">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30f21-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f21-209">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30f21-209">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f21-210">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30f21-210">INPUTS</span></span>

### <span data-ttu-id="30f21-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="30f21-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="30f21-212">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="30f21-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="30f21-213">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30f21-213">OUTPUTS</span></span>

### <span data-ttu-id="30f21-214">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="30f21-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="30f21-215">Пуск</span><span class="sxs-lookup"><span data-stu-id="30f21-215">NOTES</span></span>

## <span data-ttu-id="30f21-216">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30f21-216">RELATED LINKS</span></span>

[<span data-ttu-id="30f21-217">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30f21-217">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="30f21-218">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30f21-218">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="30f21-219">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30f21-219">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="30f21-220">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30f21-220">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="30f21-221">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30f21-221">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="30f21-222">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30f21-222">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="30f21-223">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30f21-223">Update-AzVmss</span></span>](./Update-AzVmss.md)


