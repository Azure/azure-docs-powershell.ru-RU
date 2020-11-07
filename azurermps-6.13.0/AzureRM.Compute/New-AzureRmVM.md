---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: da307e1bc5bca5c3127e33a32bb4480148fe14a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733000"
---
# <span data-ttu-id="9d585-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9d585-101">New-AzureRmVM</span></span>

## <span data-ttu-id="9d585-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d585-102">SYNOPSIS</span></span>
<span data-ttu-id="9d585-103">Создание виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d585-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d585-104">SYNTAX</span></span>

### <span data-ttu-id="9d585-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d585-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d585-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d585-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d585-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d585-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d585-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d585-108">DESCRIPTION</span></span>
<span data-ttu-id="9d585-109">Командлет **New-AzureRmVM** создает виртуальную машину в Azure.</span><span class="sxs-lookup"><span data-stu-id="9d585-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="9d585-110">Этот командлет принимает объект виртуальной машины в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="9d585-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="9d585-111">Используйте командлет New-AzureRmVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="9d585-112">Для настройки виртуальной машины, например Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface и Set-AzureRmVMOSDisk, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="9d585-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>
<span data-ttu-id="9d585-113">Этот `SimpleParameterSet` метод предоставляет удобный способ для создания ВМ, создавая общие аргументы создания виртуальных машин необязательными.</span><span class="sxs-lookup"><span data-stu-id="9d585-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="9d585-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d585-114">EXAMPLES</span></span>

### <span data-ttu-id="9d585-115">Пример 1: создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="9d585-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="9d585-116">В этом примере сценария показано, как создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="9d585-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="9d585-117">Сценарий запрашивает имя пользователя и пароль для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="9d585-118">Этот сценарий использует несколько других командлетов.</span><span class="sxs-lookup"><span data-stu-id="9d585-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="9d585-119">Пример 2: создание виртуальной машины из пользовательского пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="9d585-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="9d585-120">В этом примере для него используется существующий prepped обобщенный образ операционной системы и к нему подкрепляется диск с данными, подготавливается новая сеть, развертывается VHD и запускается.</span><span class="sxs-lookup"><span data-stu-id="9d585-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="9d585-121">Этот сценарий можно использовать для автоматической подготовки, так как он использует встроенные учетные данные администратора локальных виртуальных машин вместо вызова **Get-credentials** , требующего взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="9d585-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="9d585-122">Этот сценарий предполагает, что вы уже вошли в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="9d585-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="9d585-123">Вы можете подтвердить свое состояние входа с помощью командлета **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="9d585-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

### <span data-ttu-id="9d585-124">Пример 3: создание виртуальной машины из образа Marketplace без общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="9d585-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="9d585-125">В этом примере выполняется подготовка новой сети и развертывание виртуальной машины Windows из Marketplace без создания общедоступного IP-адреса или группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="9d585-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="9d585-126">Этот сценарий можно использовать для автоматической подготовки, так как он использует встроенные учетные данные администратора локальных виртуальных машин вместо вызова **Get-credentials** , требующего взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="9d585-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="9d585-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d585-127">PARAMETERS</span></span>

