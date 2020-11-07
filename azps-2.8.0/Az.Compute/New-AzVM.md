---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 4350a1bca25d94f2d3fab27c202eda4392180027
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721830"
---
# <span data-ttu-id="7b700-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7b700-101">New-AzVM</span></span>

## <span data-ttu-id="7b700-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b700-102">SYNOPSIS</span></span>
<span data-ttu-id="7b700-103">Создание виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="7b700-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b700-104">SYNTAX</span></span>

### <span data-ttu-id="7b700-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b700-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroup <String>]
 [-HostId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b700-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b700-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b700-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b700-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroup <String>] [-HostId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b700-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b700-108">DESCRIPTION</span></span>
<span data-ttu-id="7b700-109">Командлет **New-AzVM** создает виртуальную машину в Azure.</span><span class="sxs-lookup"><span data-stu-id="7b700-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="7b700-110">Этот командлет принимает объект виртуальной машины в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="7b700-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="7b700-111">Используйте командлет New-AzVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="7b700-112">Для настройки виртуальной машины, например Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface и Set-AzVMOSDisk, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="7b700-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="7b700-113">Этот `SimpleParameterSet` метод предоставляет удобный способ для создания ВМ, создавая общие аргументы создания виртуальных машин необязательными.</span><span class="sxs-lookup"><span data-stu-id="7b700-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="7b700-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b700-114">EXAMPLES</span></span>

### <span data-ttu-id="7b700-115">Пример 1: создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="7b700-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="7b700-116">В этом примере сценария показано, как создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="7b700-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="7b700-117">Сценарий запрашивает имя пользователя и пароль для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="7b700-118">Этот сценарий использует несколько других командлетов.</span><span class="sxs-lookup"><span data-stu-id="7b700-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="7b700-119">Пример 2: создание виртуальной машины из пользовательского пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="7b700-119">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account.
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance.
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3"
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="7b700-120">В этом примере для него используется существующий prepped обобщенный образ операционной системы и к нему подкрепляется диск с данными, подготавливается новая сеть, развертывается VHD и запускается.</span><span class="sxs-lookup"><span data-stu-id="7b700-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="7b700-121">Этот сценарий можно использовать для автоматической подготовки, так как он использует встроенные учетные данные администратора локальных виртуальных машин вместо вызова **Get-credentials** , требующего взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="7b700-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="7b700-122">Этот сценарий предполагает, что вы уже вошли в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="7b700-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="7b700-123">Вы можете подтвердить свое состояние входа с помощью командлета **Get-AzSubscription** .</span><span class="sxs-lookup"><span data-stu-id="7b700-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="7b700-124">Пример 3: создание виртуальной машины из образа Marketplace без общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="7b700-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="7b700-125">В этом примере выполняется подготовка новой сети и развертывание виртуальной машины Windows из Marketplace без создания общедоступного IP-адреса или группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="7b700-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="7b700-126">Этот сценарий можно использовать для автоматической подготовки, так как он использует встроенные учетные данные администратора локальных виртуальных машин вместо вызова **Get-credentials** , требующего взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="7b700-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="7b700-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b700-127">PARAMETERS</span></span>

### <span data-ttu-id="7b700-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7b700-128">-AddressPrefix</span></span>
<span data-ttu-id="7b700-129">Префикс адреса для виртуальной сети, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="7b700-130">-AllocationMethod</span></span>
<span data-ttu-id="7b700-131">Метод выделения IP-адреса для общедоступного IP-адреса, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b700-132">-AsJob</span></span>
<span data-ttu-id="7b700-133">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7b700-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7b700-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="7b700-134">-AvailabilitySetName</span></span>
<span data-ttu-id="7b700-135">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="7b700-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="7b700-136">-Credential</span></span>
<span data-ttu-id="7b700-137">Учетные данные администратора для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="7b700-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="7b700-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="7b700-139">Задает размеры дисков данных в ГБ.</span><span class="sxs-lookup"><span data-stu-id="7b700-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b700-140">-DefaultProfile</span></span>
<span data-ttu-id="7b700-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b700-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b700-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="7b700-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="7b700-143">Указывает на то, что этот командлет не устанавливает расширение **info для BG** на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7b700-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="7b700-144">-DiskFile</span></span>
<span data-ttu-id="7b700-145">Локальный путь к файлу виртуального жесткого диска, который нужно отправить в облако и создать виртуальную машину, и в качестве суффикса должен быть ". VHD".</span><span class="sxs-lookup"><span data-stu-id="7b700-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="7b700-146">-DomainNameLabel</span></span>
<span data-ttu-id="7b700-147">Метка поддомена для полного доменного имени (FQDN) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="7b700-148">Это займет форму `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="7b700-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="7b700-149">-EnableUltraSSD</span></span>
<span data-ttu-id="7b700-150">Используйте диски UltraSSD для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-150">Use UltraSSD disks for the vm.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7b700-151">-EvictionPolicy</span></span>
<span data-ttu-id="7b700-152">Политика вытеснения для виртуальной машины с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="7b700-152">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="7b700-153">Только поддерживаемое значение — "освободить".</span><span class="sxs-lookup"><span data-stu-id="7b700-153">Only supported value is 'Deallocate'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-154">-HostId</span><span class="sxs-lookup"><span data-stu-id="7b700-154">-HostId</span></span>
<span data-ttu-id="7b700-155">Идентификатор узла</span><span class="sxs-lookup"><span data-stu-id="7b700-155">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-156">-Image</span><span class="sxs-lookup"><span data-stu-id="7b700-156">-Image</span></span>
<span data-ttu-id="7b700-157">Понятное имя изображения, на основе которого будет создана виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="7b700-157">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="7b700-158">Сюда относятся: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE.</span><span class="sxs-lookup"><span data-stu-id="7b700-158">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="7b700-159">-LicenseType</span></span>
<span data-ttu-id="7b700-160">Указывает тип лицензии, указывающий на то, что образ или диск для виртуальной машины лицензирован локально.</span><span class="sxs-lookup"><span data-stu-id="7b700-160">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="7b700-161">Это значение используется только для изображений, которые содержат операционную систему Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7b700-161">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="7b700-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7b700-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7b700-163">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="7b700-163">Windows_Client</span></span>
- <span data-ttu-id="7b700-164">Windows_Server это значение не может быть обновлено.</span><span class="sxs-lookup"><span data-stu-id="7b700-164">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="7b700-165">Если указать этот параметр для обновления, значение должно совпадать с начальным значением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-165">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="7b700-166">-Linux</span></span>
<span data-ttu-id="7b700-167">Указывает, предназначен ли диск для виртуальной машины Linux, если он указан; или Windows, если он не указан по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7b700-167">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-168">-Location</span><span class="sxs-lookup"><span data-stu-id="7b700-168">-Location</span></span>
<span data-ttu-id="7b700-169">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-169">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="7b700-170">-MaxPrice</span></span>
<span data-ttu-id="7b700-171">Максимальная стоимость выставления счетов для виртуальной машины с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="7b700-171">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-172">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b700-172">-Name</span></span>
<span data-ttu-id="7b700-173">Имя ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-173">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-174">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="7b700-174">-OpenPorts</span></span>
<span data-ttu-id="7b700-175">Список портов, которые нужно открыть в группе безопасности сети (NSG) для созданной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-175">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="7b700-176">Значение по умолчанию зависит от выбранного типа изображения (например, Windows: 3389, 5985 и Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="7b700-176">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-177">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="7b700-177">-Priority</span></span>
<span data-ttu-id="7b700-178">Приоритет виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-178">The priority for the virtual machine.</span></span>  <span data-ttu-id="7b700-179">Поддерживаются только значения "Regular" и "Low".</span><span class="sxs-lookup"><span data-stu-id="7b700-179">Only supported values are 'Regular' and 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-180">-ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7b700-180">-ProximityPlacementGroup</span></span>
<span data-ttu-id="7b700-181">Имя или идентификатор ресурса группы размещения близкого взаимодействия, используемой с этой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="7b700-181">The name or resource id of the Proximity Placement Group to use with this VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-182">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="7b700-182">-PublicIpAddressName</span></span>
<span data-ttu-id="7b700-183">Имя нового (или существующего) общедоступного IP-адреса, который будет использоваться для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="7b700-183">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="7b700-184">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="7b700-184">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b700-185">-ResourceGroupName</span></span>
<span data-ttu-id="7b700-186">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b700-186">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-187">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="7b700-187">-SecurityGroupName</span></span>
<span data-ttu-id="7b700-188">Имя новой (или существующей) группы безопасности сети (NSG) для созданной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-188">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="7b700-189">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="7b700-189">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-190">-Size</span><span class="sxs-lookup"><span data-stu-id="7b700-190">-Size</span></span>
<span data-ttu-id="7b700-191">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-191">The Virtual Machine Size.</span></span>  <span data-ttu-id="7b700-192">Значение по умолчанию: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="7b700-192">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-193">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7b700-193">-SubnetAddressPrefix</span></span>
<span data-ttu-id="7b700-194">Префикс адреса для подсети, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-194">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-195">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="7b700-195">-SubnetName</span></span>
<span data-ttu-id="7b700-196">Имя новой (или существующей) подсети, используемой для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="7b700-196">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="7b700-197">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="7b700-197">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-198">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7b700-198">-SystemAssignedIdentity</span></span>
<span data-ttu-id="7b700-199">Если параметр присутствует, ВМ назначается управляемое системное удостоверение, которое создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="7b700-199">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-200">-Тег</span><span class="sxs-lookup"><span data-stu-id="7b700-200">-Tag</span></span>
<span data-ttu-id="7b700-201">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="7b700-201">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="7b700-202">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="7b700-202">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="7b700-203">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="7b700-203">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-204">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7b700-204">-UserAssignedIdentity</span></span>
<span data-ttu-id="7b700-205">Имя удостоверения управляемой службы, которое должно быть назначено виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7b700-205">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-206">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="7b700-206">-VirtualNetworkName</span></span>
<span data-ttu-id="7b700-207">Имя новой (или существующей) виртуальной сети, которую нужно использовать для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="7b700-207">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="7b700-208">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="7b700-208">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-209">-VM</span><span class="sxs-lookup"><span data-stu-id="7b700-209">-VM</span></span>
<span data-ttu-id="7b700-210">Указывает локальную виртуальную машину для создания.</span><span class="sxs-lookup"><span data-stu-id="7b700-210">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="7b700-211">Чтобы получить объект виртуальной машины, используйте командлет New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="7b700-211">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="7b700-212">Для настройки виртуальной машины, например Set-AzVMOperatingSystem, Set-AzVMSourceImage и Add-AzVMNetworkInterface, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="7b700-212">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-213">-Zone</span><span class="sxs-lookup"><span data-stu-id="7b700-213">-Zone</span></span>
<span data-ttu-id="7b700-214">Указывает список зон виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7b700-214">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b700-215">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b700-215">-Confirm</span></span>
<span data-ttu-id="7b700-216">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b700-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b700-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b700-217">-WhatIf</span></span>
<span data-ttu-id="7b700-218">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b700-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b700-219">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b700-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b700-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b700-220">CommonParameters</span></span>
<span data-ttu-id="7b700-221">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b700-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b700-222">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b700-222">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b700-223">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b700-223">INPUTS</span></span>

### <span data-ttu-id="7b700-224">System. String</span><span class="sxs-lookup"><span data-stu-id="7b700-224">System.String</span></span>

### <span data-ttu-id="7b700-225">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7b700-225">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7b700-226">System. String []</span><span class="sxs-lookup"><span data-stu-id="7b700-226">System.String[]</span></span>

### <span data-ttu-id="7b700-227">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7b700-227">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7b700-228">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b700-228">OUTPUTS</span></span>

### <span data-ttu-id="7b700-229">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7b700-229">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="7b700-230">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7b700-230">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7b700-231">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b700-231">NOTES</span></span>

## <span data-ttu-id="7b700-232">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b700-232">RELATED LINKS</span></span>

[<span data-ttu-id="7b700-233">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7b700-233">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7b700-234">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="7b700-234">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="7b700-235">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="7b700-235">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="7b700-236">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="7b700-236">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="7b700-237">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="7b700-237">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="7b700-238">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7b700-238">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="7b700-239">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7b700-239">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="7b700-240">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7b700-240">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="7b700-241">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7b700-241">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="7b700-242">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7b700-242">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="7b700-243">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="7b700-243">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="7b700-244">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="7b700-244">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


