---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559183"
---
# <span data-ttu-id="6e0de-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e0de-101">New-AzureRmVM</span></span>

## <span data-ttu-id="6e0de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e0de-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0de-103">Создание виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e0de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e0de-104">SYNTAX</span></span>

### <span data-ttu-id="6e0de-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e0de-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e0de-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e0de-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e0de-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e0de-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e0de-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e0de-108">DESCRIPTION</span></span>
<span data-ttu-id="6e0de-109">Командлет **New-AzureRmVM** создает виртуальную машину в Azure.</span><span class="sxs-lookup"><span data-stu-id="6e0de-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="6e0de-110">Этот командлет принимает объект виртуальной машины в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="6e0de-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="6e0de-111">Используйте командлет New-AzureRmVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="6e0de-112">Для настройки виртуальной машины, например Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface и Set-AzureRmVMOSDisk, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="6e0de-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="6e0de-113">Этот `SimpleParameterSet` метод предоставляет удобный способ для создания ВМ, создавая общие аргументы создания виртуальных машин необязательными.</span><span class="sxs-lookup"><span data-stu-id="6e0de-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="6e0de-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e0de-114">EXAMPLES</span></span>

### <span data-ttu-id="6e0de-115">Пример 1: создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6e0de-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="6e0de-116">В этом примере сценария показано, как создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="6e0de-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="6e0de-117">Сценарий запрашивает имя пользователя и пароль для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="6e0de-118">Этот сценарий использует несколько других командлетов.</span><span class="sxs-lookup"><span data-stu-id="6e0de-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="6e0de-119">Пример 2: создание виртуальной машины из пользовательского пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="6e0de-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="6e0de-120">В этом примере для него используется существующий prepped обобщенный образ операционной системы и к нему подкрепляется диск с данными, подготавливается новая сеть, развертывается VHD и запускается.</span><span class="sxs-lookup"><span data-stu-id="6e0de-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="6e0de-121">Этот сценарий можно использовать для автоматической подготовки, так как он использует встроенные учетные данные администратора локальных виртуальных машин вместо вызова **Get-credentials** , требующего взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="6e0de-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="6e0de-122">Этот сценарий предполагает, что вы уже вошли в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="6e0de-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="6e0de-123">Вы можете подтвердить свое состояние входа с помощью командлета **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="6e0de-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="6e0de-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e0de-124">PARAMETERS</span></span>

### <span data-ttu-id="6e0de-125">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6e0de-125">-AddressPrefix</span></span>
<span data-ttu-id="6e0de-126">Префикс адреса для виртуальной сети, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-126">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-127">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="6e0de-127">-AllocationMethod</span></span>
<span data-ttu-id="6e0de-128">Метод выделения IP-адреса для общедоступного IP-адреса, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-128">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e0de-129">-AsJob</span></span>
<span data-ttu-id="6e0de-130">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6e0de-130">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6e0de-131">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="6e0de-131">-AvailabilitySetName</span></span>
<span data-ttu-id="6e0de-132">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="6e0de-132">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-133">-Credential</span><span class="sxs-lookup"><span data-stu-id="6e0de-133">-Credential</span></span>
<span data-ttu-id="6e0de-134">Учетные данные администратора для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-134">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="6e0de-135">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="6e0de-135">-DataDiskSizeInGb</span></span>
<span data-ttu-id="6e0de-136">Задает размеры дисков данных в ГБ.</span><span class="sxs-lookup"><span data-stu-id="6e0de-136">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e0de-137">-DefaultProfile</span></span>
<span data-ttu-id="6e0de-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e0de-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e0de-139">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="6e0de-139">-DisableBginfoExtension</span></span>
<span data-ttu-id="6e0de-140">Указывает на то, что этот командлет не устанавливает расширение **info для BG** на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6e0de-140">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-141">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="6e0de-141">-DiskFile</span></span>
<span data-ttu-id="6e0de-142">Локальный путь к файлу виртуального жесткого диска, который нужно отправить в облако и создать виртуальную машину, и в качестве суффикса должен быть ". VHD".</span><span class="sxs-lookup"><span data-stu-id="6e0de-142">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-143">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="6e0de-143">-DomainNameLabel</span></span>
<span data-ttu-id="6e0de-144">Метка поддомена для полного доменного имени (FQDN) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-144">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="6e0de-145">Это займет форму `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="6e0de-145">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-146">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6e0de-146">-ImageName</span></span>
<span data-ttu-id="6e0de-147">Понятное имя изображения, на основе которого будет создана виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="6e0de-147">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="6e0de-148">Сюда относятся: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE.</span><span class="sxs-lookup"><span data-stu-id="6e0de-148">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6e0de-149">-LicenseType</span></span>
<span data-ttu-id="6e0de-150">Указывает тип лицензии, указывающий на то, что образ или диск для виртуальной машины лицензирован локально.</span><span class="sxs-lookup"><span data-stu-id="6e0de-150">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="6e0de-151">Это значение используется только для изображений, которые содержат операционную систему Windows Server.</span><span class="sxs-lookup"><span data-stu-id="6e0de-151">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="6e0de-152">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6e0de-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e0de-153">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="6e0de-153">Windows_Client</span></span>
- <span data-ttu-id="6e0de-154">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="6e0de-154">Windows_Server</span></span>

