---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073454"
---
# <span data-ttu-id="bc866-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="bc866-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="bc866-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc866-102">SYNOPSIS</span></span>
<span data-ttu-id="bc866-103">Добавляет диск с данными на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="bc866-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="bc866-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc866-104">SYNTAX</span></span>

### <span data-ttu-id="bc866-105">VmNormalDiskParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc866-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc866-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bc866-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc866-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc866-107">DESCRIPTION</span></span>
<span data-ttu-id="bc866-108">Командлет **Add-AzVMDataDisk** добавляет диск с данными на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="bc866-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="bc866-109">Вы можете добавить диск с данными при создании виртуальной машины или добавить диск с данными на существующую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="bc866-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="bc866-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc866-110">EXAMPLES</span></span>

### <span data-ttu-id="bc866-111">Пример 1: Добавление дисков с данными на новую виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="bc866-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="bc866-112">В первой команде создается объект виртуальной машины, который затем сохраняется в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bc866-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bc866-113">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bc866-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bc866-114">Следующие три команды назначают пути к трем дискам с данными в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="bc866-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="bc866-115">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="bc866-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="bc866-116">Последние три команды добавляют диск с данными на виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bc866-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="bc866-117">Команда задает имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="bc866-118">Универсальный код ресурса (URI) каждого диска хранится в $DataDiskVhdUri 01, $DataDiskVhdUri 02 и $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="bc866-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="bc866-119">Пример 2: Добавление диска данных к существующей виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="bc866-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="bc866-120">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="bc866-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="bc866-121">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bc866-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bc866-122">Вторая команда добавляет диск с данными для виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bc866-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="bc866-123">Последняя команда обновляет состояние виртуальной машины, сохраненной в $VirtualMachine в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bc866-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="bc866-124">Пример 3: Добавление диска с данными на новую виртуальную машину из обобщенного пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="bc866-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="bc866-125">Первая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bc866-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bc866-126">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bc866-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bc866-127">Следующие две команды назначают пути для изображения данных и дисков данных в $DataImageUri и $DataDiskUri переменные соответственно.</span><span class="sxs-lookup"><span data-stu-id="bc866-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="bc866-128">Этот подход используется для повышения удобочитаемости следующих команд.</span><span class="sxs-lookup"><span data-stu-id="bc866-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="bc866-129">Последние команды добавляют к виртуальной машине диск с данными, хранящийся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bc866-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="bc866-130">Команда задает имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="bc866-131">Пример 4: Добавление дисков с данными на новую виртуальную машину из специализированного пользовательского образа</span><span class="sxs-lookup"><span data-stu-id="bc866-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="bc866-132">Первая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bc866-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="bc866-133">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bc866-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="bc866-134">Следующие команды назначают пути к диску данных переменной $DataDiskUri.</span><span class="sxs-lookup"><span data-stu-id="bc866-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="bc866-135">Этот подход используется для повышения удобочитаемости следующих команд.</span><span class="sxs-lookup"><span data-stu-id="bc866-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="bc866-136">В последней команде вы можете добавить диск с данными на виртуальную машину, хранящуюся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="bc866-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="bc866-137">Команда задает имя и расположение диска, а также другие свойства диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="bc866-138">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc866-138">PARAMETERS</span></span>

