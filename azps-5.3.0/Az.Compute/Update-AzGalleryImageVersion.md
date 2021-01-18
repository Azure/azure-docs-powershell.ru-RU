---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519426"
---
# <span data-ttu-id="aabbb-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="aabbb-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="aabbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aabbb-102">SYNOPSIS</span></span>
<span data-ttu-id="aabbb-103">Обновив версию изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="aabbb-103">Update a gallery image version.</span></span>

## <span data-ttu-id="aabbb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aabbb-104">SYNTAX</span></span>

### <span data-ttu-id="aabbb-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aabbb-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aabbb-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="aabbb-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aabbb-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="aabbb-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aabbb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aabbb-108">DESCRIPTION</span></span>
<span data-ttu-id="aabbb-109">Обновив версию изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="aabbb-109">Update a gallery image version.</span></span>

## <span data-ttu-id="aabbb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aabbb-110">EXAMPLES</span></span>

### <span data-ttu-id="aabbb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aabbb-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="aabbb-112">Обновив версию изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="aabbb-112">Update a gallery image version.</span></span>

## <span data-ttu-id="aabbb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aabbb-113">PARAMETERS</span></span>

### <span data-ttu-id="aabbb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aabbb-114">-AsJob</span></span>
<span data-ttu-id="aabbb-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aabbb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aabbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aabbb-116">-DefaultProfile</span></span>
<span data-ttu-id="aabbb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aabbb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aabbb-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="aabbb-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="aabbb-119">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="aabbb-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="aabbb-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="aabbb-120">-GalleryName</span></span>
<span data-ttu-id="aabbb-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="aabbb-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="aabbb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aabbb-122">-InputObject</span></span>
<span data-ttu-id="aabbb-123">Объект версии изображения из коллекции PS.</span><span class="sxs-lookup"><span data-stu-id="aabbb-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="aabbb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="aabbb-124">-Name</span></span>
<span data-ttu-id="aabbb-125">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="aabbb-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="aabbb-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="aabbb-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="aabbb-127">Дата окончания жизненного срока версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="aabbb-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="aabbb-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="aabbb-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="aabbb-129">Если она установлена, виртуальные машины, развернутые из последней версии определения изображения, не будут использовать эту версию изображения.</span><span class="sxs-lookup"><span data-stu-id="aabbb-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="aabbb-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="aabbb-130">-ReplicaCount</span></span>
<span data-ttu-id="aabbb-131">Количество копий версии изображения, созда необходимой для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="aabbb-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="aabbb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aabbb-132">-ResourceGroupName</span></span>
<span data-ttu-id="aabbb-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aabbb-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="aabbb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aabbb-134">-ResourceId</span></span>
<span data-ttu-id="aabbb-135">ИД ресурса для версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="aabbb-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="aabbb-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="aabbb-136">-Tag</span></span>
<span data-ttu-id="aabbb-137">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="aabbb-137">Resource tags</span></span>

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

### <span data-ttu-id="aabbb-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="aabbb-138">-TargetRegion</span></span>
<span data-ttu-id="aabbb-139">Целевые области, в которые будет реплицирована версия изображения.</span><span class="sxs-lookup"><span data-stu-id="aabbb-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="aabbb-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aabbb-140">-Confirm</span></span>
<span data-ttu-id="aabbb-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aabbb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aabbb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aabbb-142">-WhatIf</span></span>
<span data-ttu-id="aabbb-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aabbb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aabbb-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aabbb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aabbb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabbb-145">CommonParameters</span></span>
<span data-ttu-id="aabbb-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aabbb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabbb-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aabbb-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabbb-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aabbb-148">INPUTS</span></span>

### <span data-ttu-id="aabbb-149">System.String</span><span class="sxs-lookup"><span data-stu-id="aabbb-149">System.String</span></span>

### <span data-ttu-id="aabbb-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="aabbb-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="aabbb-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aabbb-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aabbb-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="aabbb-152">System.Int32</span></span>

### <span data-ttu-id="aabbb-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aabbb-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="aabbb-154">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="aabbb-154">System.DateTime</span></span>

### <span data-ttu-id="aabbb-155">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="aabbb-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="aabbb-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aabbb-156">OUTPUTS</span></span>

### <span data-ttu-id="aabbb-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="aabbb-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="aabbb-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aabbb-158">NOTES</span></span>

## <span data-ttu-id="aabbb-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aabbb-159">RELATED LINKS</span></span>
