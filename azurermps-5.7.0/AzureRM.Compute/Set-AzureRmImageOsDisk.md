---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 8deb191a6a26e4fb0001a1cbb78540460256dd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557532"
---
# <span data-ttu-id="d6275-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="d6275-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="d6275-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6275-102">SYNOPSIS</span></span>
<span data-ttu-id="d6275-103">Задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="d6275-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6275-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6275-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <Image> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6275-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6275-105">DESCRIPTION</span></span>
<span data-ttu-id="d6275-106">Командлет **Set-AzureRmImageOsDisk** задает свойства диска операционной системы для объекта Image.</span><span class="sxs-lookup"><span data-stu-id="d6275-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="d6275-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6275-107">EXAMPLES</span></span>

### <span data-ttu-id="d6275-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6275-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="d6275-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="d6275-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="d6275-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="d6275-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="d6275-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="d6275-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="d6275-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="d6275-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="d6275-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="d6275-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="d6275-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d6275-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d6275-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6275-115">PARAMETERS</span></span>

### <span data-ttu-id="d6275-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="d6275-116">-BlobUri</span></span>
<span data-ttu-id="d6275-117">Задает универсальный код ресурса (URI) большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="d6275-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6275-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="d6275-118">-Caching</span></span>
<span data-ttu-id="d6275-119">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="d6275-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6275-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d6275-120">-DiskSizeGB</span></span>
<span data-ttu-id="d6275-121">Задает размер диска в ГБ.</span><span class="sxs-lookup"><span data-stu-id="d6275-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="d6275-122">-Image</span><span class="sxs-lookup"><span data-stu-id="d6275-122">-Image</span></span>
<span data-ttu-id="d6275-123">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="d6275-123">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6275-124">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="d6275-124">-ManagedDiskId</span></span>
<span data-ttu-id="d6275-125">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="d6275-125">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="d6275-126">-OsState</span><span class="sxs-lookup"><span data-stu-id="d6275-126">-OsState</span></span>
<span data-ttu-id="d6275-127">Указывает состояние операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d6275-127">Specifies the OS state.</span></span>

```yaml
Type: OperatingSystemStateTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6275-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="d6275-128">-OsType</span></span>
<span data-ttu-id="d6275-129">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d6275-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6275-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="d6275-130">-SnapshotId</span></span>
<span data-ttu-id="d6275-131">Указывает идентификатор снимка.</span><span class="sxs-lookup"><span data-stu-id="d6275-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="d6275-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d6275-132">-StorageAccountType</span></span>
<span data-ttu-id="d6275-133">Тип учетной записи хранения на диске образа операционной системы</span><span class="sxs-lookup"><span data-stu-id="d6275-133">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6275-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6275-134">-Confirm</span></span>
<span data-ttu-id="d6275-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6275-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6275-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6275-136">-WhatIf</span></span>
<span data-ttu-id="d6275-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6275-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6275-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6275-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6275-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6275-139">CommonParameters</span></span>
<span data-ttu-id="d6275-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6275-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6275-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6275-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6275-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6275-142">INPUTS</span></span>

### <span data-ttu-id="d6275-143">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="d6275-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="d6275-144">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. Version = 14.0.0.0, Culture. OperatingSystemStateTypes;. System. String.. Nullable, # = 31bf3856ad364e35]] String. строковых параметров `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` : NULL 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d6275-144">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d6275-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6275-145">OUTPUTS</span></span>

### <span data-ttu-id="d6275-146">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="d6275-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="d6275-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6275-147">NOTES</span></span>

## <span data-ttu-id="d6275-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6275-148">RELATED LINKS</span></span>