### <span data-ttu-id="bc866-139">-Caching</span><span class="sxs-lookup"><span data-stu-id="bc866-139">-Caching</span></span>
<span data-ttu-id="bc866-140">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="bc866-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bc866-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc866-142">Чтения</span><span class="sxs-lookup"><span data-stu-id="bc866-142">ReadOnly</span></span>
- <span data-ttu-id="bc866-143">Операцию</span><span class="sxs-lookup"><span data-stu-id="bc866-143">ReadWrite</span></span>
- <span data-ttu-id="bc866-144">Отсутствует значение по умолчанию: ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="bc866-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="bc866-145">Изменение этого значения приводит к перезапуску виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc866-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="bc866-146">Этот параметр влияет на согласованность и производительность диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="bc866-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="bc866-147">-CreateOption</span></span>
<span data-ttu-id="bc866-148">Указывает, создает ли этот командлет диск на виртуальной машине из платформы или пользовательского образа, создает пустой диск или прикрепляет существующий диск.</span><span class="sxs-lookup"><span data-stu-id="bc866-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="bc866-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bc866-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc866-150">Подключает.</span><span class="sxs-lookup"><span data-stu-id="bc866-150">Attach.</span></span>
<span data-ttu-id="bc866-151">Укажите этот параметр, чтобы создать виртуальную машину на основе специализированного диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="bc866-152">Если вы задаете этот параметр, не указывайте параметр *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="bc866-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="bc866-153">*VhdUri* — это все, что необходимо для того, чтобы указать платформе Azure расположение виртуального жесткого диска (VHD) для присоединения в качестве диска данных виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bc866-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="bc866-154">Очистку.</span><span class="sxs-lookup"><span data-stu-id="bc866-154">Empty.</span></span>
<span data-ttu-id="bc866-155">Укажите этот объект, чтобы создать пустой диск с данными.</span><span class="sxs-lookup"><span data-stu-id="bc866-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="bc866-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="bc866-156">FromImage.</span></span>
<span data-ttu-id="bc866-157">Укажите этот параметр, чтобы создать виртуальную машину на основе обобщенного образа или диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="bc866-158">При указании этого параметра необходимо указать параметр *SourceImageUri* , чтобы сообщить платформе Azure о том, что расположение виртуального жесткого диска будет прикрепляться в качестве диска данных.</span><span class="sxs-lookup"><span data-stu-id="bc866-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="bc866-159">Параметр *VhdUri* используется в качестве расположения, которое определяет, где будет храниться диск данных, когда он используется виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="bc866-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="bc866-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc866-160">-DefaultProfile</span></span>
<span data-ttu-id="bc866-161">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc866-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc866-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="bc866-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="bc866-163">Указывает идентификатор ресурса набора шифрования диска, управляемого клиентом.</span><span class="sxs-lookup"><span data-stu-id="bc866-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="bc866-164">Это может быть указано только для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="bc866-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="bc866-165">-DiskSizeInGB</span></span>
<span data-ttu-id="bc866-166">Задает размер пустого диска (в гигабайтах), который нужно прикрепить к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="bc866-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="bc866-167">-LUN</span><span class="sxs-lookup"><span data-stu-id="bc866-167">-Lun</span></span>
<span data-ttu-id="bc866-168">Задает логический номер устройства (LUN) для диска с данными.</span><span class="sxs-lookup"><span data-stu-id="bc866-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="bc866-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="bc866-169">-ManagedDiskId</span></span>
<span data-ttu-id="bc866-170">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="bc866-171">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc866-171">-Name</span></span>
<span data-ttu-id="bc866-172">Указывает имя диска данных, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="bc866-172">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="bc866-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="bc866-173">-SourceImageUri</span></span>
<span data-ttu-id="bc866-174">Указывает URI источника диска, к которому прикрепляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bc866-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="bc866-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="bc866-175">-StorageAccountType</span></span>
<span data-ttu-id="bc866-176">Указывает тип учетной записи хранения для управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="bc866-176">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="bc866-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="bc866-177">-VhdUri</span></span>
<span data-ttu-id="bc866-178">Задает универсальный код ресурса (URI) для файла виртуального жесткого диска (VHD), который будет создан при использовании образа платформы или пользовательского образа.</span><span class="sxs-lookup"><span data-stu-id="bc866-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="bc866-179">Этот командлет копирует большой двоичный объект изображения (BLOB) в это расположение.</span><span class="sxs-lookup"><span data-stu-id="bc866-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="bc866-180">Это место, с которого запускается виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="bc866-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="bc866-181">-VM</span><span class="sxs-lookup"><span data-stu-id="bc866-181">-VM</span></span>
<span data-ttu-id="bc866-182">Указывает локальный объект виртуальной машины, к которому нужно добавить диск с данными.</span><span class="sxs-lookup"><span data-stu-id="bc866-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="bc866-183">Вы можете использовать командлет **Get-AzVM** для получения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc866-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="bc866-184">Вы можете использовать командлет **New-AzVMConfig** для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bc866-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="bc866-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="bc866-185">-WriteAccelerator</span></span>
<span data-ttu-id="bc866-186">Указывает, следует ли включить или отключить WriteAccelerator на диске с управляемыми данными.</span><span class="sxs-lookup"><span data-stu-id="bc866-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="bc866-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc866-187">CommonParameters</span></span>
<span data-ttu-id="bc866-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc866-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc866-189">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc866-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc866-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc866-190">INPUTS</span></span>

### <span data-ttu-id="bc866-191">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bc866-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="bc866-192">System. String</span><span class="sxs-lookup"><span data-stu-id="bc866-192">System.String</span></span>

### <span data-ttu-id="bc866-193">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="bc866-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="bc866-194">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc866-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bc866-195">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc866-195">OUTPUTS</span></span>

### <span data-ttu-id="bc866-196">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bc866-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="bc866-197">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="bc866-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="bc866-198">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc866-198">NOTES</span></span>

## <span data-ttu-id="bc866-199">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc866-199">RELATED LINKS</span></span>

[<span data-ttu-id="bc866-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="bc866-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="bc866-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bc866-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bc866-202">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="bc866-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
