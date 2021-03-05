---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: a106435739d7e4ec358038be476cc3f2ba8cd09d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013043"
---
# <span data-ttu-id="c7b15-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="c7b15-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="c7b15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7b15-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b15-103">В нем описывается источник изображений виртуальной машины для создания, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="c7b15-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="c7b15-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7b15-104">SYNTAX</span></span>

### <span data-ttu-id="c7b15-105">ManagedImage (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7b15-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="c7b15-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="c7b15-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="c7b15-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="c7b15-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7b15-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="c7b15-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="c7b15-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7b15-109">DESCRIPTION</span></span>
<span data-ttu-id="c7b15-110">В нем описывается источник изображений виртуальной машины для создания, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="c7b15-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="c7b15-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7b15-111">EXAMPLES</span></span>

### <span data-ttu-id="c7b15-112">Пример 1. Создание источника управляемых изображений</span><span class="sxs-lookup"><span data-stu-id="c7b15-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="c7b15-113">Эта команда создает управляемый источник изображений.</span><span class="sxs-lookup"><span data-stu-id="c7b15-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="c7b15-114">Пример 2. Создание общего источника изображений</span><span class="sxs-lookup"><span data-stu-id="c7b15-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="c7b15-115">Эта команда создает общий источник изображений.</span><span class="sxs-lookup"><span data-stu-id="c7b15-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="c7b15-116">Пример 3. Создание источника изображений platfrom</span><span class="sxs-lookup"><span data-stu-id="c7b15-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="c7b15-117">Эта команда создает источник изображений platfrom.</span><span class="sxs-lookup"><span data-stu-id="c7b15-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="c7b15-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7b15-118">PARAMETERS</span></span>

### <span data-ttu-id="c7b15-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="c7b15-119">-ImageId</span></span>
<span data-ttu-id="c7b15-120">ARM ресурса управляемого изображения в подписке клиента.</span><span class="sxs-lookup"><span data-stu-id="c7b15-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="c7b15-121">-ImageVersionId</span></span>
<span data-ttu-id="c7b15-122">ARM ресурса версии изображения в коллекции общих изображений.</span><span class="sxs-lookup"><span data-stu-id="c7b15-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="c7b15-123">-Offer</span></span>
<span data-ttu-id="c7b15-124">Предложение для изображений из [коллекции Изображений Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="c7b15-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c7b15-125">-PlanName</span></span>
<span data-ttu-id="c7b15-126">Название плана покупки.</span><span class="sxs-lookup"><span data-stu-id="c7b15-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="c7b15-127">-PlanProduct</span></span>
<span data-ttu-id="c7b15-128">Продукт плана покупки.</span><span class="sxs-lookup"><span data-stu-id="c7b15-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="c7b15-129">-PlanPublisher</span></span>
<span data-ttu-id="c7b15-130">Издатель плана покупки.</span><span class="sxs-lookup"><span data-stu-id="c7b15-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c7b15-131">-Publisher</span></span>
<span data-ttu-id="c7b15-132">Изображение Publisher в [коллекции изображений Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="c7b15-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="c7b15-133">-Sku</span></span>
<span data-ttu-id="c7b15-134">SKU изображений из [коллекции изображений Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="c7b15-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="c7b15-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="c7b15-136">В статье описан источник изображений, который является управляемым изображением в подписке клиента.</span><span class="sxs-lookup"><span data-stu-id="c7b15-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="c7b15-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="c7b15-138">Описание источника изображений из коллекции [изображений Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="c7b15-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="c7b15-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="c7b15-140">В статье описан источник изображений, который является версией изображения из коллекции общих изображений.</span><span class="sxs-lookup"><span data-stu-id="c7b15-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-141">-Version</span><span class="sxs-lookup"><span data-stu-id="c7b15-141">-Version</span></span>
<span data-ttu-id="c7b15-142">Версия изображения из [коллекции изображений Azure.](https://docs.microsoft.com/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="c7b15-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b15-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b15-143">CommonParameters</span></span>
<span data-ttu-id="c7b15-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b15-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b15-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7b15-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b15-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7b15-146">INPUTS</span></span>

## <span data-ttu-id="c7b15-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7b15-147">OUTPUTS</span></span>

### <span data-ttu-id="c7b15-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="c7b15-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="c7b15-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7b15-149">NOTES</span></span>

<span data-ttu-id="c7b15-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c7b15-150">ALIASES</span></span>

## <span data-ttu-id="c7b15-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7b15-151">RELATED LINKS</span></span>

