---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 107441c07e958099d330859a5003a2dafcd64bf9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911463"
---
# <span data-ttu-id="26213-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="26213-101">New-AzVM</span></span>

## <span data-ttu-id="26213-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26213-102">SYNOPSIS</span></span>
<span data-ttu-id="26213-103">Создание виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="26213-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26213-104">SYNTAX</span></span>

### <span data-ttu-id="26213-105">SimpleParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26213-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26213-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="26213-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26213-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="26213-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26213-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26213-108">DESCRIPTION</span></span>
<span data-ttu-id="26213-109">Командлет **New-AzVM** создает виртуальную машину в Azure.</span><span class="sxs-lookup"><span data-stu-id="26213-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="26213-110">Этот командлет принимает объект виртуальной машины в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="26213-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="26213-111">Используйте командлет New-AzVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="26213-112">Для настройки виртуальной машины, например Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface и Set-AzVMOSDisk, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="26213-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

<span data-ttu-id="26213-113">Этот `SimpleParameterSet` метод предоставляет удобный способ для создания ВМ, создавая общие аргументы создания виртуальных машин необязательными.</span><span class="sxs-lookup"><span data-stu-id="26213-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="26213-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26213-114">EXAMPLES</span></span>

### <span data-ttu-id="26213-115">Пример 1: создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="26213-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm
```

<span data-ttu-id="26213-116">В этом примере сценария показано, как создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="26213-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="26213-117">Этот сценарий использует несколько других командлетов.</span><span class="sxs-lookup"><span data-stu-id="26213-117">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="26213-118">Пример 2: создание виртуальной машины из пользовательского пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="26213-118">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="26213-119">В этом примере для него используется существующий prepped обобщенный образ операционной системы и к нему подкрепляется диск с данными, подготавливается новая сеть, развертывается VHD и запускается.</span><span class="sxs-lookup"><span data-stu-id="26213-119">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="26213-120">Этот сценарий можно использовать для автоматической подготовки, так как он использует встроенные учетные данные администратора локальных виртуальных машин вместо вызова **Get-credentials** , требующего взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="26213-120">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="26213-121">Этот сценарий предполагает, что вы уже вошли в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="26213-121">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="26213-122">Вы можете подтвердить свое состояние входа с помощью командлета **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="26213-122">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="26213-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26213-123">PARAMETERS</span></span>

### <span data-ttu-id="26213-124">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="26213-124">-AddressPrefix</span></span>
<span data-ttu-id="26213-125">Префикс адреса для виртуальной сети, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-125">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="26213-126">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="26213-126">-AllocationMethod</span></span>
<span data-ttu-id="26213-127">Метод выделения IP-адреса для общедоступного IP-адреса, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-127">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="26213-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26213-128">-AsJob</span></span>
<span data-ttu-id="26213-129">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="26213-129">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="26213-130">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="26213-130">-AvailabilitySetName</span></span>
<span data-ttu-id="26213-131">Указывает имя для группы доступности.</span><span class="sxs-lookup"><span data-stu-id="26213-131">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="26213-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="26213-132">-Credential</span></span>
<span data-ttu-id="26213-133">Учетные данные администратора для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-133">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="26213-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26213-134">-DefaultProfile</span></span>
<span data-ttu-id="26213-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26213-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26213-136">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="26213-136">-DisableBginfoExtension</span></span>
<span data-ttu-id="26213-137">Указывает на то, что этот командлет не устанавливает расширение **info для BG** на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="26213-137">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="26213-138">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="26213-138">-DiskFile</span></span>
<span data-ttu-id="26213-139">Локальный путь к файлу виртуального жесткого диска, который нужно отправить в облако и создать виртуальную машину, и в качестве суффикса должен быть ". VHD".</span><span class="sxs-lookup"><span data-stu-id="26213-139">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="26213-140">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="26213-140">-DomainNameLabel</span></span>
<span data-ttu-id="26213-141">Метка поддомена для полного доменного имени (FQDN) виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-141">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="26213-142">Это займет форму `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="26213-142">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="26213-143">-ImageName</span><span class="sxs-lookup"><span data-stu-id="26213-143">-ImageName</span></span>
<span data-ttu-id="26213-144">Понятное имя изображения, на основе которого будет создана виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="26213-144">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="26213-145">Сюда относятся: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE.</span><span class="sxs-lookup"><span data-stu-id="26213-145">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="26213-146">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="26213-146">-LicenseType</span></span>
<span data-ttu-id="26213-147">Указывает тип лицензии, указывающий на то, что образ или диск для виртуальной машины лицензирован локально.</span><span class="sxs-lookup"><span data-stu-id="26213-147">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="26213-148">Это значение используется только для изображений, которые содержат операционную систему Windows Server.</span><span class="sxs-lookup"><span data-stu-id="26213-148">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="26213-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="26213-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="26213-150">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="26213-150">Windows_Client</span></span> 
- <span data-ttu-id="26213-151">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="26213-151">Windows_Server</span></span>

