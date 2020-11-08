---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074625"
---
# <span data-ttu-id="2c6ee-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="2c6ee-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="2c6ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6ee-103">Задает свойства диска операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="2c6ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c6ee-104">SYNTAX</span></span>

### <span data-ttu-id="2c6ee-105">DefaultParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c6ee-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c6ee-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="2c6ee-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c6ee-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c6ee-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c6ee-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="2c6ee-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c6ee-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c6ee-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c6ee-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c6ee-110">DESCRIPTION</span></span>
<span data-ttu-id="2c6ee-111">Командлет **Set-AzVMOSDisk** задает свойства диска операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="2c6ee-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c6ee-112">EXAMPLES</span></span>

### <span data-ttu-id="2c6ee-113">Пример 1: Настройка свойств виртуальной машины из образа платформы</span><span class="sxs-lookup"><span data-stu-id="2c6ee-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="2c6ee-114">Первая команда получает группу доступности с именем AvailabilitySet13 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="2c6ee-115">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2c6ee-116">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2c6ee-117">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="2c6ee-118">Последняя команда задает свойства виртуальной машины в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="2c6ee-119">Пример 2: Настройка свойств виртуальной машины из обобщенного пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="2c6ee-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="2c6ee-120">Первая команда получает группу доступности с именем AvailabilitySet13 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="2c6ee-121">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2c6ee-122">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2c6ee-123">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="2c6ee-124">Последняя команда задает свойства виртуальной машины в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="2c6ee-125">Пример 3: Настройка свойств виртуальной машины из специального пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="2c6ee-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="2c6ee-126">Первая команда получает группу доступности с именем AvailabilitySet13 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="2c6ee-127">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2c6ee-128">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="2c6ee-129">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="2c6ee-130">Последняя команда задает свойства виртуальной машины в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="2c6ee-131">Пример 4: Настройка параметров шифрования дисков на диске операционной системы виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="2c6ee-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="2c6ee-132">В этом примере устанавливаются параметры шифрования дисков на диске операционной системы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="2c6ee-133">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c6ee-133">PARAMETERS</span></span>

### <span data-ttu-id="2c6ee-134">-Caching</span><span class="sxs-lookup"><span data-stu-id="2c6ee-134">-Caching</span></span>
<span data-ttu-id="2c6ee-135">Задает режим кэширования диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="2c6ee-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2c6ee-136">Valid values are:</span></span> 
- <span data-ttu-id="2c6ee-137">Чтения</span><span class="sxs-lookup"><span data-stu-id="2c6ee-137">ReadOnly</span></span>
- <span data-ttu-id="2c6ee-138">ReadWrite по умолчанию используется значение ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="2c6ee-139">Изменение значения Caching приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="2c6ee-140">Этот параметр влияет на производительность диска.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="2c6ee-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="2c6ee-141">-CreateOption</span></span>
<span data-ttu-id="2c6ee-142">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа либо добавляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="2c6ee-143">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2c6ee-143">Valid values are:</span></span> 
- <span data-ttu-id="2c6ee-144">Подключает.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-144">Attach.</span></span>
<span data-ttu-id="2c6ee-145">Укажите этот параметр, чтобы создать виртуальную машину на основе специализированного диска.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="2c6ee-146">Если вы задаете этот параметр, не указывайте параметр *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="2c6ee-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="2c6ee-147">Вместо этого используйте командлет Set-AzVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="2c6ee-148">Кроме того, вы должны использовать параметры *Windows* или *Linux* , чтобы сообщить платформе Azure тип операционной системы на виртуальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="2c6ee-149">Параметр *VhdUri* достаточно для того, чтобы сообщить платформе Azure расположение диска для присоединения.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="2c6ee-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-150">FromImage.</span></span>
<span data-ttu-id="2c6ee-151">Укажите этот параметр, чтобы создать виртуальную машину на основе образа платформы или обобщенного пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="2c6ee-152">В случае обобщенного образа пользователя также необходимо указать параметр *SourceImageUri* и параметры *Windows* или *Linux* , чтобы сообщить платформе Azure расположение и тип диска операционной системы, а не использовать командлет **Set-AzVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="2c6ee-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="2c6ee-153">В случае с изображением платформы достаточно параметра *VhdUri* .</span><span class="sxs-lookup"><span data-stu-id="2c6ee-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="2c6ee-154">Очистку.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-154">Empty.</span></span>

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

