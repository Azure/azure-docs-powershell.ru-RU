---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 79d8852fb3827e7856610d79ea7fb5f0a17543c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727520"
---
# <span data-ttu-id="fb3af-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fb3af-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="fb3af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb3af-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3af-103">Добавляет диск с данными на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="fb3af-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="fb3af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb3af-104">SYNTAX</span></span>

### <span data-ttu-id="fb3af-105">VmNormalDiskParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb3af-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb3af-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="fb3af-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb3af-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb3af-107">DESCRIPTION</span></span>
<span data-ttu-id="fb3af-108">Командлет **Add-AzVMDataDisk** добавляет диск с данными на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="fb3af-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="fb3af-109">Вы можете добавить диск с данными при создании виртуальной машины или добавить диск с данными на существующую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="fb3af-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="fb3af-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb3af-110">EXAMPLES</span></span>

### <span data-ttu-id="fb3af-111">Пример 1: Добавление дисков с данными на новую виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="fb3af-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="fb3af-112">В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fb3af-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fb3af-113">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fb3af-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="fb3af-114">Следующие три команды назначают пути к трем дискам с данными в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="fb3af-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="fb3af-115">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="fb3af-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="fb3af-116">Последние три команды добавляют диск с данными на виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fb3af-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="fb3af-117">Команда задает имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="fb3af-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="fb3af-118">Универсальный код ресурса (URI) каждого диска хранится в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="fb3af-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="fb3af-119">Пример 2: Добавление диска данных к существующей виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="fb3af-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="fb3af-120">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="fb3af-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="fb3af-121">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fb3af-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fb3af-122">Вторая команда добавляет диск с данными для виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fb3af-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="fb3af-123">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fb3af-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="fb3af-124">Пример 3: Добавление диска с данными на новую виртуальную машину из обобщенного пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="fb3af-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="fb3af-125">Первая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fb3af-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fb3af-126">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fb3af-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="fb3af-127">Следующие две команды назначают пути для изображения данных и дисков данных в $DataImageUri и $DataDiskUri переменные соответственно.</span><span class="sxs-lookup"><span data-stu-id="fb3af-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="fb3af-128">Этот подход используется для повышения удобочитаемости следующих команд.</span><span class="sxs-lookup"><span data-stu-id="fb3af-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="fb3af-129">Последние команды добавляют к виртуальной машине диск с данными, хранящийся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fb3af-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="fb3af-130">Команда задает имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="fb3af-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="fb3af-131">Пример 4: Добавление дисков с данными на новую виртуальную машину из специализированного пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="fb3af-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="fb3af-132">Первая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fb3af-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fb3af-133">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fb3af-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="fb3af-134">Следующие команды назначают пути к диску данных переменной $DataDiskUri.</span><span class="sxs-lookup"><span data-stu-id="fb3af-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="fb3af-135">Этот подход используется для повышения удобочитаемости следующих команд.</span><span class="sxs-lookup"><span data-stu-id="fb3af-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="fb3af-136">В последней команде вы можете добавить диск с данными на виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fb3af-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="fb3af-137">Команда задает имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="fb3af-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="fb3af-138">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb3af-138">PARAMETERS</span></span>

