---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: ff6945369f16e9c7996ab9be80dcefce759926a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731226"
---
# <span data-ttu-id="e4783-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="e4783-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="e4783-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4783-102">SYNOPSIS</span></span>
<span data-ttu-id="e4783-103">Задает свойства диска операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e4783-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="e4783-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4783-104">SYNTAX</span></span>

### <span data-ttu-id="e4783-105">DefaultParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4783-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4783-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="e4783-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4783-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4783-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4783-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="e4783-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4783-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4783-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4783-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4783-110">DESCRIPTION</span></span>
<span data-ttu-id="e4783-111">Командлет **Set-AzVMOSDisk** задает свойства диска операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e4783-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="e4783-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4783-112">EXAMPLES</span></span>

### <span data-ttu-id="e4783-113">Пример 1: Настройка свойств виртуальной машины из образа платформы</span><span class="sxs-lookup"><span data-stu-id="e4783-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="e4783-114">Первая команда получает группу доступности с именем AvailablitySet13 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e4783-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e4783-115">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e4783-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e4783-116">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e4783-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e4783-117">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e4783-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e4783-118">Последняя команда задает свойства виртуальной машины в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e4783-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="e4783-119">Пример 2: Настройка свойств виртуальной машины из обобщенного пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="e4783-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="e4783-120">Первая команда получает группу доступности с именем AvailablitySet13 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e4783-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e4783-121">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e4783-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e4783-122">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e4783-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e4783-123">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e4783-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e4783-124">Последняя команда задает свойства виртуальной машины в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e4783-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="e4783-125">Пример 3: Настройка свойств виртуальной машины из специального пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="e4783-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="e4783-126">Первая команда получает группу доступности с именем AvailablitySet13 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e4783-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="e4783-127">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e4783-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e4783-128">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e4783-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="e4783-129">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="e4783-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="e4783-130">Последняя команда задает свойства виртуальной машины в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e4783-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="e4783-131">Пример 4: Настройка параметров шифрования дисков на диске операционной системы виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="e4783-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="e4783-132">В этом примере устанавливаются параметры шифрования дисков на диске операционной системы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e4783-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="e4783-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4783-133">PARAMETERS</span></span>

