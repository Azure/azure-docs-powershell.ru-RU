---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: a5a15ed27b5a862513b15667b343e932dc2571e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569636"
---
# <span data-ttu-id="9f01a-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f01a-101">New-AzureRmVM</span></span>

## <span data-ttu-id="9f01a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f01a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f01a-103">Создание виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9f01a-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f01a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f01a-104">SYNTAX</span></span>

```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tags <Hashtable>] [-LicenseType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f01a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f01a-105">DESCRIPTION</span></span>
<span data-ttu-id="9f01a-106">Командлет **New-AzureRmVM** создает виртуальную машину в Azure.</span><span class="sxs-lookup"><span data-stu-id="9f01a-106">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="9f01a-107">Этот командлет принимает объект виртуальной машины в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="9f01a-107">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="9f01a-108">Используйте командлет New-AzureRmVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9f01a-108">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="9f01a-109">Для настройки виртуальной машины, например Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface и Set-AzureRmVMOSDisk, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="9f01a-109">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="9f01a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f01a-110">EXAMPLES</span></span>

### <span data-ttu-id="9f01a-111">Пример 1: создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="9f01a-111">Example 1: Create a virtual machine</span></span>
```
PS C:\> # Variables    
## Global
$ResourceGroupName = "ResourceGroup11"
$Location = "WestEurope"

## Storage
$StorageName = "generalstorage6cc"
$StorageType = "Standard_GRS"

## Network
$InterfaceName = "ServerInterface06"
$Subnet1Name = "Subnet1"
$VNetName = "VNet09"
$VNetAddressPrefix = "10.0.0.0/16"
$VNetSubnetAddressPrefix = "10.0.0.0/24"

## Compute
$VMName = "VirtualMachine12"
$ComputerName = "Server22"
$VMSize = "Standard_A2"
$OSDiskName = $VMName + "OSDisk"

# Resource Group
New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Type $StorageType -Location $Location

# Network
$PIp = New-AzureRmPublicIpAddress -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -AllocationMethod Dynamic
$SubnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name $Subnet1Name -AddressPrefix $VNetSubnetAddressPrefix
$VNet = New-AzureRmVirtualNetwork -Name $VNetName -ResourceGroupName $ResourceGroupName -Location $Location -AddressPrefix $VNetAddressPrefix -Subnet $SubnetConfig
$Interface = New-AzureRmNetworkInterface -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -SubnetId $VNet.Subnets[0].Id -PublicIpAddressId $PIp.Id

# Compute

## Setup local VM object
$Credential = Get-Credential
$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2012-R2-Datacenter -Version "latest"
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $Interface.Id
$OSDiskUri = $StorageAccount.PrimaryEndpoints.Blob.ToString() + "vhds/" + $OSDiskName + ".vhd"
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -CreateOption FromImage