### <span data-ttu-id="2c6ee-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6ee-155">-DefaultProfile</span></span>
<span data-ttu-id="2c6ee-156">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c6ee-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="2c6ee-157">-DiffDiskSetting</span></span>
<span data-ttu-id="2c6ee-158">Задает параметры разностного диска для диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="2c6ee-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="2c6ee-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="2c6ee-160">Указывает расположение ключа шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="2c6ee-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2c6ee-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="2c6ee-162">Указывает ИД ресурса для хранилища ключей, содержащего ключ шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="2c6ee-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="2c6ee-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="2c6ee-164">Указывает идентификатор ресурса набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="2c6ee-165">Это может быть указано только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="2c6ee-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="2c6ee-166">-DiskSizeInGB</span></span>
<span data-ttu-id="2c6ee-167">Задает размер (в ГБ) диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-167">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="2c6ee-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="2c6ee-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="2c6ee-169">Задает расположение ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-169">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="2c6ee-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2c6ee-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="2c6ee-171">Указывает ИД ресурса для хранилища ключей, содержащего ключ шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="2c6ee-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="2c6ee-172">-Linux</span></span>
<span data-ttu-id="2c6ee-173">Указывает, что операционная система на пользовательском изображении — Linux.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="2c6ee-174">Укажите этот параметр для развертывания виртуальной машины на основе пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-174">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="2c6ee-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="2c6ee-175">-ManagedDiskId</span></span>
<span data-ttu-id="2c6ee-176">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="2c6ee-177">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2c6ee-177">-Name</span></span>
<span data-ttu-id="2c6ee-178">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-178">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="2c6ee-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="2c6ee-179">-SourceImageUri</span></span>
<span data-ttu-id="2c6ee-180">Задает универсальный код ресурса (URI) для сценариев пользователей в формате VHD.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-180">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="2c6ee-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2c6ee-181">-StorageAccountType</span></span>
<span data-ttu-id="2c6ee-182">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="2c6ee-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="2c6ee-183">-VhdUri</span></span>
<span data-ttu-id="2c6ee-184">Задает универсальный код ресурса (URI) виртуального жесткого диска (VHD).</span><span class="sxs-lookup"><span data-stu-id="2c6ee-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="2c6ee-185">Для виртуальной машины на основе изображений этот параметр указывает VHD-файл, который будет создан при указании образа платформы или пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="2c6ee-186">Это расположение, из которого копируется большой двоичный объект (BLOB), чтобы запустить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="2c6ee-187">Для сценария загрузки виртуальной машины на диске этот параметр указывает VHD-файл, который виртуальная машина использует для запуска.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="2c6ee-188">-VM</span><span class="sxs-lookup"><span data-stu-id="2c6ee-188">-VM</span></span>
<span data-ttu-id="2c6ee-189">Указывает локальный объект виртуальной машины, на котором нужно задать свойства диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="2c6ee-190">Чтобы получить объект виртуальной машины, используйте командлет Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="2c6ee-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="2c6ee-191">-Windows</span></span>
<span data-ttu-id="2c6ee-192">Указывает, что операционная система на пользовательском изображении — Windows.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-192">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="2c6ee-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="2c6ee-193">-WriteAccelerator</span></span>
<span data-ttu-id="2c6ee-194">Указывает, следует ли включить или отключить WriteAccelerator на диске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="2c6ee-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6ee-195">CommonParameters</span></span>
<span data-ttu-id="2c6ee-196">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c6ee-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6ee-197">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c6ee-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6ee-198">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c6ee-198">INPUTS</span></span>

### <span data-ttu-id="2c6ee-199">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2c6ee-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="2c6ee-200">System. String</span><span class="sxs-lookup"><span data-stu-id="2c6ee-200">System.String</span></span>

## <span data-ttu-id="2c6ee-201">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c6ee-201">OUTPUTS</span></span>

### <span data-ttu-id="2c6ee-202">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2c6ee-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2c6ee-203">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c6ee-203">NOTES</span></span>

## <span data-ttu-id="2c6ee-204">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c6ee-204">RELATED LINKS</span></span>

[<span data-ttu-id="2c6ee-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2c6ee-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2c6ee-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2c6ee-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="2c6ee-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2c6ee-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


