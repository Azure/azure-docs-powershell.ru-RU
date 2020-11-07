---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
ms.openlocfilehash: f27c861386e7a570fe72a5266362bee7fed39e5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734686"
---
# <span data-ttu-id="c2237-101">New-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="c2237-101">New-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="c2237-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2237-102">SYNOPSIS</span></span>
<span data-ttu-id="c2237-103">Создайте версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="c2237-103">Create a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2237-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2237-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2237-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2237-105">DESCRIPTION</span></span>
<span data-ttu-id="c2237-106">Создайте версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="c2237-106">Create a gallery image version.</span></span>

## <span data-ttu-id="c2237-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2237-107">EXAMPLES</span></span>

### <span data-ttu-id="c2237-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2237-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="c2237-109">Создайте версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="c2237-109">Create a gallery image version.</span></span>

## <span data-ttu-id="c2237-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2237-110">PARAMETERS</span></span>

### <span data-ttu-id="c2237-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2237-111">-AsJob</span></span>
<span data-ttu-id="c2237-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c2237-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2237-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2237-113">-DefaultProfile</span></span>
<span data-ttu-id="c2237-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2237-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="c2237-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="c2237-116">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="c2237-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="c2237-117">-GalleryName</span></span>
<span data-ttu-id="c2237-118">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="c2237-118">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c2237-119">-Location</span></span>
<span data-ttu-id="c2237-120">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="c2237-120">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2237-121">-Name</span></span>
<span data-ttu-id="c2237-122">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="c2237-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="c2237-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="c2237-124">Дата окончания срока действия версии изображения в галерее.</span><span class="sxs-lookup"><span data-stu-id="c2237-124">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="c2237-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="c2237-126">Если задано значение, виртуальные машины, развернутые из последней версии определения образа, не будут использовать эту версию изображения.</span><span class="sxs-lookup"><span data-stu-id="c2237-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="c2237-127">-ReplicaCount</span></span>
<span data-ttu-id="c2237-128">Число реплик для версии изображения, создаваемой для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="c2237-128">The number of replicas of the Image Version to be created per region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2237-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2237-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c2237-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="c2237-131">-SourceImageId</span></span>
<span data-ttu-id="c2237-132">Идентификатор исходного изображения, из которого будет создана версия изображения.</span><span class="sxs-lookup"><span data-stu-id="c2237-132">The ID of the source image from which the Image Version is going to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="c2237-133">-Tag</span></span>
<span data-ttu-id="c2237-134">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="c2237-134">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="c2237-135">-TargetRegion</span></span>
<span data-ttu-id="c2237-136">Целевые области, на которые должна быть реплицирована версия изображения.</span><span class="sxs-lookup"><span data-stu-id="c2237-136">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2237-137">-Confirm</span></span>
<span data-ttu-id="c2237-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c2237-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2237-139">-WhatIf</span></span>
<span data-ttu-id="c2237-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c2237-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2237-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c2237-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2237-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2237-142">CommonParameters</span></span>
<span data-ttu-id="c2237-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2237-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2237-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2237-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2237-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2237-145">INPUTS</span></span>

### <span data-ttu-id="c2237-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c2237-146">System.String</span></span>

### <span data-ttu-id="c2237-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c2237-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c2237-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c2237-148">System.Int32</span></span>

### <span data-ttu-id="c2237-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2237-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c2237-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c2237-150">System.DateTime</span></span>

### <span data-ttu-id="c2237-151">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="c2237-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="c2237-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2237-152">OUTPUTS</span></span>

### <span data-ttu-id="c2237-153">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="c2237-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="c2237-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2237-154">NOTES</span></span>

## <span data-ttu-id="c2237-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2237-155">RELATED LINKS</span></span>
