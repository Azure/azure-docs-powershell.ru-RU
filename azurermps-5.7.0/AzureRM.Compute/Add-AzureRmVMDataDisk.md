---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 7566c1ef5c8e9cbf2134bc18b3aecf37d9f88bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561923"
---
# <span data-ttu-id="ed926-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ed926-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="ed926-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed926-102">SYNOPSIS</span></span>
<span data-ttu-id="ed926-103">Добавляет диск с данными на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ed926-103">Adds a data disk to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed926-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed926-104">SYNTAX</span></span>

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed926-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed926-105">DESCRIPTION</span></span>
<span data-ttu-id="ed926-106">Командлет **Add-AzureRmVMDataDisk** добавляет диск с данными на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ed926-106">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="ed926-107">Вы можете добавить диск с данными при создании виртуальной машины или добавить диск с данными на существующую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="ed926-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="ed926-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed926-108">EXAMPLES</span></span>

### <span data-ttu-id="ed926-109">Пример 1: Добавление дисков с данными на новую виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="ed926-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="ed926-110">В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ed926-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ed926-111">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ed926-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="ed926-112">Следующие три команды назначают пути к трем дискам с данными в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="ed926-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="ed926-113">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="ed926-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="ed926-114">Последние три команды добавляют диск с данными на виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ed926-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ed926-115">Команда задает имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="ed926-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="ed926-116">Универсальный код ресурса (URI) каждого диска хранится в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="ed926-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="ed926-117">Пример 2: Добавление диска данных к существующей виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="ed926-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="ed926-118">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="ed926-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="ed926-119">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ed926-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ed926-120">Вторая команда добавляет диск с данными для виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ed926-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="ed926-121">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ed926-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="ed926-122">Пример 3: Добавление диска с данными на новую виртуальную машину из обобщенного пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="ed926-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="ed926-123">Первая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ed926-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ed926-124">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ed926-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="ed926-125">Следующие две команды назначают пути для изображения данных и дисков данных в $DataImageUri и $DataDiskUri переменные соответственно.</span><span class="sxs-lookup"><span data-stu-id="ed926-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="ed926-126">Этот подход используется для повышения удобочитаемости следующих команд.</span><span class="sxs-lookup"><span data-stu-id="ed926-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="ed926-127">Последние команды добавляют к виртуальной машине диск с данными, хранящийся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ed926-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ed926-128">Команда задает имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="ed926-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="ed926-129">Пример 4: Добавление дисков с данными на новую виртуальную машину из специализированного пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="ed926-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="ed926-130">Первая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ed926-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ed926-131">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ed926-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="ed926-132">Следующие команды назначают пути к диску данных переменной $DataDiskUri.</span><span class="sxs-lookup"><span data-stu-id="ed926-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="ed926-133">Этот подход используется для повышения удобочитаемости следующих команд.</span><span class="sxs-lookup"><span data-stu-id="ed926-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="ed926-134">В последней команде вы можете добавить диск с данными на виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ed926-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ed926-135">Команда задает имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="ed926-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="ed926-136">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed926-136">PARAMETERS</span></span>

### <span data-ttu-id="ed926-137">-Caching</span><span class="sxs-lookup"><span data-stu-id="ed926-137">-Caching</span></span>
<span data-ttu-id="ed926-138">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="ed926-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="ed926-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ed926-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed926-140">Чтения</span><span class="sxs-lookup"><span data-stu-id="ed926-140">ReadOnly</span></span>
- <span data-ttu-id="ed926-141">Операцию</span><span class="sxs-lookup"><span data-stu-id="ed926-141">ReadWrite</span></span>
- <span data-ttu-id="ed926-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed926-142">None</span></span>

