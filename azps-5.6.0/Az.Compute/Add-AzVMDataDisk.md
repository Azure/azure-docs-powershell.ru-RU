---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 685a1768dac652b3981bd081a2f8b29997c08639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981160"
---
# <span data-ttu-id="4bec4-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4bec4-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="4bec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bec4-102">SYNOPSIS</span></span>
<span data-ttu-id="4bec4-103">Добавляет диск данных на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="4bec4-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="4bec4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4bec4-104">SYNTAX</span></span>

### <span data-ttu-id="4bec4-105">VmNormalDiskParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4bec4-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bec4-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4bec4-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bec4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bec4-107">DESCRIPTION</span></span>
<span data-ttu-id="4bec4-108">**Cmdlet Add-AzVMDataDisk** добавляет диск данных на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="4bec4-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="4bec4-109">Диск данных можно добавить при создании виртуальной машины или на существующую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="4bec4-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="4bec4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4bec4-110">EXAMPLES</span></span>

### <span data-ttu-id="4bec4-111">Пример 1. Добавление дисков данных на новую виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="4bec4-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="4bec4-112">Первая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="4bec4-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4bec4-113">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4bec4-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4bec4-114">Следующие три команды назначают пути из трех дисков данных переменным $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="4bec4-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="4bec4-115">Этот подход подходит только для учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="4bec4-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="4bec4-116">Последние три команды добавляют диск данных на виртуальную машину, храняную в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4bec4-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4bec4-117">Команда определяет имя и расположение диска, а также другие его свойства.</span><span class="sxs-lookup"><span data-stu-id="4bec4-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="4bec4-118">URI каждого диска хранится в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="4bec4-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="4bec4-119">Пример 2. Добавление диска данных в существующую виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="4bec4-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="4bec4-120">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью [командлета Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="4bec4-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="4bec4-121">Эта команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4bec4-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4bec4-122">Вторая команда добавляет диск данных на виртуальную машину, которая хранится в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4bec4-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4bec4-123">Последняя команда обновляет состояние виртуальной машины, которая хранится в $VirtualMachine ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4bec4-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="4bec4-124">Пример 3. Добавление диска данных на новую виртуальную машину из изображения пользователя</span><span class="sxs-lookup"><span data-stu-id="4bec4-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="4bec4-125">Первая команда создает объект виртуальной машины и сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="4bec4-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4bec4-126">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4bec4-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4bec4-127">Следующие две команды назначают пути к изображению данных и дискам данных переменным $DataImageUri и $DataDiskUri данных соответственно.</span><span class="sxs-lookup"><span data-stu-id="4bec4-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="4bec4-128">Этот подход используется для повышения учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="4bec4-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="4bec4-129">Полученные команды добавляют диск данных на виртуальную машину, которая хранится в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4bec4-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4bec4-130">Команда определяет имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="4bec4-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="4bec4-131">Пример 4. Добавление дисков данных на новую виртуальную машину со специализированного изображения пользователя</span><span class="sxs-lookup"><span data-stu-id="4bec4-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="4bec4-132">Первая команда создает объект виртуальной машины и сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="4bec4-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4bec4-133">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4bec4-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4bec4-134">Следующая команда назначает пути диска данных переменной $DataDiskUri данных.</span><span class="sxs-lookup"><span data-stu-id="4bec4-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="4bec4-135">Этот подход используется для повышения учитаемости следующих команд:</span><span class="sxs-lookup"><span data-stu-id="4bec4-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="4bec4-136">Конечная команда добавляет диск данных на виртуальную машину, которая хранится в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4bec4-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4bec4-137">Команда определяет имя и расположение диска, а также другие его свойства.</span><span class="sxs-lookup"><span data-stu-id="4bec4-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="4bec4-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bec4-138">PARAMETERS</span></span>

