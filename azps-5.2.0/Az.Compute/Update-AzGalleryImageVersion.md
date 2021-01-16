---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397604"
---
# <span data-ttu-id="46844-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="46844-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="46844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46844-102">SYNOPSIS</span></span>
<span data-ttu-id="46844-103">Обновив версию изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="46844-103">Update a gallery image version.</span></span>

## <span data-ttu-id="46844-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46844-104">SYNTAX</span></span>

### <span data-ttu-id="46844-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46844-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46844-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="46844-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46844-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="46844-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46844-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46844-108">DESCRIPTION</span></span>
<span data-ttu-id="46844-109">Обновив версию изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="46844-109">Update a gallery image version.</span></span>

## <span data-ttu-id="46844-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46844-110">EXAMPLES</span></span>

### <span data-ttu-id="46844-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46844-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="46844-112">Обновив версию изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="46844-112">Update a gallery image version.</span></span>

## <span data-ttu-id="46844-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46844-113">PARAMETERS</span></span>

### <span data-ttu-id="46844-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46844-114">-AsJob</span></span>
<span data-ttu-id="46844-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="46844-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46844-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46844-116">-DefaultProfile</span></span>
<span data-ttu-id="46844-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46844-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46844-118">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="46844-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="46844-119">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="46844-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="46844-120">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="46844-120">-GalleryName</span></span>
<span data-ttu-id="46844-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="46844-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="46844-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46844-122">-InputObject</span></span>
<span data-ttu-id="46844-123">Объект версии изображения из коллекции PS.</span><span class="sxs-lookup"><span data-stu-id="46844-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="46844-124">-Name</span><span class="sxs-lookup"><span data-stu-id="46844-124">-Name</span></span>
<span data-ttu-id="46844-125">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="46844-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="46844-126">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="46844-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="46844-127">Дата окончания жизненного срока версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="46844-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="46844-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="46844-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="46844-129">Если он установлен, виртуальные машины, развернутые из последней версии определения изображения, не будут использовать эту версию изображения.</span><span class="sxs-lookup"><span data-stu-id="46844-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="46844-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="46844-130">-ReplicaCount</span></span>
<span data-ttu-id="46844-131">Количество копий версии изображения, созда необходимой для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="46844-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="46844-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46844-132">-ResourceGroupName</span></span>
<span data-ttu-id="46844-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46844-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="46844-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46844-134">-ResourceId</span></span>
<span data-ttu-id="46844-135">ИД ресурса для версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="46844-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="46844-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="46844-136">-Tag</span></span>
<span data-ttu-id="46844-137">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="46844-137">Resource tags</span></span>

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

### <span data-ttu-id="46844-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="46844-138">-TargetRegion</span></span>
<span data-ttu-id="46844-139">Целевые области, в которые будет реплицирована версия изображения.</span><span class="sxs-lookup"><span data-stu-id="46844-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="46844-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46844-140">-Confirm</span></span>
<span data-ttu-id="46844-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46844-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46844-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46844-142">-WhatIf</span></span>
<span data-ttu-id="46844-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46844-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46844-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="46844-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46844-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46844-145">CommonParameters</span></span>
<span data-ttu-id="46844-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46844-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46844-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46844-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46844-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46844-148">INPUTS</span></span>

### <span data-ttu-id="46844-149">System.String</span><span class="sxs-lookup"><span data-stu-id="46844-149">System.String</span></span>

### <span data-ttu-id="46844-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="46844-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="46844-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="46844-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="46844-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="46844-152">System.Int32</span></span>

### <span data-ttu-id="46844-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="46844-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="46844-154">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="46844-154">System.DateTime</span></span>

### <span data-ttu-id="46844-155">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="46844-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="46844-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46844-156">OUTPUTS</span></span>

### <span data-ttu-id="46844-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="46844-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="46844-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46844-158">NOTES</span></span>

## <span data-ttu-id="46844-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46844-159">RELATED LINKS</span></span>