<span data-ttu-id="26213-152">Это значение не может быть обновлено.</span><span class="sxs-lookup"><span data-stu-id="26213-152">This value cannot be updated.</span></span>
<span data-ttu-id="26213-153">Если указать этот параметр для обновления, значение должно совпадать с начальным значением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-153">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="26213-154">-Linux</span><span class="sxs-lookup"><span data-stu-id="26213-154">-Linux</span></span>
<span data-ttu-id="26213-155">Указывает, предназначен ли диск для виртуальной машины Linux, если он указан; или Windows, если он не указан по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="26213-155">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="26213-156">-Location</span><span class="sxs-lookup"><span data-stu-id="26213-156">-Location</span></span>
<span data-ttu-id="26213-157">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-157">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="26213-158">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26213-158">-Name</span></span>
<span data-ttu-id="26213-159">Имя ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-159">The name of the VM resource.</span></span>

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

### <span data-ttu-id="26213-160">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="26213-160">-OpenPorts</span></span>
<span data-ttu-id="26213-161">Список портов, которые нужно открыть в группе безопасности сети (NSG) для созданной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-161">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="26213-162">Значение по умолчанию зависит от выбранного типа изображения (например, Windows: 3389, 5985 и Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="26213-162">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="26213-163">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="26213-163">-PublicIpAddressName</span></span>
<span data-ttu-id="26213-164">Имя нового (или существующего) общедоступного IP-адреса, который будет использоваться для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="26213-164">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="26213-165">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="26213-165">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="26213-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26213-166">-ResourceGroupName</span></span>
<span data-ttu-id="26213-167">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26213-167">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="26213-168">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="26213-168">-SecurityGroupName</span></span>
<span data-ttu-id="26213-169">Имя новой (или существующей) группы безопасности сети (NSG) для созданной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-169">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="26213-170">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="26213-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="26213-171">-Size</span><span class="sxs-lookup"><span data-stu-id="26213-171">-Size</span></span>
<span data-ttu-id="26213-172">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-172">The Virtual Machine Size.</span></span>  <span data-ttu-id="26213-173">Значение по умолчанию: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="26213-173">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="26213-174">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="26213-174">-SubnetAddressPrefix</span></span>
<span data-ttu-id="26213-175">Префикс адреса для подсети, который будет создан для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-175">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="26213-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="26213-176">-SubnetName</span></span>
<span data-ttu-id="26213-177">Имя новой (или существующей) подсети, используемой для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="26213-177">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="26213-178">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="26213-178">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="26213-179">-Тег</span><span class="sxs-lookup"><span data-stu-id="26213-179">-Tag</span></span>
<span data-ttu-id="26213-180">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="26213-180">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="26213-181">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="26213-181">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="26213-182">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="26213-182">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="26213-183">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="26213-183">-VirtualNetworkName</span></span>
<span data-ttu-id="26213-184">Имя новой (или существующей) виртуальной сети, которую нужно использовать для созданной ВМ.</span><span class="sxs-lookup"><span data-stu-id="26213-184">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="26213-185">Если не указано, будет создано имя.</span><span class="sxs-lookup"><span data-stu-id="26213-185">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="26213-186">-VM</span><span class="sxs-lookup"><span data-stu-id="26213-186">-VM</span></span>
<span data-ttu-id="26213-187">Указывает локальную виртуальную машину для создания.</span><span class="sxs-lookup"><span data-stu-id="26213-187">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="26213-188">Чтобы получить объект виртуальной машины, используйте командлет New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="26213-188">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="26213-189">Для настройки виртуальной машины, например Set-AzVMOperatingSystem, Set-AzVMSourceImage и Add-AzVMNetworkInterface, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="26213-189">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="26213-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="26213-190">-Zone</span></span>
<span data-ttu-id="26213-191">Указывает список зон виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26213-191">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="26213-192">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26213-192">-Confirm</span></span>
<span data-ttu-id="26213-193">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26213-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26213-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26213-194">-WhatIf</span></span>
<span data-ttu-id="26213-195">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26213-195">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="26213-196">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26213-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26213-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26213-197">CommonParameters</span></span>
<span data-ttu-id="26213-198">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26213-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26213-199">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26213-199">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26213-200">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26213-200">INPUTS</span></span>

### <span data-ttu-id="26213-201">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="26213-201">PSVirtualMachine</span></span>
<span data-ttu-id="26213-202">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="26213-202">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="26213-203">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26213-203">OUTPUTS</span></span>

### <span data-ttu-id="26213-204">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="26213-204">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="26213-205">Пуск</span><span class="sxs-lookup"><span data-stu-id="26213-205">NOTES</span></span>

## <span data-ttu-id="26213-206">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26213-206">RELATED LINKS</span></span>

[<span data-ttu-id="26213-207">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="26213-207">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="26213-208">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="26213-208">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="26213-209">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="26213-209">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="26213-210">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="26213-210">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="26213-211">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="26213-211">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="26213-212">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="26213-212">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="26213-213">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="26213-213">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="26213-214">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="26213-214">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="26213-215">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="26213-215">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="26213-216">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="26213-216">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="26213-217">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="26213-217">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="26213-218">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="26213-218">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