<span data-ttu-id="6e0de-155">Это значение не может быть обновлено.</span><span class="sxs-lookup"><span data-stu-id="6e0de-155">This value cannot be updated.</span></span>
<span data-ttu-id="6e0de-156">Если указать этот параметр для обновления, значение должно совпадать с начальным значением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-156">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-157">-Linux</span><span class="sxs-lookup"><span data-stu-id="6e0de-157">-Linux</span></span>
<span data-ttu-id="6e0de-158">Указывает, предназначен ли диск для виртуальной машины Linux, если он указан; или Windows, если он не указан по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6e0de-158">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-159">-Location</span><span class="sxs-lookup"><span data-stu-id="6e0de-159">-Location</span></span>
<span data-ttu-id="6e0de-160">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-160">Specifies a location for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-161">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e0de-161">-Name</span></span>
<span data-ttu-id="6e0de-162">Имя ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-162">The name of the VM resource.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-163">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="6e0de-163">-OpenPorts</span></span>
<span data-ttu-id="6e0de-164">Список портов, которые нужно открыть в группе безопасности сети (NSG) для созданной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-164">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="6e0de-165">Значение по умолчанию зависит от выбранного типа изображения (например, Windows: 3389, 5985 и Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="6e0de-165">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-166">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="6e0de-166">-PublicIpAddressName</span></span>
<span data-ttu-id="6e0de-167">Имя нового (или существующего) общедоступного IP-адреса, который будет использоваться для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="6e0de-167">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="6e0de-168">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="6e0de-168">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e0de-169">-ResourceGroupName</span></span>
<span data-ttu-id="6e0de-170">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e0de-170">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-171">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="6e0de-171">-SecurityGroupName</span></span>
<span data-ttu-id="6e0de-172">Имя новой (или существующей) группы безопасности сети (NSG) для созданной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-172">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="6e0de-173">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="6e0de-173">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-174">-Size</span><span class="sxs-lookup"><span data-stu-id="6e0de-174">-Size</span></span>
<span data-ttu-id="6e0de-175">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-175">The Virtual Machine Size.</span></span>  <span data-ttu-id="6e0de-176">Значение по умолчанию: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="6e0de-176">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-177">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6e0de-177">-SubnetAddressPrefix</span></span>
<span data-ttu-id="6e0de-178">Префикс адреса для подсети, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-178">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-179">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6e0de-179">-SubnetName</span></span>
<span data-ttu-id="6e0de-180">Имя новой (или существующей) подсети, используемой для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="6e0de-180">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="6e0de-181">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="6e0de-181">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-182">-Тег</span><span class="sxs-lookup"><span data-stu-id="6e0de-182">-Tag</span></span>
<span data-ttu-id="6e0de-183">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="6e0de-183">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="6e0de-184">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="6e0de-184">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="6e0de-185">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="6e0de-185">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-186">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6e0de-186">-VirtualNetworkName</span></span>
<span data-ttu-id="6e0de-187">Имя новой (или существующей) виртуальной сети, которую нужно использовать для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="6e0de-187">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="6e0de-188">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="6e0de-188">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-189">-VM</span><span class="sxs-lookup"><span data-stu-id="6e0de-189">-VM</span></span>
<span data-ttu-id="6e0de-190">Указывает локальную виртуальную машину для создания.</span><span class="sxs-lookup"><span data-stu-id="6e0de-190">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="6e0de-191">Чтобы получить объект виртуальной машины, используйте командлет New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="6e0de-191">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="6e0de-192">Для настройки виртуальной машины, например Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage и Add-AzureRmVMNetworkInterface, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="6e0de-192">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-193">-Zone</span><span class="sxs-lookup"><span data-stu-id="6e0de-193">-Zone</span></span>
<span data-ttu-id="6e0de-194">Указывает список зон виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e0de-194">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e0de-195">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e0de-195">-Confirm</span></span>
<span data-ttu-id="6e0de-196">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e0de-196">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e0de-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e0de-197">-WhatIf</span></span>
<span data-ttu-id="6e0de-198">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e0de-198">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6e0de-199">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e0de-199">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e0de-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0de-200">CommonParameters</span></span>
<span data-ttu-id="6e0de-201">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e0de-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0de-202">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e0de-202">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0de-203">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e0de-203">INPUTS</span></span>

### <span data-ttu-id="6e0de-204">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6e0de-204">PSVirtualMachine</span></span>
<span data-ttu-id="6e0de-205">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6e0de-205">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="6e0de-206">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e0de-206">OUTPUTS</span></span>

### <span data-ttu-id="6e0de-207">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6e0de-207">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6e0de-208">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e0de-208">NOTES</span></span>

## <span data-ttu-id="6e0de-209">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e0de-209">RELATED LINKS</span></span>

[<span data-ttu-id="6e0de-210">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e0de-210">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="6e0de-211">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e0de-211">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="6e0de-212">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e0de-212">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="6e0de-213">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e0de-213">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="6e0de-214">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e0de-214">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="6e0de-215">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6e0de-215">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="6e0de-216">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6e0de-216">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="6e0de-217">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6e0de-217">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="6e0de-218">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="6e0de-218">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="6e0de-219">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="6e0de-219">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="6e0de-220">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="6e0de-220">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="6e0de-221">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="6e0de-221">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