### <span data-ttu-id="e4783-134">-Caching</span><span class="sxs-lookup"><span data-stu-id="e4783-134">-Caching</span></span>
<span data-ttu-id="e4783-135">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e4783-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="e4783-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e4783-136">Valid values are:</span></span> 
- <span data-ttu-id="e4783-137">Чтения</span><span class="sxs-lookup"><span data-stu-id="e4783-137">ReadOnly</span></span>
- <span data-ttu-id="e4783-138">ReadWrite по умолчанию используется значение ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="e4783-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="e4783-139">Изменение значения Caching приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e4783-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="e4783-140">Этот параметр влияет на производительность диска.</span><span class="sxs-lookup"><span data-stu-id="e4783-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e4783-141">-CreateOption</span></span>
<span data-ttu-id="e4783-142">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа либо добавляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="e4783-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="e4783-143">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="e4783-143">Valid values are:</span></span> 
- <span data-ttu-id="e4783-144">Подключает.</span><span class="sxs-lookup"><span data-stu-id="e4783-144">Attach.</span></span>
<span data-ttu-id="e4783-145">Укажите этот параметр, чтобы создать виртуальную машину на основе специализированного диска.</span><span class="sxs-lookup"><span data-stu-id="e4783-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="e4783-146">Если вы задаете этот параметр, не указывайте параметр *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="e4783-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="e4783-147">Вместо этого используйте командлет Set-AzVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="e4783-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="e4783-148">Кроме того, вы должны использовать параметры *Windows* или *Linux* , чтобы сообщить платформе Azure тип операционной системы на виртуальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="e4783-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="e4783-149">Параметр *VhdUri* достаточно для того, чтобы сообщить платформе Azure расположение диска для присоединения.</span><span class="sxs-lookup"><span data-stu-id="e4783-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="e4783-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="e4783-150">FromImage.</span></span>
<span data-ttu-id="e4783-151">Укажите этот параметр, чтобы создать виртуальную машину на основе образа платформы или обобщенного пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="e4783-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="e4783-152">В случае обобщенного образа пользователя также необходимо указать параметр *SourceImageUri* и параметры *Windows* или *Linux* , чтобы сообщить платформе Azure расположение и тип диска операционной системы, а не использовать командлет **Set-AzVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="e4783-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="e4783-153">В случае с изображением платформы достаточно параметра *VhdUri* .</span><span class="sxs-lookup"><span data-stu-id="e4783-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="e4783-154">Очистку.</span><span class="sxs-lookup"><span data-stu-id="e4783-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4783-155">-DefaultProfile</span></span>
<span data-ttu-id="e4783-156">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4783-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4783-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="e4783-157">-DiffDiskSetting</span></span>
<span data-ttu-id="e4783-158">Задает параметры разностного диска для диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e4783-158">Specifies the differencing disk settings for operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e4783-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="e4783-160">Указывает расположение ключа шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="e4783-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e4783-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="e4783-162">Указывает ИД ресурса для хранилища ключей, содержащего ключ шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="e4783-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-163">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e4783-163">-DiskSizeInGB</span></span>
<span data-ttu-id="e4783-164">Задает размер (в ГБ) диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e4783-164">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-165">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e4783-165">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e4783-166">Задает расположение ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="e4783-166">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-167">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e4783-167">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="e4783-168">Указывает ИД ресурса для хранилища ключей, содержащего ключ шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="e4783-168">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-169">-Linux</span><span class="sxs-lookup"><span data-stu-id="e4783-169">-Linux</span></span>
<span data-ttu-id="e4783-170">Указывает, что операционная система на пользовательском изображении — Linux.</span><span class="sxs-lookup"><span data-stu-id="e4783-170">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="e4783-171">Укажите этот параметр для развертывания виртуальной машины на основе пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="e4783-171">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e4783-172">-ManagedDiskId</span></span>
<span data-ttu-id="e4783-173">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="e4783-173">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="e4783-174">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4783-174">-Name</span></span>
<span data-ttu-id="e4783-175">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e4783-175">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="e4783-176">-SourceImageUri</span></span>
<span data-ttu-id="e4783-177">Задает универсальный код ресурса (URI) для сценариев пользователей в формате VHD.</span><span class="sxs-lookup"><span data-stu-id="e4783-177">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e4783-178">-StorageAccountType</span></span>
<span data-ttu-id="e4783-179">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="e4783-179">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="e4783-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="e4783-180">-VhdUri</span></span>
<span data-ttu-id="e4783-181">Задает универсальный код ресурса (URI) виртуального жесткого диска (VHD).</span><span class="sxs-lookup"><span data-stu-id="e4783-181">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="e4783-182">Для виртуальной машины на основе изображений этот параметр указывает VHD-файл, который будет создан при указании образа платформы или пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="e4783-182">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="e4783-183">Это расположение, из которого копируется большой двоичный объект (BLOB), чтобы запустить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e4783-183">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="e4783-184">Для сценария загрузки виртуальной машины на диске этот параметр указывает VHD-файл, который виртуальная машина использует для запуска.</span><span class="sxs-lookup"><span data-stu-id="e4783-184">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-185">-VM</span><span class="sxs-lookup"><span data-stu-id="e4783-185">-VM</span></span>
<span data-ttu-id="e4783-186">Указывает локальный объект виртуальной машины, на котором нужно задать свойства диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e4783-186">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="e4783-187">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="e4783-187">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-188">-Windows</span><span class="sxs-lookup"><span data-stu-id="e4783-188">-Windows</span></span>
<span data-ttu-id="e4783-189">Указывает, что операционная система на пользовательском изображении — Windows.</span><span class="sxs-lookup"><span data-stu-id="e4783-189">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4783-190">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e4783-190">-WriteAccelerator</span></span>
<span data-ttu-id="e4783-191">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e4783-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="e4783-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4783-192">CommonParameters</span></span>
<span data-ttu-id="e4783-193">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4783-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4783-194">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4783-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4783-195">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4783-195">INPUTS</span></span>

### <span data-ttu-id="e4783-196">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e4783-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e4783-197">System. String</span><span class="sxs-lookup"><span data-stu-id="e4783-197">System.String</span></span>

## <span data-ttu-id="e4783-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4783-198">OUTPUTS</span></span>

### <span data-ttu-id="e4783-199">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e4783-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e4783-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4783-200">NOTES</span></span>

## <span data-ttu-id="e4783-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4783-201">RELATED LINKS</span></span>

[<span data-ttu-id="e4783-202">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e4783-202">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e4783-203">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e4783-203">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="e4783-204">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e4783-204">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


