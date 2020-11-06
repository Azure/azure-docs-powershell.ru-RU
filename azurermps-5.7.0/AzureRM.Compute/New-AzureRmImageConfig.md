---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: 7c0f89d9c33dca961b822de62c05158a53195767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568625"
---
# <span data-ttu-id="e6012-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="e6012-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="e6012-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6012-102">SYNOPSIS</span></span>
<span data-ttu-id="e6012-103">Создание настраиваемого объекта изображения.</span><span class="sxs-lookup"><span data-stu-id="e6012-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6012-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6012-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6012-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6012-105">DESCRIPTION</span></span>
<span data-ttu-id="e6012-106">Командлет **New-AzureRmImageConfig** создает настраиваемый объект Image.</span><span class="sxs-lookup"><span data-stu-id="e6012-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="e6012-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6012-107">EXAMPLES</span></span>

### <span data-ttu-id="e6012-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6012-108">Example 1</span></span>
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

<span data-ttu-id="e6012-109">В первой команде создается объект Image, который затем сохраняется в переменной $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="e6012-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="e6012-110">Следующие три команды назначают пути к диску операционной системы и двум дискам данных в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2 переменные.</span><span class="sxs-lookup"><span data-stu-id="e6012-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="e6012-111">Этот подход предназначен для чтения следующих команд.</span><span class="sxs-lookup"><span data-stu-id="e6012-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="e6012-112">Следующие три команды добавляют диск операционной системы и два диска данных в образ, хранящийся в $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="e6012-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="e6012-113">Универсальный код ресурса (URI) каждого диска хранится в $osDiskVhdUri, $dataDiskVhdUri 1 и $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="e6012-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="e6012-114">Последняя команда создает изображение с именем "ImageName01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e6012-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e6012-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6012-115">PARAMETERS</span></span>

### <span data-ttu-id="e6012-116">-Диск</span><span class="sxs-lookup"><span data-stu-id="e6012-116">-DataDisk</span></span>
<span data-ttu-id="e6012-117">Указывает объект диска данных.</span><span class="sxs-lookup"><span data-stu-id="e6012-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6012-118">-Location</span><span class="sxs-lookup"><span data-stu-id="e6012-118">-Location</span></span>
<span data-ttu-id="e6012-119">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="e6012-119">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6012-120">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="e6012-120">-OsDisk</span></span>
<span data-ttu-id="e6012-121">Указывает диск операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e6012-121">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6012-122">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e6012-122">-SourceVirtualMachineId</span></span>
<span data-ttu-id="e6012-123">Указывает идентификатор исходной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e6012-123">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="e6012-124">-Тег</span><span class="sxs-lookup"><span data-stu-id="e6012-124">-Tag</span></span>
<span data-ttu-id="e6012-125">Указывает, что ресурсы и группы ресурсов можно пометить с помощью набора пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="e6012-125">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6012-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6012-126">-Confirm</span></span>
<span data-ttu-id="e6012-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6012-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6012-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6012-128">-WhatIf</span></span>
<span data-ttu-id="e6012-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6012-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6012-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6012-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6012-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6012-131">CommonParameters</span></span>
<span data-ttu-id="e6012-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6012-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6012-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6012-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6012-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6012-134">INPUTS</span></span>

### <span data-ttu-id="e6012-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e6012-135">System.String</span></span>
<span data-ttu-id="e6012-136">System. Collections. Hashtable Microsoft. Azure. Management. COMPUTE. Models. ImageOSDisk Microsoft. Azure. Management. COMPUTE. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="e6012-136">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="e6012-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6012-137">OUTPUTS</span></span>

### <span data-ttu-id="e6012-138">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="e6012-138">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="e6012-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6012-139">NOTES</span></span>

## <span data-ttu-id="e6012-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6012-140">RELATED LINKS</span></span>

