---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: dfcd408e3afa7988b06a1e020d76844c48d990b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559148"
---
# <span data-ttu-id="a7485-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="a7485-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="a7485-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7485-102">SYNOPSIS</span></span>
<span data-ttu-id="a7485-103">Задает свойства диска операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7485-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7485-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7485-104">SYNTAX</span></span>

### <span data-ttu-id="a7485-105">DefaultParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7485-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes>
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7485-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="a7485-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7485-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7485-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

### <span data-ttu-id="a7485-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="a7485-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7485-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7485-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [-CreateOption] <DiskCreateOptionTypes> [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [<CommonParameters>]
```

## <span data-ttu-id="a7485-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7485-110">DESCRIPTION</span></span>
<span data-ttu-id="a7485-111">Командлет **Set-AzureRmVMOSDisk** задает свойства диска операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7485-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="a7485-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7485-112">EXAMPLES</span></span>

### <span data-ttu-id="a7485-113">Пример 1: Настройка свойств виртуальной машины из образа платформы</span><span class="sxs-lookup"><span data-stu-id="a7485-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="a7485-114">Первая команда получает группу доступности с именем AvailablitySet13 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a7485-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a7485-115">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a7485-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a7485-116">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a7485-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a7485-117">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a7485-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a7485-118">Последняя команда задает свойства виртуальной машины в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a7485-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="a7485-119">Пример 2: Настройка свойств виртуальной машины из обобщенного пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="a7485-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="a7485-120">Первая команда получает группу доступности с именем AvailablitySet13 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a7485-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a7485-121">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a7485-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a7485-122">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a7485-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a7485-123">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a7485-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a7485-124">Последняя команда задает свойства виртуальной машины в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a7485-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="a7485-125">Пример 3: Настройка свойств виртуальной машины из специального пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="a7485-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="a7485-126">Первая команда получает группу доступности с именем AvailablitySet13 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a7485-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a7485-127">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a7485-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a7485-128">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a7485-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a7485-129">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="a7485-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a7485-130">Последняя команда задает свойства виртуальной машины в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a7485-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="a7485-131">Пример 4: Настройка параметров шифрования дисков на диске операционной системы виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="a7485-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="a7485-132">В этом примере устанавливаются параметры шифрования дисков на диске операционной системы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7485-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="a7485-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7485-133">PARAMETERS</span></span>

### <span data-ttu-id="a7485-134">-Caching</span><span class="sxs-lookup"><span data-stu-id="a7485-134">-Caching</span></span>
<span data-ttu-id="a7485-135">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a7485-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="a7485-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a7485-136">Valid values are:</span></span> 

- <span data-ttu-id="a7485-137">Чтения</span><span class="sxs-lookup"><span data-stu-id="a7485-137">ReadOnly</span></span>
- <span data-ttu-id="a7485-138">Операцию</span><span class="sxs-lookup"><span data-stu-id="a7485-138">ReadWrite</span></span>

<span data-ttu-id="a7485-139">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="a7485-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="a7485-140">Изменение значения Caching приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7485-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="a7485-141">Этот параметр влияет на производительность диска.</span><span class="sxs-lookup"><span data-stu-id="a7485-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-142">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="a7485-142">-CreateOption</span></span>
<span data-ttu-id="a7485-143">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа либо добавляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="a7485-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="a7485-144">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a7485-144">Valid values are:</span></span> 

- <span data-ttu-id="a7485-145">Подключает.</span><span class="sxs-lookup"><span data-stu-id="a7485-145">Attach.</span></span>
<span data-ttu-id="a7485-146">Укажите этот параметр, чтобы создать виртуальную машину на основе специализированного диска.</span><span class="sxs-lookup"><span data-stu-id="a7485-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="a7485-147">Если вы задаете этот параметр, не указывайте параметр *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="a7485-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="a7485-148">Вместо этого используйте командлет Set-AzureRmVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="a7485-148">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="a7485-149">Кроме того, вы должны использовать параметры *Windows* или *Linux* , чтобы сообщить платформе azure2 тип операционной системы на виртуальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="a7485-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="a7485-150">Параметр *VhdUri* достаточно для того, чтобы сообщить платформе azure2 расположение диска для присоединения.</span><span class="sxs-lookup"><span data-stu-id="a7485-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="a7485-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="a7485-151">FromImage.</span></span>
<span data-ttu-id="a7485-152">Укажите этот параметр, чтобы создать виртуальную машину на основе образа платформы или обобщенного пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="a7485-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="a7485-153">В случае обобщенного образа пользователя также необходимо указать параметр *SourceImageUri* и параметры *Windows* или *Linux* , чтобы сообщить платформе Azure расположение и тип диска операционной системы, а не использовать командлет **Set-AzureRmVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="a7485-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="a7485-154">В случае с изображением платформы достаточно параметра *VhdUri* .</span><span class="sxs-lookup"><span data-stu-id="a7485-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="a7485-155">Очистку.</span><span class="sxs-lookup"><span data-stu-id="a7485-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-156">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="a7485-156">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="a7485-157">Указывает расположение ключа шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="a7485-157">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-158">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="a7485-158">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="a7485-159">Указывает ИД ресурса для хранилища ключей, содержащего ключ шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="a7485-159">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-160">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a7485-160">-DiskSizeInGB</span></span>
<span data-ttu-id="a7485-161">Задает размер (в ГБ) диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a7485-161">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-162">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="a7485-162">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="a7485-163">Задает расположение ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="a7485-163">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-164">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="a7485-164">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="a7485-165">Указывает ИД ресурса для хранилища ключей, содержащего ключ шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="a7485-165">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="a7485-166">-Linux</span></span>
<span data-ttu-id="a7485-167">Указывает, что операционная система на пользовательском изображении — Linux.</span><span class="sxs-lookup"><span data-stu-id="a7485-167">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="a7485-168">Укажите этот параметр для развертывания виртуальной машины на основе пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="a7485-168">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="a7485-169">-ManagedDiskId</span></span>
<span data-ttu-id="a7485-170">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="a7485-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-171">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7485-171">-Name</span></span>
<span data-ttu-id="a7485-172">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a7485-172">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="a7485-173">-SourceImageUri</span></span>
<span data-ttu-id="a7485-174">Задает универсальный код ресурса (URI) для сценариев пользователей в формате VHD.</span><span class="sxs-lookup"><span data-stu-id="a7485-174">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a7485-175">-StorageAccountType</span></span>
<span data-ttu-id="a7485-176">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="a7485-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="a7485-177">-VhdUri</span></span>
<span data-ttu-id="a7485-178">Задает универсальный код ресурса (URI) виртуального жесткого диска (VHD).</span><span class="sxs-lookup"><span data-stu-id="a7485-178">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="a7485-179">Для виртуальной машины на основе изображений этот параметр указывает VHD-файл, который будет создан при указании образа платформы или пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="a7485-179">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="a7485-180">Это расположение, из которого копируется большой двоичный объект (BLOB), чтобы запустить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a7485-180">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="a7485-181">Для сценария загрузки виртуальной машины на диске этот параметр указывает VHD-файл, который виртуальная машина использует для запуска.</span><span class="sxs-lookup"><span data-stu-id="a7485-181">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-182">-VM</span><span class="sxs-lookup"><span data-stu-id="a7485-182">-VM</span></span>
<span data-ttu-id="a7485-183">Указывает локальный объект виртуальной машины, на котором нужно задать свойства диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a7485-183">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="a7485-184">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="a7485-184">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-185">-Windows</span><span class="sxs-lookup"><span data-stu-id="a7485-185">-Windows</span></span>
<span data-ttu-id="a7485-186">Указывает, что операционная система на пользовательском изображении — Windows.</span><span class="sxs-lookup"><span data-stu-id="a7485-186">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7485-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7485-187">CommonParameters</span></span>
<span data-ttu-id="a7485-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7485-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7485-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7485-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7485-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7485-190">INPUTS</span></span>

### <span data-ttu-id="a7485-191">Ничего</span><span class="sxs-lookup"><span data-stu-id="a7485-191">None</span></span>
<span data-ttu-id="a7485-192">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a7485-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7485-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7485-193">OUTPUTS</span></span>

## <span data-ttu-id="a7485-194">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7485-194">NOTES</span></span>

## <span data-ttu-id="a7485-195">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7485-195">RELATED LINKS</span></span>

[<span data-ttu-id="a7485-196">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a7485-196">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a7485-197">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a7485-197">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="a7485-198">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="a7485-198">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