### <span data-ttu-id="9d585-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9d585-128">-AddressPrefix</span></span>
<span data-ttu-id="9d585-129">Префикс адреса для виртуальной сети, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="9d585-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="9d585-130">-AllocationMethod</span></span>
<span data-ttu-id="9d585-131">Метод выделения IP-адреса для общедоступного IP-адреса, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="9d585-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d585-132">-AsJob</span></span>
<span data-ttu-id="9d585-133">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9d585-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9d585-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="9d585-134">-AvailabilitySetName</span></span>
<span data-ttu-id="9d585-135">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="9d585-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="9d585-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="9d585-136">-Credential</span></span>
<span data-ttu-id="9d585-137">Учетные данные администратора для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="9d585-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="9d585-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="9d585-139">Задает размеры дисков данных в ГБ.</span><span class="sxs-lookup"><span data-stu-id="9d585-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="9d585-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d585-140">-DefaultProfile</span></span>
<span data-ttu-id="9d585-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d585-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d585-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="9d585-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="9d585-143">Указывает на то, что этот командлет не устанавливает расширение **info для BG** на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9d585-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="9d585-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="9d585-144">-DiskFile</span></span>
<span data-ttu-id="9d585-145">Локальный путь к файлу виртуального жесткого диска, который нужно отправить в облако и создать виртуальную машину, и в качестве суффикса должен быть ". VHD".</span><span class="sxs-lookup"><span data-stu-id="9d585-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="9d585-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="9d585-146">-DomainNameLabel</span></span>
<span data-ttu-id="9d585-147">Метка поддомена для полного доменного имени (FQDN) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="9d585-148">Это займет форму `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="9d585-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="9d585-149">-Image</span><span class="sxs-lookup"><span data-stu-id="9d585-149">-Image</span></span>
<span data-ttu-id="9d585-150">Понятное имя изображения, на основе которого будет создана виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="9d585-150">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="9d585-151">Сюда относятся: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE.</span><span class="sxs-lookup"><span data-stu-id="9d585-151">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="9d585-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9d585-152">-LicenseType</span></span>
<span data-ttu-id="9d585-153">Указывает тип лицензии, указывающий на то, что образ или диск для виртуальной машины лицензирован локально.</span><span class="sxs-lookup"><span data-stu-id="9d585-153">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="9d585-154">Это значение используется только для изображений, которые содержат операционную систему Windows Server.</span><span class="sxs-lookup"><span data-stu-id="9d585-154">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="9d585-155">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9d585-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d585-156">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="9d585-156">Windows_Client</span></span>
- <span data-ttu-id="9d585-157">Windows_Server это значение не может быть обновлено.</span><span class="sxs-lookup"><span data-stu-id="9d585-157">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="9d585-158">Если указать этот параметр для обновления, значение должно совпадать с начальным значением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-158">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="9d585-159">-Linux</span><span class="sxs-lookup"><span data-stu-id="9d585-159">-Linux</span></span>
<span data-ttu-id="9d585-160">Указывает, предназначен ли диск для виртуальной машины Linux, если он указан; или Windows, если он не указан по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9d585-160">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="9d585-161">-Location</span><span class="sxs-lookup"><span data-stu-id="9d585-161">-Location</span></span>
<span data-ttu-id="9d585-162">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-162">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="9d585-163">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d585-163">-Name</span></span>
<span data-ttu-id="9d585-164">Имя ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-164">The name of the VM resource.</span></span>

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

### <span data-ttu-id="9d585-165">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="9d585-165">-OpenPorts</span></span>
<span data-ttu-id="9d585-166">Список портов, которые нужно открыть в группе безопасности сети (NSG) для созданной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-166">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="9d585-167">Значение по умолчанию зависит от выбранного типа изображения (например, Windows: 3389, 5985 и Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="9d585-167">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="9d585-168">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="9d585-168">-PublicIpAddressName</span></span>
<span data-ttu-id="9d585-169">Имя нового (или существующего) общедоступного IP-адреса, который будет использоваться для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="9d585-169">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="9d585-170">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="9d585-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="9d585-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d585-171">-ResourceGroupName</span></span>
<span data-ttu-id="9d585-172">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d585-172">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9d585-173">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="9d585-173">-SecurityGroupName</span></span>
<span data-ttu-id="9d585-174">Имя новой (или существующей) группы безопасности сети (NSG) для созданной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-174">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="9d585-175">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="9d585-175">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="9d585-176">-Size</span><span class="sxs-lookup"><span data-stu-id="9d585-176">-Size</span></span>
<span data-ttu-id="9d585-177">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-177">The Virtual Machine Size.</span></span>  <span data-ttu-id="9d585-178">Значение по умолчанию: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="9d585-178">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="9d585-179">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9d585-179">-SubnetAddressPrefix</span></span>
<span data-ttu-id="9d585-180">Префикс адреса для подсети, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-180">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="9d585-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="9d585-181">-SubnetName</span></span>
<span data-ttu-id="9d585-182">Имя новой (или существующей) подсети, используемой для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="9d585-182">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="9d585-183">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="9d585-183">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="9d585-184">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9d585-184">-SystemAssignedIdentity</span></span>
<span data-ttu-id="9d585-185">Если параметр присутствует, ВМ назначается управляемое системное удостоверение, которое создается автоматически.</span><span class="sxs-lookup"><span data-stu-id="9d585-185">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="9d585-186">-Тег</span><span class="sxs-lookup"><span data-stu-id="9d585-186">-Tag</span></span>
<span data-ttu-id="9d585-187">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="9d585-187">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="9d585-188">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="9d585-188">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="9d585-189">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="9d585-189">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="9d585-190">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9d585-190">-UserAssignedIdentity</span></span>
<span data-ttu-id="9d585-191">Имя удостоверения управляемой службы, которое должно быть назначено виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9d585-191">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="9d585-192">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="9d585-192">-VirtualNetworkName</span></span>
<span data-ttu-id="9d585-193">Имя новой (или существующей) виртуальной сети, которую нужно использовать для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="9d585-193">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="9d585-194">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="9d585-194">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="9d585-195">-VM</span><span class="sxs-lookup"><span data-stu-id="9d585-195">-VM</span></span>
<span data-ttu-id="9d585-196">Указывает локальную виртуальную машину для создания.</span><span class="sxs-lookup"><span data-stu-id="9d585-196">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="9d585-197">Чтобы получить объект виртуальной машины, используйте командлет New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="9d585-197">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="9d585-198">Для настройки виртуальной машины, например Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage и Add-AzureRmVMNetworkInterface, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="9d585-198">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="9d585-199">-Zone</span><span class="sxs-lookup"><span data-stu-id="9d585-199">-Zone</span></span>
<span data-ttu-id="9d585-200">Указывает список зон виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9d585-200">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="9d585-201">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d585-201">-Confirm</span></span>
<span data-ttu-id="9d585-202">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9d585-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d585-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d585-203">-WhatIf</span></span>
<span data-ttu-id="9d585-204">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9d585-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d585-205">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9d585-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d585-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d585-206">CommonParameters</span></span>
<span data-ttu-id="9d585-207">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d585-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d585-208">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d585-208">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d585-209">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d585-209">INPUTS</span></span>

### <span data-ttu-id="9d585-210">System. String</span><span class="sxs-lookup"><span data-stu-id="9d585-210">System.String</span></span>

### <span data-ttu-id="9d585-211">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9d585-211">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="9d585-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="9d585-212">System.String[]</span></span>

### <span data-ttu-id="9d585-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9d585-213">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9d585-214">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d585-214">OUTPUTS</span></span>

### <span data-ttu-id="9d585-215">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9d585-215">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="9d585-216">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9d585-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9d585-217">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d585-217">NOTES</span></span>

## <span data-ttu-id="9d585-218">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d585-218">RELATED LINKS</span></span>

[<span data-ttu-id="9d585-219">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9d585-219">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9d585-220">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9d585-220">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="9d585-221">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9d585-221">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="9d585-222">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9d585-222">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="9d585-223">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9d585-223">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="9d585-224">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9d585-224">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="9d585-225">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9d585-225">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="9d585-226">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9d585-226">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="9d585-227">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9d585-227">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="9d585-228">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9d585-228">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="9d585-229">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="9d585-229">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="9d585-230">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="9d585-230">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


