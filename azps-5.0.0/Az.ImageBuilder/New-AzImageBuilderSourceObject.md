---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311771"
---
# <span data-ttu-id="6947c-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="6947c-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="6947c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6947c-102">SYNOPSIS</span></span>
<span data-ttu-id="6947c-103">Описывает источник образа виртуальной машины для сборки, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="6947c-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="6947c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6947c-104">SYNTAX</span></span>

### <span data-ttu-id="6947c-105">ManagedImage (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6947c-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="6947c-106">PlatformImage</span><span class="sxs-lookup"><span data-stu-id="6947c-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="6947c-107">PlatformImagePlanInfo</span><span class="sxs-lookup"><span data-stu-id="6947c-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6947c-108">SharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="6947c-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="6947c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6947c-109">DESCRIPTION</span></span>
<span data-ttu-id="6947c-110">Описывает источник образа виртуальной машины для сборки, настройки и распространения.</span><span class="sxs-lookup"><span data-stu-id="6947c-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="6947c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6947c-111">EXAMPLES</span></span>

### <span data-ttu-id="6947c-112">Пример 1: создание источника управляемых изображений</span><span class="sxs-lookup"><span data-stu-id="6947c-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="6947c-113">Эта команда создает управляемый источник изображений.</span><span class="sxs-lookup"><span data-stu-id="6947c-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="6947c-114">Пример 2: создание общего источника изображения</span><span class="sxs-lookup"><span data-stu-id="6947c-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="6947c-115">Эта команда создает общий источник изображений.</span><span class="sxs-lookup"><span data-stu-id="6947c-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="6947c-116">Пример 3: создание источника изображения platfrom</span><span class="sxs-lookup"><span data-stu-id="6947c-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="6947c-117">Эта команда создает источник изображения platfrom.</span><span class="sxs-lookup"><span data-stu-id="6947c-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="6947c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6947c-118">PARAMETERS</span></span>

### <span data-ttu-id="6947c-119">-ImageId</span><span class="sxs-lookup"><span data-stu-id="6947c-119">-ImageId</span></span>
<span data-ttu-id="6947c-120">Идентификатор ресурса ARM управляемого изображения в подписке клиента.</span><span class="sxs-lookup"><span data-stu-id="6947c-120">ARM resource id of the managed image in customer subscription.</span></span>

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

### <span data-ttu-id="6947c-121">-ImageVersionId</span><span class="sxs-lookup"><span data-stu-id="6947c-121">-ImageVersionId</span></span>
<span data-ttu-id="6947c-122">Идентификатор ресурса ARM для версии изображения в коллекции общих изображений.</span><span class="sxs-lookup"><span data-stu-id="6947c-122">ARM resource id of the image version in the shared image gallery.</span></span>

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

### <span data-ttu-id="6947c-123">-Предложение</span><span class="sxs-lookup"><span data-stu-id="6947c-123">-Offer</span></span>
<span data-ttu-id="6947c-124">Предложения изображений из [коллекций Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="6947c-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="6947c-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="6947c-125">-PlanName</span></span>
<span data-ttu-id="6947c-126">Название плана покупок.</span><span class="sxs-lookup"><span data-stu-id="6947c-126">Name of the purchase plan.</span></span>

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

### <span data-ttu-id="6947c-127">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="6947c-127">-PlanProduct</span></span>
<span data-ttu-id="6947c-128">Произведение плана покупок.</span><span class="sxs-lookup"><span data-stu-id="6947c-128">Product of the purchase plan.</span></span>

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

### <span data-ttu-id="6947c-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="6947c-129">-PlanPublisher</span></span>
<span data-ttu-id="6947c-130">Издатель плана покупок.</span><span class="sxs-lookup"><span data-stu-id="6947c-130">Publisher of the purchase plan.</span></span>

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

### <span data-ttu-id="6947c-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6947c-131">-Publisher</span></span>
<span data-ttu-id="6947c-132">Издатель изображений в [коллекции образов Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="6947c-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="6947c-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="6947c-133">-Sku</span></span>
<span data-ttu-id="6947c-134">SKU изображений из [коллекции Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="6947c-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="6947c-135">-SourceTypeManagedImage</span><span class="sxs-lookup"><span data-stu-id="6947c-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="6947c-136">Описывает источник изображения, который является управляемым изображением в подписке клиента.</span><span class="sxs-lookup"><span data-stu-id="6947c-136">Describes an image source that is a managed image in customer subscription.</span></span>

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

### <span data-ttu-id="6947c-137">-SourceTypePlatformImage</span><span class="sxs-lookup"><span data-stu-id="6947c-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="6947c-138">Описывает источник изображения из [образов коллекции Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="6947c-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="6947c-139">-SourceTypeSharedImageVersion</span><span class="sxs-lookup"><span data-stu-id="6947c-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="6947c-140">Описывает источник изображения, который является версией изображения в общей коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="6947c-140">Describes an image source that is an image version in a shared image gallery.</span></span>

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

### <span data-ttu-id="6947c-141">-Version</span><span class="sxs-lookup"><span data-stu-id="6947c-141">-Version</span></span>
<span data-ttu-id="6947c-142">Версия изображения из [образов коллекции Azure](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span><span class="sxs-lookup"><span data-stu-id="6947c-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

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

### <span data-ttu-id="6947c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6947c-143">CommonParameters</span></span>
<span data-ttu-id="6947c-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6947c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6947c-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6947c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6947c-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6947c-146">INPUTS</span></span>

## <span data-ttu-id="6947c-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6947c-147">OUTPUTS</span></span>

### <span data-ttu-id="6947c-148">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. Api20200214. IImageTemplateSource</span><span class="sxs-lookup"><span data-stu-id="6947c-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="6947c-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="6947c-149">NOTES</span></span>

<span data-ttu-id="6947c-150">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="6947c-150">ALIASES</span></span>

## <span data-ttu-id="6947c-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6947c-151">RELATED LINKS</span></span>