### <span data-ttu-id="4bec4-139">-Кэшинг</span><span class="sxs-lookup"><span data-stu-id="4bec4-139">-Caching</span></span>
<span data-ttu-id="4bec4-140">Определяет режим кэшации диска.</span><span class="sxs-lookup"><span data-stu-id="4bec4-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="4bec4-141">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="4bec4-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4bec4-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4bec4-142">ReadOnly</span></span>
- <span data-ttu-id="4bec4-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4bec4-143">ReadWrite</span></span>
- <span data-ttu-id="4bec4-144">По умолчанию значение "ReadWrite" отсутствует.</span><span class="sxs-lookup"><span data-stu-id="4bec4-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="4bec4-145">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4bec4-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="4bec4-146">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="4bec4-146">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="4bec4-147">-CreateOption</span></span>
<span data-ttu-id="4bec4-148">Указывает, создает ли этот cmdlet диск в виртуальной машине из платформы или изображения пользователя, создает пустой диск или влог существующий диск.</span><span class="sxs-lookup"><span data-stu-id="4bec4-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="4bec4-149">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="4bec4-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4bec4-150">Вложите.</span><span class="sxs-lookup"><span data-stu-id="4bec4-150">Attach.</span></span>
<span data-ttu-id="4bec4-151">Укажите этот параметр, чтобы создать виртуальную машину на специализированном диске.</span><span class="sxs-lookup"><span data-stu-id="4bec4-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="4bec4-152">При указании этого параметра не укажите параметр *SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="4bec4-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="4bec4-153">Для того чтобы указать платформе Azure расположение виртуального жесткого диска (VHD), который нужно прикрепить в качестве диска данных к виртуальной машине, достаточно *VhdUri.*</span><span class="sxs-lookup"><span data-stu-id="4bec4-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="4bec4-154">"Пустая".</span><span class="sxs-lookup"><span data-stu-id="4bec4-154">Empty.</span></span>
<span data-ttu-id="4bec4-155">Укажите это, чтобы создать пустой диск данных.</span><span class="sxs-lookup"><span data-stu-id="4bec4-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="4bec4-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="4bec4-156">FromImage.</span></span>
<span data-ttu-id="4bec4-157">Укажите этот параметр, чтобы создать виртуальную машину на общем изображении или диске.</span><span class="sxs-lookup"><span data-stu-id="4bec4-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="4bec4-158">При указании этого параметра необходимо указать параметр *SourceImageUri,* чтобы указать платформе Azure расположение VHD для вложения в качестве диска данных.</span><span class="sxs-lookup"><span data-stu-id="4bec4-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="4bec4-159">Параметр *VhdUri* используется в качестве расположения, определяющих, где будет храниться VHD-диск данных при его использовании виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="4bec4-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bec4-160">-DefaultProfile</span></span>
<span data-ttu-id="4bec4-161">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bec4-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bec4-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="4bec4-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="4bec4-163">Определяет код ресурса для набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="4bec4-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="4bec4-164">Эта проверка может быть задана только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="4bec4-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="4bec4-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4bec4-165">-DiskSizeInGB</span></span>
<span data-ttu-id="4bec4-166">Определяет размер в гигабайтах пустого диска, который нужно прикрепить к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4bec4-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-167">-Lun</span><span class="sxs-lookup"><span data-stu-id="4bec4-167">-Lun</span></span>
<span data-ttu-id="4bec4-168">Определяет логический номер единицы (LUN) для диска данных.</span><span class="sxs-lookup"><span data-stu-id="4bec4-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="4bec4-169">-ManagedDiskId</span></span>
<span data-ttu-id="4bec4-170">Определяет ИД управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="4bec4-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-171">-Name</span><span class="sxs-lookup"><span data-stu-id="4bec4-171">-Name</span></span>
<span data-ttu-id="4bec4-172">Имя добавляемого диска данных.</span><span class="sxs-lookup"><span data-stu-id="4bec4-172">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="4bec4-173">-SourceImageUri</span></span>
<span data-ttu-id="4bec4-174">Определяет исходный URI диска, который вложен в этот проектлет.</span><span class="sxs-lookup"><span data-stu-id="4bec4-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4bec4-175">-StorageAccountType</span></span>
<span data-ttu-id="4bec4-176">Определяет тип учетной записи хранения управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="4bec4-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="4bec4-177">-VhdUri</span></span>
<span data-ttu-id="4bec4-178">URI указывает URI для виртуального жесткого диска (VHD), который создается при создании изображения платформы или пользователя.</span><span class="sxs-lookup"><span data-stu-id="4bec4-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="4bec4-179">Этот cmdlet копирует изображение двоичного большого объекта (BLOB-объекта) в это расположение.</span><span class="sxs-lookup"><span data-stu-id="4bec4-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="4bec4-180">Это расположение, из которого нужно запустить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="4bec4-180">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-181">-VM</span><span class="sxs-lookup"><span data-stu-id="4bec4-181">-VM</span></span>
<span data-ttu-id="4bec4-182">Определяет объект локальной виртуальной машины, к которому нужно добавить диск данных.</span><span class="sxs-lookup"><span data-stu-id="4bec4-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="4bec4-183">Для получения объекта виртуальной машины можно использовать **cmdlet Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="4bec4-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="4bec4-184">Для создания объекта виртуальной машины можно использовать **cmdlet New-AzVMConfig.**</span><span class="sxs-lookup"><span data-stu-id="4bec4-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="4bec4-185">-WriteAccelerator</span></span>
<span data-ttu-id="4bec4-186">Указывает, следует ли включить или отключить WriteAccelerator на диске управляемых данных.</span><span class="sxs-lookup"><span data-stu-id="4bec4-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bec4-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bec4-187">CommonParameters</span></span>
<span data-ttu-id="4bec4-188">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bec4-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bec4-189">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bec4-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bec4-190">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bec4-190">INPUTS</span></span>

### <span data-ttu-id="4bec4-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="4bec4-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4bec4-192">System.String</span><span class="sxs-lookup"><span data-stu-id="4bec4-192">System.String</span></span>

### <span data-ttu-id="4bec4-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="4bec4-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="4bec4-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4bec4-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4bec4-195">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4bec4-195">OUTPUTS</span></span>

### <span data-ttu-id="4bec4-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="4bec4-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4bec4-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4bec4-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4bec4-198">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4bec4-198">NOTES</span></span>

## <span data-ttu-id="4bec4-199">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bec4-199">RELATED LINKS</span></span>

[<span data-ttu-id="4bec4-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4bec4-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="4bec4-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4bec4-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4bec4-202">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4bec4-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