### <span data-ttu-id="fb3af-139">-Caching</span><span class="sxs-lookup"><span data-stu-id="fb3af-139">-Caching</span></span>
<span data-ttu-id="fb3af-140">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="fb3af-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="fb3af-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fb3af-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb3af-142">Чтения</span><span class="sxs-lookup"><span data-stu-id="fb3af-142">ReadOnly</span></span>
- <span data-ttu-id="fb3af-143">Операцию</span><span class="sxs-lookup"><span data-stu-id="fb3af-143">ReadWrite</span></span>
- <span data-ttu-id="fb3af-144">Отсутствует значение по умолчанию: ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="fb3af-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="fb3af-145">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fb3af-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="fb3af-146">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="fb3af-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="fb3af-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="fb3af-147">-CreateOption</span></span>
<span data-ttu-id="fb3af-148">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="fb3af-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="fb3af-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fb3af-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fb3af-150">Подключает.</span><span class="sxs-lookup"><span data-stu-id="fb3af-150">Attach.</span></span>
<span data-ttu-id="fb3af-151">Укажите этот параметр, чтобы создать виртуальную машину на основе специализированного диска.</span><span class="sxs-lookup"><span data-stu-id="fb3af-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="fb3af-152">Если вы задаете этот параметр, не указывайте параметр *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="fb3af-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="fb3af-153">*VhdUri* — это все, что необходимо для того, чтобы указать платформе Azure расположение виртуального жесткого диска (VHD) для присоединения в качестве диска данных виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fb3af-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="fb3af-154">Очистку.</span><span class="sxs-lookup"><span data-stu-id="fb3af-154">Empty.</span></span>
<span data-ttu-id="fb3af-155">Укажите этот объект, чтобы создать пустой диск с данными.</span><span class="sxs-lookup"><span data-stu-id="fb3af-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="fb3af-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="fb3af-156">FromImage.</span></span>
<span data-ttu-id="fb3af-157">Укажите этот параметр, чтобы создать виртуальную машину на основе обобщенного образа или диска.</span><span class="sxs-lookup"><span data-stu-id="fb3af-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="fb3af-158">При указании этого параметра необходимо указать параметр *SourceImageUri* , чтобы сообщить платформе Azure о том, что расположение виртуального жесткого диска будет прикрепляться в качестве диска данных.</span><span class="sxs-lookup"><span data-stu-id="fb3af-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="fb3af-159">Параметр *VhdUri* используется в качестве расположения, которое определяет, где будет храниться диск данных, когда он используется виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="fb3af-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="fb3af-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3af-160">-DefaultProfile</span></span>
<span data-ttu-id="fb3af-161">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb3af-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb3af-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="fb3af-162">-DiskSizeInGB</span></span>
<span data-ttu-id="fb3af-163">Задает размер пустого диска (в гигабайтах), который нужно прикрепить к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fb3af-163">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="fb3af-164">-LUN</span><span class="sxs-lookup"><span data-stu-id="fb3af-164">-Lun</span></span>
<span data-ttu-id="fb3af-165">Задает логический номер устройства (LUN) для диска с данными.</span><span class="sxs-lookup"><span data-stu-id="fb3af-165">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="fb3af-166">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="fb3af-166">-ManagedDiskId</span></span>
<span data-ttu-id="fb3af-167">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="fb3af-167">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="fb3af-168">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb3af-168">-Name</span></span>
<span data-ttu-id="fb3af-169">Указывает имя диска данных, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="fb3af-169">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="fb3af-170">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="fb3af-170">-SourceImageUri</span></span>
<span data-ttu-id="fb3af-171">Указывает URI источника диска, к которому прикрепляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fb3af-171">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="fb3af-172">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="fb3af-172">-StorageAccountType</span></span>
<span data-ttu-id="fb3af-173">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="fb3af-173">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="fb3af-174">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="fb3af-174">-VhdUri</span></span>
<span data-ttu-id="fb3af-175">Задает универсальный код ресурса (URI) для файла виртуального жесткого диска (VHD), который будет создан при использовании образа платформы или пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="fb3af-175">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="fb3af-176">Этот командлет копирует большой двоичный объект изображения (BLOB) в это расположение.</span><span class="sxs-lookup"><span data-stu-id="fb3af-176">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="fb3af-177">Это место, с которого запускается виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="fb3af-177">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="fb3af-178">-VM</span><span class="sxs-lookup"><span data-stu-id="fb3af-178">-VM</span></span>
<span data-ttu-id="fb3af-179">Указывает локальный объект виртуальной машины, к которому нужно добавить диск с данными.</span><span class="sxs-lookup"><span data-stu-id="fb3af-179">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="fb3af-180">Вы можете использовать командлет **Get-AzVM** для получения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fb3af-180">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="fb3af-181">Вы можете использовать командлет **New-AzVMConfig** для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fb3af-181">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="fb3af-182">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="fb3af-182">-WriteAccelerator</span></span>
<span data-ttu-id="fb3af-183">Указывает, следует ли включить или отключить WriteAccelerator на диске с управляемыми данными.</span><span class="sxs-lookup"><span data-stu-id="fb3af-183">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="fb3af-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3af-184">CommonParameters</span></span>
<span data-ttu-id="fb3af-185">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb3af-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3af-186">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb3af-186">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3af-187">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb3af-187">INPUTS</span></span>

### <span data-ttu-id="fb3af-188">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fb3af-188">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fb3af-189">System. String</span><span class="sxs-lookup"><span data-stu-id="fb3af-189">System.String</span></span>

### <span data-ttu-id="fb3af-190">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="fb3af-190">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="fb3af-191">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb3af-191">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fb3af-192">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb3af-192">OUTPUTS</span></span>

### <span data-ttu-id="fb3af-193">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fb3af-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fb3af-194">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fb3af-194">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="fb3af-195">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb3af-195">NOTES</span></span>

## <span data-ttu-id="fb3af-196">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb3af-196">RELATED LINKS</span></span>

[<span data-ttu-id="fb3af-197">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fb3af-197">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="fb3af-198">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fb3af-198">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="fb3af-199">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="fb3af-199">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
