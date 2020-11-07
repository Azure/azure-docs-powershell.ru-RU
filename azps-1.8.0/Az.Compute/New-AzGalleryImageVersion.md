---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 6d5731916309baf93552f9b5d71f30943178f11c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731313"
---
# <span data-ttu-id="7a919-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7a919-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="7a919-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a919-102">SYNOPSIS</span></span>
<span data-ttu-id="7a919-103">Создайте версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="7a919-103">Create a gallery image version.</span></span>

## <span data-ttu-id="7a919-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a919-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a919-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a919-105">DESCRIPTION</span></span>
<span data-ttu-id="7a919-106">Создайте версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="7a919-106">Create a gallery image version.</span></span>

## <span data-ttu-id="7a919-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a919-107">EXAMPLES</span></span>

### <span data-ttu-id="7a919-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a919-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="7a919-109">Создайте версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="7a919-109">Create a gallery image version.</span></span>

## <span data-ttu-id="7a919-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a919-110">PARAMETERS</span></span>

### <span data-ttu-id="7a919-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a919-111">-AsJob</span></span>
<span data-ttu-id="7a919-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7a919-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a919-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a919-113">-DefaultProfile</span></span>
<span data-ttu-id="7a919-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a919-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a919-115">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7a919-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="7a919-116">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="7a919-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="7a919-117">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="7a919-117">-GalleryName</span></span>
<span data-ttu-id="7a919-118">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="7a919-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="7a919-119">-Location</span><span class="sxs-lookup"><span data-stu-id="7a919-119">-Location</span></span>
<span data-ttu-id="7a919-120">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="7a919-120">Resource location</span></span>

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

### <span data-ttu-id="7a919-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a919-121">-Name</span></span>
<span data-ttu-id="7a919-122">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="7a919-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="7a919-123">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="7a919-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="7a919-124">Дата окончания срока действия версии изображения в галерее.</span><span class="sxs-lookup"><span data-stu-id="7a919-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="7a919-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="7a919-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="7a919-126">Если задано значение, виртуальные машины, развернутые из последней версии определения образа, не будут использовать эту версию изображения.</span><span class="sxs-lookup"><span data-stu-id="7a919-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="7a919-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="7a919-127">-ReplicaCount</span></span>
<span data-ttu-id="7a919-128">Число реплик для версии изображения, создаваемой для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="7a919-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="7a919-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a919-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a919-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a919-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a919-131">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="7a919-131">-SourceImageId</span></span>
<span data-ttu-id="7a919-132">Идентификатор исходного изображения, из которого будет создана версия изображения.</span><span class="sxs-lookup"><span data-stu-id="7a919-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="7a919-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="7a919-133">-Tag</span></span>
<span data-ttu-id="7a919-134">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="7a919-134">Resource tags</span></span>

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

### <span data-ttu-id="7a919-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="7a919-135">-TargetRegion</span></span>
<span data-ttu-id="7a919-136">Целевые области, на которые должна быть реплицирована версия изображения.</span><span class="sxs-lookup"><span data-stu-id="7a919-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="7a919-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a919-137">-Confirm</span></span>
<span data-ttu-id="7a919-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a919-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a919-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a919-139">-WhatIf</span></span>
<span data-ttu-id="7a919-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a919-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a919-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a919-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a919-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a919-142">CommonParameters</span></span>
<span data-ttu-id="7a919-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a919-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a919-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a919-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a919-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a919-145">INPUTS</span></span>

### <span data-ttu-id="7a919-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7a919-146">System.String</span></span>

### <span data-ttu-id="7a919-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7a919-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7a919-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7a919-148">System.Int32</span></span>

### <span data-ttu-id="7a919-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a919-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7a919-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="7a919-150">System.DateTime</span></span>

### <span data-ttu-id="7a919-151">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="7a919-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="7a919-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a919-152">OUTPUTS</span></span>

### <span data-ttu-id="7a919-153">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7a919-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="7a919-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a919-154">NOTES</span></span>

## <span data-ttu-id="7a919-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a919-155">RELATED LINKS</span></span>
