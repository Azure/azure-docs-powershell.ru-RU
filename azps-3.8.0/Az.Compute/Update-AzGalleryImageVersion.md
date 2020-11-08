---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072581"
---
# <span data-ttu-id="8b175-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8b175-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="8b175-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b175-102">SYNOPSIS</span></span>
<span data-ttu-id="8b175-103">Обновите версию картинки в галерее.</span><span class="sxs-lookup"><span data-stu-id="8b175-103">Update a gallery image version.</span></span>

## <span data-ttu-id="8b175-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b175-104">SYNTAX</span></span>

### <span data-ttu-id="8b175-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b175-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b175-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8b175-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b175-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8b175-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b175-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b175-108">DESCRIPTION</span></span>
<span data-ttu-id="8b175-109">Обновите версию картинки в галерее.</span><span class="sxs-lookup"><span data-stu-id="8b175-109">Update a gallery image version.</span></span>

## <span data-ttu-id="8b175-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b175-110">EXAMPLES</span></span>

### <span data-ttu-id="8b175-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b175-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="8b175-112">Обновите версию картинки в галерее.</span><span class="sxs-lookup"><span data-stu-id="8b175-112">Update a gallery image version.</span></span>

## <span data-ttu-id="8b175-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b175-113">PARAMETERS</span></span>

### <span data-ttu-id="8b175-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b175-114">-AsJob</span></span>
<span data-ttu-id="8b175-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8b175-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b175-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b175-116">-DefaultProfile</span></span>
<span data-ttu-id="8b175-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b175-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b175-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="8b175-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="8b175-119">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="8b175-119">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b175-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="8b175-120">-GalleryName</span></span>
<span data-ttu-id="8b175-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="8b175-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b175-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b175-122">-InputObject</span></span>
<span data-ttu-id="8b175-123">Объект версии изображения коллекции PS.</span><span class="sxs-lookup"><span data-stu-id="8b175-123">The PS Gallery Image Version Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b175-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b175-124">-Name</span></span>
<span data-ttu-id="8b175-125">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="8b175-125">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b175-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="8b175-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="8b175-127">Дата окончания срока действия версии изображения в галерее.</span><span class="sxs-lookup"><span data-stu-id="8b175-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="8b175-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="8b175-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="8b175-129">Если задано значение, виртуальные машины, развернутые из последней версии определения образа, не будут использовать эту версию изображения.</span><span class="sxs-lookup"><span data-stu-id="8b175-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="8b175-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="8b175-130">-ReplicaCount</span></span>
<span data-ttu-id="8b175-131">Число реплик для версии изображения, создаваемой для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="8b175-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="8b175-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b175-132">-ResourceGroupName</span></span>
<span data-ttu-id="8b175-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b175-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b175-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b175-134">-ResourceId</span></span>
<span data-ttu-id="8b175-135">Идентификатор ресурса для версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="8b175-135">The resource ID for the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b175-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="8b175-136">-Tag</span></span>
<span data-ttu-id="8b175-137">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="8b175-137">Resource tags</span></span>

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

### <span data-ttu-id="8b175-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="8b175-138">-TargetRegion</span></span>
<span data-ttu-id="8b175-139">Целевые области, на которые должна быть реплицирована версия изображения.</span><span class="sxs-lookup"><span data-stu-id="8b175-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="8b175-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b175-140">-Confirm</span></span>
<span data-ttu-id="8b175-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b175-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b175-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b175-142">-WhatIf</span></span>
<span data-ttu-id="8b175-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b175-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b175-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b175-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b175-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b175-145">CommonParameters</span></span>
<span data-ttu-id="8b175-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b175-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b175-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b175-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b175-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b175-148">INPUTS</span></span>

### <span data-ttu-id="8b175-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8b175-149">System.String</span></span>

### <span data-ttu-id="8b175-150">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8b175-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="8b175-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8b175-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8b175-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8b175-152">System.Int32</span></span>

### <span data-ttu-id="8b175-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8b175-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8b175-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="8b175-154">System.DateTime</span></span>

### <span data-ttu-id="8b175-155">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="8b175-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="8b175-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b175-156">OUTPUTS</span></span>

### <span data-ttu-id="8b175-157">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8b175-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="8b175-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b175-158">NOTES</span></span>

## <span data-ttu-id="8b175-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b175-159">RELATED LINKS</span></span>