<span data-ttu-id="ed926-143">Значением по умолчанию является ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ed926-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="ed926-144">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ed926-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="ed926-145">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="ed926-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="ed926-146">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="ed926-146">-CreateOption</span></span>
<span data-ttu-id="ed926-147">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="ed926-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="ed926-148">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ed926-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed926-149">Подключает.</span><span class="sxs-lookup"><span data-stu-id="ed926-149">Attach.</span></span>
<span data-ttu-id="ed926-150">Укажите этот параметр, чтобы создать виртуальную машину на основе специализированного диска.</span><span class="sxs-lookup"><span data-stu-id="ed926-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="ed926-151">Если вы задаете этот параметр, не указывайте параметр *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="ed926-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="ed926-152">*VhdUri* — это все, что необходимо для того, чтобы указать платформе Azure расположение виртуального жесткого диска (VHD) для присоединения в качестве диска данных виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ed926-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="ed926-153">Очистку.</span><span class="sxs-lookup"><span data-stu-id="ed926-153">Empty.</span></span>
<span data-ttu-id="ed926-154">Укажите этот объект, чтобы создать пустой диск с данными.</span><span class="sxs-lookup"><span data-stu-id="ed926-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="ed926-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="ed926-155">FromImage.</span></span>
<span data-ttu-id="ed926-156">Укажите этот параметр, чтобы создать виртуальную машину на основе обобщенного образа или диска.</span><span class="sxs-lookup"><span data-stu-id="ed926-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="ed926-157">При указании этого параметра необходимо указать параметр *SourceImageUri* , чтобы сообщить платформе Azure о том, что расположение виртуального жесткого диска будет прикрепляться в качестве диска данных.</span><span class="sxs-lookup"><span data-stu-id="ed926-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="ed926-158">Параметр *VhdUri* используется в качестве расположения, которое определяет, где будет храниться диск данных, когда он используется виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="ed926-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-159">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ed926-159">-DiskSizeInGB</span></span>
<span data-ttu-id="ed926-160">Задает размер пустого диска (в гигабайтах), который нужно прикрепить к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ed926-160">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-161">-LUN</span><span class="sxs-lookup"><span data-stu-id="ed926-161">-Lun</span></span>
<span data-ttu-id="ed926-162">Задает логический номер устройства (LUN) для диска с данными.</span><span class="sxs-lookup"><span data-stu-id="ed926-162">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-163">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="ed926-163">-ManagedDiskId</span></span>
<span data-ttu-id="ed926-164">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="ed926-164">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-165">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed926-165">-Name</span></span>
<span data-ttu-id="ed926-166">Указывает имя диска данных, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="ed926-166">Specifies the name of the data disk to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-167">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="ed926-167">-SourceImageUri</span></span>
<span data-ttu-id="ed926-168">Указывает URI источника диска, к которому прикрепляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ed926-168">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-169">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ed926-169">-StorageAccountType</span></span>
<span data-ttu-id="ed926-170">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="ed926-170">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-171">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="ed926-171">-VhdUri</span></span>
<span data-ttu-id="ed926-172">Задает универсальный код ресурса (URI) для файла виртуального жесткого диска (VHD), который будет создан при использовании образа платформы или пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="ed926-172">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="ed926-173">Этот командлет копирует большой двоичный объект изображения (BLOB) в это расположение.</span><span class="sxs-lookup"><span data-stu-id="ed926-173">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="ed926-174">Это место, с которого запускается виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="ed926-174">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed926-175">-VM</span><span class="sxs-lookup"><span data-stu-id="ed926-175">-VM</span></span>
<span data-ttu-id="ed926-176">Указывает локальный объект виртуальной машины, к которому нужно добавить диск с данными.</span><span class="sxs-lookup"><span data-stu-id="ed926-176">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="ed926-177">Вы можете использовать командлет **Get-AzureRmVM** для получения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ed926-177">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="ed926-178">Вы можете использовать командлет **New-AzureRmVMConfig** для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ed926-178">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="ed926-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed926-179">CommonParameters</span></span>
<span data-ttu-id="ed926-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed926-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed926-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed926-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed926-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed926-182">INPUTS</span></span>

### <span data-ttu-id="ed926-183">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed926-183">None</span></span>
<span data-ttu-id="ed926-184">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ed926-184">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed926-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed926-185">OUTPUTS</span></span>

## <span data-ttu-id="ed926-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed926-186">NOTES</span></span>

## <span data-ttu-id="ed926-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed926-187">RELATED LINKS</span></span>

[<span data-ttu-id="ed926-188">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ed926-188">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="ed926-189">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ed926-189">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ed926-190">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="ed926-190">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