## Create the VM in Azure
New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $Location -VM $VirtualMachine
```

<span data-ttu-id="9f01a-112">В этом примере сценария показано, как создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="9f01a-112">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="9f01a-113">Этот сценарий использует несколько других командлетов.</span><span class="sxs-lookup"><span data-stu-id="9f01a-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="9f01a-114">Пример 2: создание виртуальной машины из пользовательского пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="9f01a-114">Example 2: Create a virtual machine from a custom user image</span></span>
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

$Crededntial = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword); 

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="9f01a-115">В этом примере для него используется существующий prepped обобщенный образ операционной системы и к нему подкрепляется диск с данными, подготавливается новая сеть, развертывается VHD и запускается.</span><span class="sxs-lookup"><span data-stu-id="9f01a-115">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="9f01a-116">Этот сценарий можно использовать для автоматической подготовки, так как он использует встроенные учетные данные администратора локальных виртуальных машин вместо вызова **Get-credentials** , требующего взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="9f01a-116">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="9f01a-117">Этот сценарий предполагает, что вы уже вошли в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="9f01a-117">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="9f01a-118">Вы можете подтвердить свое состояние входа с помощью командлета **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="9f01a-118">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="9f01a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f01a-119">PARAMETERS</span></span>

### <span data-ttu-id="9f01a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f01a-120">-DefaultProfile</span></span>
<span data-ttu-id="9f01a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f01a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f01a-122">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="9f01a-122">-DisableBginfoExtension</span></span>
<span data-ttu-id="9f01a-123">Указывает на то, что этот командлет не устанавливает расширение **info для BG** на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9f01a-123">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="9f01a-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9f01a-124">-LicenseType</span></span>
<span data-ttu-id="9f01a-125">Указывает тип лицензии, указывающий на то, что образ или диск для виртуальной машины лицензирован локально.</span><span class="sxs-lookup"><span data-stu-id="9f01a-125">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="9f01a-126">Это значение используется только для изображений, которые содержат операционную систему Windows Server.</span><span class="sxs-lookup"><span data-stu-id="9f01a-126">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="9f01a-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9f01a-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f01a-128">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="9f01a-128">Windows_Client</span></span> 
- <span data-ttu-id="9f01a-129">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="9f01a-129">Windows_Server</span></span>

<span data-ttu-id="9f01a-130">Это значение не может быть обновлено.</span><span class="sxs-lookup"><span data-stu-id="9f01a-130">This value cannot be updated.</span></span>
<span data-ttu-id="9f01a-131">Если указать этот параметр для обновления, значение должно совпадать с начальным значением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9f01a-131">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f01a-132">-Location</span><span class="sxs-lookup"><span data-stu-id="9f01a-132">-Location</span></span>
<span data-ttu-id="9f01a-133">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9f01a-133">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f01a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f01a-134">-ResourceGroupName</span></span>
<span data-ttu-id="9f01a-135">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f01a-135">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f01a-136">-Теги</span><span class="sxs-lookup"><span data-stu-id="9f01a-136">-Tags</span></span>
<span data-ttu-id="9f01a-137">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="9f01a-137">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="9f01a-138">Добавление тегов к ресурсам позволяет группировать ресурсы по группам ресурсов и создавать собственные представления.</span><span class="sxs-lookup"><span data-stu-id="9f01a-138">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="9f01a-139">Каждый ресурс или группа ресурсов может содержать не более 15 тегов.</span><span class="sxs-lookup"><span data-stu-id="9f01a-139">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f01a-140">-VM</span><span class="sxs-lookup"><span data-stu-id="9f01a-140">-VM</span></span>
<span data-ttu-id="9f01a-141">Указывает локальную виртуальную машину для создания.</span><span class="sxs-lookup"><span data-stu-id="9f01a-141">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="9f01a-142">Чтобы получить объект виртуальной машины, используйте командлет New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="9f01a-142">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="9f01a-143">Для настройки виртуальной машины, например Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage и Add-AzureRmVMNetworkInterface, можно использовать другие командлеты.</span><span class="sxs-lookup"><span data-stu-id="9f01a-143">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f01a-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="9f01a-144">-Zone</span></span>
<span data-ttu-id="9f01a-145">Указывает список зон виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9f01a-145">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f01a-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f01a-146">-Confirm</span></span>
<span data-ttu-id="9f01a-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f01a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f01a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f01a-148">-WhatIf</span></span>
<span data-ttu-id="9f01a-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f01a-149">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9f01a-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f01a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f01a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f01a-151">CommonParameters</span></span>
<span data-ttu-id="9f01a-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f01a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f01a-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f01a-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f01a-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f01a-154">INPUTS</span></span>

## <span data-ttu-id="9f01a-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f01a-155">OUTPUTS</span></span>

## <span data-ttu-id="9f01a-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f01a-156">NOTES</span></span>

## <span data-ttu-id="9f01a-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f01a-157">RELATED LINKS</span></span>

[<span data-ttu-id="9f01a-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f01a-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9f01a-159">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f01a-159">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="9f01a-160">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f01a-160">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="9f01a-161">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f01a-161">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="9f01a-162">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f01a-162">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="9f01a-163">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9f01a-163">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="9f01a-164">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9f01a-164">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="9f01a-165">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9f01a-165">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="9f01a-166">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9f01a-166">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="9f01a-167">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9f01a-167">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="9f01a-168">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="9f01a-168">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="9f01a-169">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="9f01a-169">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


