---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermimagedatadisk
schema: 2.0.0
ms.openlocfilehash: b4412cb85534d1aae780b16450726920921d811e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913501"
---
# <span data-ttu-id="90016-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="90016-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="90016-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90016-102">SYNOPSIS</span></span>
<span data-ttu-id="90016-103">Добавляет диск с данными в объект Image.</span><span class="sxs-lookup"><span data-stu-id="90016-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90016-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90016-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90016-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90016-105">DESCRIPTION</span></span>
<span data-ttu-id="90016-106">Командлет **Add-AzureRmImageDataDisk** добавляет диск с данными в объект Image.</span><span class="sxs-lookup"><span data-stu-id="90016-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="90016-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90016-107">EXAMPLES</span></span>

### <span data-ttu-id="90016-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90016-108">Example 1</span></span>
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

<span data-ttu-id="90016-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="90016-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="90016-110">Следующие три команды назначают пути к дискам операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="90016-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="90016-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="90016-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="90016-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="90016-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="90016-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="90016-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="90016-114">Последняя команда создает изображение с именем ImageName01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="90016-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="90016-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90016-115">PARAMETERS</span></span>

### <span data-ttu-id="90016-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="90016-116">-BlobUri</span></span>
<span data-ttu-id="90016-117">Указывает ссылку в качестве универсального кода ресурса (URI) большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="90016-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="90016-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="90016-118">-Caching</span></span>
<span data-ttu-id="90016-119">Задает режим кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="90016-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="90016-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90016-120">-DefaultProfile</span></span>
<span data-ttu-id="90016-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90016-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90016-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="90016-122">-DiskSizeGB</span></span>
<span data-ttu-id="90016-123">Задает размер диска в гигабайтах (ГБ).</span><span class="sxs-lookup"><span data-stu-id="90016-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="90016-124">-Image</span><span class="sxs-lookup"><span data-stu-id="90016-124">-Image</span></span>
<span data-ttu-id="90016-125">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="90016-125">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90016-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="90016-126">-Lun</span></span>
<span data-ttu-id="90016-127">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="90016-127">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90016-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="90016-128">-ManagedDiskId</span></span>
<span data-ttu-id="90016-129">Указывает идентификатор управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="90016-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="90016-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="90016-130">-SnapshotId</span></span>
<span data-ttu-id="90016-131">Указывает идентификатор снимка.</span><span class="sxs-lookup"><span data-stu-id="90016-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="90016-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="90016-132">-StorageAccountType</span></span>
<span data-ttu-id="90016-133">Тип учетной записи хранения на диске образа данных</span><span class="sxs-lookup"><span data-stu-id="90016-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="90016-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90016-134">-Confirm</span></span>
<span data-ttu-id="90016-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90016-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90016-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90016-136">-WhatIf</span></span>
<span data-ttu-id="90016-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90016-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90016-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90016-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90016-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90016-139">CommonParameters</span></span>
<span data-ttu-id="90016-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90016-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90016-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90016-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90016-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90016-142">INPUTS</span></span>

### <span data-ttu-id="90016-143">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="90016-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="90016-144">System. Int32 System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="90016-144">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="90016-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90016-145">OUTPUTS</span></span>

### <span data-ttu-id="90016-146">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="90016-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="90016-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="90016-147">NOTES</span></span>

## <span data-ttu-id="90016-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90016-148">RELATED LINKS</span></span>

