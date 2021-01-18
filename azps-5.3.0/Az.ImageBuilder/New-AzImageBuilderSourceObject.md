---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504789"
---
# <span data-ttu-id="064b8-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="064b8-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="064b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="064b8-102">SYNOPSIS</span></span>
<span data-ttu-id="064b8-103">В нем описывается источник изображений виртуальной машины для создания, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="064b8-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="064b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="064b8-104">SYNTAX</span></span>

### <span data-ttu-id="064b8-105">ManagedImage (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="064b8-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="064b8-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="064b8-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="064b8-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="064b8-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="064b8-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="064b8-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="064b8-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="064b8-109">DESCRIPTION</span></span>
<span data-ttu-id="064b8-110">В нем описывается источник изображений виртуальной машины для создания, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="064b8-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="064b8-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="064b8-111">EXAMPLES</span></span>

### <span data-ttu-id="064b8-112">Пример 1. Создание управляемого источника изображений</span><span class="sxs-lookup"><span data-stu-id="064b8-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="064b8-113">Эта команда создает управляемый источник изображений.</span><span class="sxs-lookup"><span data-stu-id="064b8-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="064b8-114">Пример 2. Создание общего источника изображений</span><span class="sxs-lookup"><span data-stu-id="064b8-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="064b8-115">Эта команда создает общий источник изображений.</span><span class="sxs-lookup"><span data-stu-id="064b8-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="064b8-116">Пример 3. Создание источника изображений platfrom</span><span class="sxs-lookup"><span data-stu-id="064b8-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="064b8-117">Эта команда создает источник изображений platfrom.</span><span class="sxs-lookup"><span data-stu-id="064b8-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="064b8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="064b8-118">PARAMETERS</span></span>

### <span data-ttu-id="064b8-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="064b8-119">-ImageId</span></span>
<span data-ttu-id="064b8-120">ARM ресурса управляемого изображения в подписке клиента.</span><span class="sxs-lookup"><span data-stu-id="064b8-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="064b8-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="064b8-121">-ImageVersionId</span></span>
<span data-ttu-id="064b8-122">ARM ресурса версии изображения в коллекции общих изображений.</span><span class="sxs-lookup"><span data-stu-id="064b8-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="064b8-123">-Offer</span><span class="sxs-lookup"><span data-stu-id="064b8-123">-Offer</span></span>
<span data-ttu-id="064b8-124">Предложение для изображений из [коллекции Изображений Azure.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="064b8-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="064b8-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="064b8-125">-PlanName</span></span>
<span data-ttu-id="064b8-126">Имя плана покупки.</span><span class="sxs-lookup"><span data-stu-id="064b8-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="064b8-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="064b8-127">-PlanProduct</span></span>
<span data-ttu-id="064b8-128">Продукт плана покупки.</span><span class="sxs-lookup"><span data-stu-id="064b8-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="064b8-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="064b8-129">-PlanPublisher</span></span>
<span data-ttu-id="064b8-130">Издатель плана покупки.</span><span class="sxs-lookup"><span data-stu-id="064b8-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="064b8-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="064b8-131">-Publisher</span></span>
<span data-ttu-id="064b8-132">Изображение Publisher в [коллекции изображений Azure.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="064b8-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="064b8-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="064b8-133">-Sku</span></span>
<span data-ttu-id="064b8-134">SKU изображений из [коллекции изображений Azure.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="064b8-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="064b8-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="064b8-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="064b8-136">В статье описан источник изображений, который является управляемым изображением в подписке клиента.</span><span class="sxs-lookup"><span data-stu-id="064b8-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="064b8-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="064b8-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="064b8-138">Описание источника изображений из коллекции [изображений Azure.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="064b8-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="064b8-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="064b8-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="064b8-140">В статье описан источник изображений, который является версией изображения из общей коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="064b8-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="064b8-141">-Версия</span><span class="sxs-lookup"><span data-stu-id="064b8-141">-Version</span></span>
<span data-ttu-id="064b8-142">Версия изображения из [коллекции изображений Azure.](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)</span><span class="sxs-lookup"><span data-stu-id="064b8-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="064b8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064b8-143">CommonParameters</span></span>
<span data-ttu-id="064b8-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="064b8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064b8-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="064b8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064b8-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="064b8-146">INPUTS</span></span>

## <span data-ttu-id="064b8-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="064b8-147">OUTPUTS</span></span>

### <span data-ttu-id="064b8-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="064b8-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="064b8-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="064b8-149">NOTES</span></span>

<span data-ttu-id="064b8-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="064b8-150">ALIASES</span></span>

## <span data-ttu-id="064b8-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="064b8-151">RELATED LINKS</span></span>

