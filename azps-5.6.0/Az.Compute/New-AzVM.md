---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: a7fbf991357e63dbe2436350892f9e601eb586db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956435"
---
# <span data-ttu-id="22dcd-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="22dcd-101">New-AzVM</span></span>

## <span data-ttu-id="22dcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="22dcd-103">Создает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="22dcd-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="22dcd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22dcd-104">SYNTAX</span></span>

### <span data-ttu-id="22dcd-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22dcd-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>]
 [-HostId <String>] [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22dcd-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="22dcd-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22dcd-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="22dcd-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22dcd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22dcd-108">DESCRIPTION</span></span>
<span data-ttu-id="22dcd-109">С **его использованием в** Azure создается виртуальная машину.</span><span class="sxs-lookup"><span data-stu-id="22dcd-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="22dcd-110">Этот cmdlet принимает в качестве входных данных объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="22dcd-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="22dcd-111">Используйте New-AzVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="22dcd-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="22dcd-112">Для настройки виртуальной машины можно использовать другие командлеты, например Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface и Set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="22dcd-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="22dcd-113">Этот `SimpleParameterSet` способ удобен для создания VM-решения, делая необязательные аргументы создания VM.</span><span class="sxs-lookup"><span data-stu-id="22dcd-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="22dcd-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22dcd-114">EXAMPLES</span></span>

### <span data-ttu-id="22dcd-115">Пример 1. Создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="22dcd-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="22dcd-116">В этом примере показано, как создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="22dcd-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="22dcd-117">Сценарий запросит имя пользователя и пароль для VM-компьютера.</span><span class="sxs-lookup"><span data-stu-id="22dcd-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="22dcd-118">Этот сценарий использует несколько других cmdlets.</span><span class="sxs-lookup"><span data-stu-id="22dcd-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="22dcd-119">Пример 2. Создание виртуальной машины из пользовательского изображения пользователя</span><span class="sxs-lookup"><span data-stu-id="22dcd-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="22dcd-120">В этом примере принимается существующее изображение пользовательской операционной системы с общими сведениями, к нему прикрепляются диски данных, настраивается новая сеть, развертывается VHD и запускается.</span><span class="sxs-lookup"><span data-stu-id="22dcd-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="22dcd-121">Этот сценарий можно использовать для автоматической подготовка, так как он использует в тексте учетные данные администратора локальной виртуальной машины, а не вызывает **Get-Credential,** что требует взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="22dcd-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="22dcd-122">Предполагается, что вы уже вошли в свою учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="22dcd-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="22dcd-123">Вы можете подтвердить свой статус входа с помощью **cmdlet Get-AzSubscription.**</span><span class="sxs-lookup"><span data-stu-id="22dcd-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="22dcd-124">Пример 3. Создание VM-изображения из marketplace без общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="22dcd-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

<span data-ttu-id="22dcd-125">В этом примере создается новая сеть и развертывается VM-система Windows из Marketplace, не создавая общедоступный IP-адрес или группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="22dcd-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="22dcd-126">Этот сценарий можно использовать для автоматической подготовка, так как он использует в тексте учетные данные администратора локальной виртуальной машины, а не вызывает **Get-Credential,** что требует взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="22dcd-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="22dcd-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22dcd-127">PARAMETERS</span></span>

### <span data-ttu-id="22dcd-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="22dcd-128">-AddressPrefix</span></span>
<span data-ttu-id="22dcd-129">Префикс адреса для виртуальной сети, который будет создан для виртуальной виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="22dcd-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="22dcd-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="22dcd-130">-AllocationMethod</span></span>
<span data-ttu-id="22dcd-131">Способ выделения IP-адреса для общего IP-адреса, который будет создан для VM.</span><span class="sxs-lookup"><span data-stu-id="22dcd-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="22dcd-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22dcd-132">-AsJob</span></span>
<span data-ttu-id="22dcd-133">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="22dcd-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="22dcd-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="22dcd-134">-AvailabilitySetName</span></span>
<span data-ttu-id="22dcd-135">Указывает имя набора доступности.</span><span class="sxs-lookup"><span data-stu-id="22dcd-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="22dcd-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="22dcd-136">-Credential</span></span>
<span data-ttu-id="22dcd-137">Учетные данные администратора для VM.</span><span class="sxs-lookup"><span data-stu-id="22dcd-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="22dcd-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="22dcd-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="22dcd-139">Определяет размер дисков данных в ГБ.</span><span class="sxs-lookup"><span data-stu-id="22dcd-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="22dcd-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22dcd-140">-DefaultProfile</span></span>
<span data-ttu-id="22dcd-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22dcd-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22dcd-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="22dcd-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="22dcd-143">Указывает на то, что этот cmdlet не устанавливает расширение **BG Info** на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="22dcd-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="22dcd-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="22dcd-144">-DiskFile</span></span>
<span data-ttu-id="22dcd-145">Локальный путь к виртуальному жесткому диску для отправки в облако и для создания VM-файла, который должен иметь суффикс VHD.</span><span class="sxs-lookup"><span data-stu-id="22dcd-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="22dcd-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="22dcd-146">-DomainNameLabel</span></span>
<span data-ttu-id="22dcd-147">Метка поддомена для полного доменного имени (FQDN) VM.</span><span class="sxs-lookup"><span data-stu-id="22dcd-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="22dcd-148">Он примет `{domainNameLabel}.{location}.cloudapp.azure.com` форму.</span><span class="sxs-lookup"><span data-stu-id="22dcd-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="22dcd-149">-EnableUltrasSD</span><span class="sxs-lookup"><span data-stu-id="22dcd-149">-EnableUltraSSD</span></span>
<span data-ttu-id="22dcd-150">Используйте диски UltraSSD для vm.</span><span class="sxs-lookup"><span data-stu-id="22dcd-150">Use UltraSSD disks for the vm.</span></span>

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

### <span data-ttu-id="22dcd-151">-ВехионПолиция</span><span class="sxs-lookup"><span data-stu-id="22dcd-151">-EvictionPolicy</span></span>
<span data-ttu-id="22dcd-152">Политика присоединения к виртуальной машине Azure Spot.</span><span class="sxs-lookup"><span data-stu-id="22dcd-152">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="22dcd-153">Поддерживаются значения Deallocate и Delete.</span><span class="sxs-lookup"><span data-stu-id="22dcd-153">Supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="22dcd-154">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="22dcd-154">-HostGroupId</span></span>
<span data-ttu-id="22dcd-155">Указывает выделенную группу хостов, в которые будет находиться виртуальная машину.</span><span class="sxs-lookup"><span data-stu-id="22dcd-155">Specifies the dedicated host group the virtual machine will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22dcd-156">-HostId</span><span class="sxs-lookup"><span data-stu-id="22dcd-156">-HostId</span></span>
<span data-ttu-id="22dcd-157">ИД хоста</span><span class="sxs-lookup"><span data-stu-id="22dcd-157">The Id of Host</span></span>

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

### <span data-ttu-id="22dcd-158">-Image</span><span class="sxs-lookup"><span data-stu-id="22dcd-158">-Image</span></span>
<span data-ttu-id="22dcd-159">Удобное имя изображения, на котором будет встроено VM-решение.</span><span class="sxs-lookup"><span data-stu-id="22dcd-159">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="22dcd-160">К ним относятся: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="22dcd-160">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="22dcd-161">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="22dcd-161">-LicenseType</span></span>
<span data-ttu-id="22dcd-162">Тип лицензии, который указывает на то, что изображение или диск для виртуальной машины были лицензированы локально.</span><span class="sxs-lookup"><span data-stu-id="22dcd-162">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="22dcd-163">Возможные значения для Windows Server:</span><span class="sxs-lookup"><span data-stu-id="22dcd-163">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="22dcd-164">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="22dcd-164">Windows_Client</span></span>
- <span data-ttu-id="22dcd-165">Windows_Server возможности операционной системы Linux Server:</span><span class="sxs-lookup"><span data-stu-id="22dcd-165">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="22dcd-166">RHEL_BYOS (для RHEL)</span><span class="sxs-lookup"><span data-stu-id="22dcd-166">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="22dcd-167">SLES_BYOS (для SUSE)</span><span class="sxs-lookup"><span data-stu-id="22dcd-167">SLES_BYOS (for SUSE)</span></span> 

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

### <span data-ttu-id="22dcd-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="22dcd-168">-Linux</span></span>
<span data-ttu-id="22dcd-169">Указывает, является ли дисковый файл для Linux VM (если он указан); или Windows, если они не указаны по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22dcd-169">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="22dcd-170">-Location</span><span class="sxs-lookup"><span data-stu-id="22dcd-170">-Location</span></span>
<span data-ttu-id="22dcd-171">Определяет расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="22dcd-171">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="22dcd-172">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="22dcd-172">-MaxPrice</span></span>
<span data-ttu-id="22dcd-173">Максимальная цена выставить счет виртуальной машины с низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="22dcd-173">The max price of the billing of a low priority virtual machine.</span></span>

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

### <span data-ttu-id="22dcd-174">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="22dcd-174">-EncryptionAtHost</span></span>
<span data-ttu-id="22dcd-175">Свойство EncryptionAtHost может использоваться пользователем в запросе для того, чтобы включить или отключить шифрование хоста для набора масштаба виртуальной машины или виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="22dcd-175">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="22dcd-176">Это позволит шифровать все диски, включая диск Resource/Temp на самом хосте.</span><span class="sxs-lookup"><span data-stu-id="22dcd-176">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="22dcd-177">По умолчанию: шифрование на хосте будет отключено, если это свойство не имеет значения true для ресурса.</span><span class="sxs-lookup"><span data-stu-id="22dcd-177">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskParameterSet
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="22dcd-178">-Name</span><span class="sxs-lookup"><span data-stu-id="22dcd-178">-Name</span></span>
<span data-ttu-id="22dcd-179">Имя ресурса VM.</span><span class="sxs-lookup"><span data-stu-id="22dcd-179">The name of the VM resource.</span></span>

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

### <span data-ttu-id="22dcd-180">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="22dcd-180">-OpenPorts</span></span>
<span data-ttu-id="22dcd-181">Список портов, которые нужно открыть в группе безопасности сети (NSG) для созданного VM-порта.</span><span class="sxs-lookup"><span data-stu-id="22dcd-181">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="22dcd-182">Значение по умолчанию зависит от типа выбранного изображения (например, Windows: 3389, 5985 и Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="22dcd-182">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="22dcd-183">-Priority</span><span class="sxs-lookup"><span data-stu-id="22dcd-183">-Priority</span></span>
<span data-ttu-id="22dcd-184">Приоритет виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="22dcd-184">The priority for the virtual machine.</span></span>  <span data-ttu-id="22dcd-185">Поддерживаются только такие значения, как "Обычный", "Spot" и "Низкий".</span><span class="sxs-lookup"><span data-stu-id="22dcd-185">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="22dcd-186">"Обычный" — для обычных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="22dcd-186">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="22dcd-187">Spot — для spot virtual machine.</span><span class="sxs-lookup"><span data-stu-id="22dcd-187">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="22dcd-188">"Низкая" также для spot virtual machine, но заменяется spot.</span><span class="sxs-lookup"><span data-stu-id="22dcd-188">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="22dcd-189">Используйте "Spot" вместо "Низкий".</span><span class="sxs-lookup"><span data-stu-id="22dcd-189">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="22dcd-190">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="22dcd-190">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="22dcd-191">ИД ресурса группы расположения близости, который можно использовать с этой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="22dcd-191">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22dcd-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="22dcd-192">-PublicIpAddressName</span></span>
<span data-ttu-id="22dcd-193">Имя нового (или существующего) общего IP-адреса создаемого VM-адреса.</span><span class="sxs-lookup"><span data-stu-id="22dcd-193">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="22dcd-194">Если не указано, будет сгенерировано имя.</span><span class="sxs-lookup"><span data-stu-id="22dcd-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="22dcd-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22dcd-195">-ResourceGroupName</span></span>
<span data-ttu-id="22dcd-196">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="22dcd-196">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="22dcd-197">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="22dcd-197">-SecurityGroupName</span></span>
<span data-ttu-id="22dcd-198">Имя новой (или существующей) группы безопасности сети (NSG) для созданной VM-системы.</span><span class="sxs-lookup"><span data-stu-id="22dcd-198">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="22dcd-199">Если не указано, будет сгенерировано имя.</span><span class="sxs-lookup"><span data-stu-id="22dcd-199">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="22dcd-200">-Size</span><span class="sxs-lookup"><span data-stu-id="22dcd-200">-Size</span></span>
<span data-ttu-id="22dcd-201">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="22dcd-201">The Virtual Machine Size.</span></span>  <span data-ttu-id="22dcd-202">Значение по умолчанию: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="22dcd-202">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="22dcd-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="22dcd-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="22dcd-204">Префикс адреса для подсети, которая будет создана для VM-решения.</span><span class="sxs-lookup"><span data-stu-id="22dcd-204">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="22dcd-205">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="22dcd-205">-SubnetName</span></span>
<span data-ttu-id="22dcd-206">Имя новой (или существующей) подсети для созданной VM-системы.</span><span class="sxs-lookup"><span data-stu-id="22dcd-206">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="22dcd-207">Если не указано, будет сгенерировано имя.</span><span class="sxs-lookup"><span data-stu-id="22dcd-207">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="22dcd-208">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="22dcd-208">-SystemAssignedIdentity</span></span>
<span data-ttu-id="22dcd-209">Если параметр присутствует, то VM назначено управляемое системное удостоверение, которое генерируется автоматически.</span><span class="sxs-lookup"><span data-stu-id="22dcd-209">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="22dcd-210">-Tag</span><span class="sxs-lookup"><span data-stu-id="22dcd-210">-Tag</span></span>
<span data-ttu-id="22dcd-211">Указывает, что ресурсы и группы ресурсов могут быть помечены парой имен и значений.</span><span class="sxs-lookup"><span data-stu-id="22dcd-211">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="22dcd-212">Добавив теги к ресурсам, вы сможете сгруппить ресурсы в группах ресурсов и создать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="22dcd-212">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="22dcd-213">Каждая группа ресурсов может иметь не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="22dcd-213">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="22dcd-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="22dcd-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="22dcd-215">Имя управляемого удостоверения службы, которое должно быть назначено VM.</span><span class="sxs-lookup"><span data-stu-id="22dcd-215">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="22dcd-216">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="22dcd-216">-VirtualNetworkName</span></span>
<span data-ttu-id="22dcd-217">Имя новой (или существующей) виртуальной сети для создаемой виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="22dcd-217">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="22dcd-218">Если не указано, будет сгенерировано имя.</span><span class="sxs-lookup"><span data-stu-id="22dcd-218">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="22dcd-219">-VM</span><span class="sxs-lookup"><span data-stu-id="22dcd-219">-VM</span></span>
<span data-ttu-id="22dcd-220">Указывает локализованную виртуальную машину, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="22dcd-220">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="22dcd-221">Чтобы получить объект виртуальной машины, воспользуйтесь New-AzVMConfig..</span><span class="sxs-lookup"><span data-stu-id="22dcd-221">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="22dcd-222">Для настройки виртуальной машины можно использовать другие командлеты, например Set-AzVMOperatingSystem, Set-AzVMSourceImage и Add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="22dcd-222">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="22dcd-223">-VmssId</span><span class="sxs-lookup"><span data-stu-id="22dcd-223">-VmssId</span></span>
<span data-ttu-id="22dcd-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span><span class="sxs-lookup"><span data-stu-id="22dcd-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span></span>

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

### <span data-ttu-id="22dcd-225">-Zone</span><span class="sxs-lookup"><span data-stu-id="22dcd-225">-Zone</span></span>
<span data-ttu-id="22dcd-226">Определяет список зон виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="22dcd-226">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="22dcd-227">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22dcd-227">-Confirm</span></span>
<span data-ttu-id="22dcd-228">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22dcd-228">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22dcd-229">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22dcd-229">-WhatIf</span></span>
<span data-ttu-id="22dcd-230">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22dcd-230">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22dcd-231">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="22dcd-231">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22dcd-232">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22dcd-232">CommonParameters</span></span>
<span data-ttu-id="22dcd-233">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22dcd-233">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22dcd-234">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22dcd-234">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22dcd-235">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22dcd-235">INPUTS</span></span>

### <span data-ttu-id="22dcd-236">System.String</span><span class="sxs-lookup"><span data-stu-id="22dcd-236">System.String</span></span>

### <span data-ttu-id="22dcd-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="22dcd-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="22dcd-238">System.String[]</span><span class="sxs-lookup"><span data-stu-id="22dcd-238">System.String[]</span></span>

### <span data-ttu-id="22dcd-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="22dcd-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22dcd-240">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22dcd-240">OUTPUTS</span></span>

### <span data-ttu-id="22dcd-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="22dcd-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="22dcd-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="22dcd-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="22dcd-243">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22dcd-243">NOTES</span></span>

## <span data-ttu-id="22dcd-244">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22dcd-244">RELATED LINKS</span></span>

[<span data-ttu-id="22dcd-245">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="22dcd-245">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="22dcd-246">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="22dcd-246">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="22dcd-247">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="22dcd-247">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="22dcd-248">Start-AzvM</span><span class="sxs-lookup"><span data-stu-id="22dcd-248">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="22dcd-249">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="22dcd-249">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="22dcd-250">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="22dcd-250">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="22dcd-251">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="22dcd-251">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="22dcd-252">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="22dcd-252">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="22dcd-253">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="22dcd-253">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="22dcd-254">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="22dcd-254">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="22dcd-255">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="22dcd-255">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="22dcd-256">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="22dcd-256">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


