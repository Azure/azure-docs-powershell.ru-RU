---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403708"
---
# <span data-ttu-id="9ab55-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="9ab55-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="9ab55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ab55-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab55-103">Универсальный объект рассылки</span><span class="sxs-lookup"><span data-stu-id="9ab55-103">Generic distribution object</span></span>

## <span data-ttu-id="9ab55-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ab55-104">SYNTAX</span></span>

### <span data-ttu-id="9ab55-105">ManagedImageDistributor (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ab55-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="9ab55-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="9ab55-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="9ab55-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="9ab55-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="9ab55-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ab55-108">DESCRIPTION</span></span>
<span data-ttu-id="9ab55-109">Универсальный объект рассылки</span><span class="sxs-lookup"><span data-stu-id="9ab55-109">Generic distribution object</span></span>

## <span data-ttu-id="9ab55-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ab55-110">EXAMPLES</span></span>

### <span data-ttu-id="9ab55-111">Пример 1. Создание распространителя управляемых изображений</span><span class="sxs-lookup"><span data-stu-id="9ab55-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="9ab55-112">Эта команда создает распространитель управляемых изображений.</span><span class="sxs-lookup"><span data-stu-id="9ab55-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="9ab55-113">Пример 2. Создание распространителя VHD</span><span class="sxs-lookup"><span data-stu-id="9ab55-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="9ab55-114">Эта команда создает распространитель VHD.</span><span class="sxs-lookup"><span data-stu-id="9ab55-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="9ab55-115">Пример 3. Создание распространителя общих изображений</span><span class="sxs-lookup"><span data-stu-id="9ab55-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="9ab55-116">Эта команда создает общий распространитель изображений.</span><span class="sxs-lookup"><span data-stu-id="9ab55-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="9ab55-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ab55-117">PARAMETERS</span></span>

### <span data-ttu-id="9ab55-118">-Артефакт</span><span class="sxs-lookup"><span data-stu-id="9ab55-118">-ArtifactTag</span></span>
<span data-ttu-id="9ab55-119">Теги, которые будут применяться к артефакту после его создания или обновления дистрибьютором.</span><span class="sxs-lookup"><span data-stu-id="9ab55-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="9ab55-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="9ab55-121">Флаг, который показывает, следует ли исключить созданную версию изображения из последней версии.</span><span class="sxs-lookup"><span data-stu-id="9ab55-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="9ab55-122">Опустить значение по умолчанию (false).</span><span class="sxs-lookup"><span data-stu-id="9ab55-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="9ab55-123">-GalleryImageId</span></span>
<span data-ttu-id="9ab55-124">ИД ресурса коллекции общих изображений.</span><span class="sxs-lookup"><span data-stu-id="9ab55-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="9ab55-125">-ImageId</span></span>
<span data-ttu-id="9ab55-126">ИД ресурса изображения управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="9ab55-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-127">-Location</span><span class="sxs-lookup"><span data-stu-id="9ab55-127">-Location</span></span>
<span data-ttu-id="9ab55-128">Расположение изображения в Azure должно совпадать, если изображение уже существует.</span><span class="sxs-lookup"><span data-stu-id="9ab55-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="9ab55-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="9ab55-130">Распространение в качестве изображения управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="9ab55-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="9ab55-131">-ReplicationRegion</span></span>
<span data-ttu-id="9ab55-132">Список областей, в которые будет реплицироваться изображение.</span><span class="sxs-lookup"><span data-stu-id="9ab55-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="9ab55-133">-RunOutputName</span></span>
<span data-ttu-id="9ab55-134">Имя, которое будет использоваться для связанной runOutput.</span><span class="sxs-lookup"><span data-stu-id="9ab55-134">The name to be used for the associated RunOutput.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="9ab55-135">-SharedImageDistributor</span></span>
<span data-ttu-id="9ab55-136">Распространение с помощью коллекции общих изображений.</span><span class="sxs-lookup"><span data-stu-id="9ab55-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9ab55-137">-StorageAccountType</span></span>
<span data-ttu-id="9ab55-138">Тип учетной записи хранения для хранения общего изображения.</span><span class="sxs-lookup"><span data-stu-id="9ab55-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="9ab55-139">Опустить значение по умолчанию (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="9ab55-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="9ab55-140">-VhdDistributor</span></span>
<span data-ttu-id="9ab55-141">Распространение через VHD в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9ab55-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ab55-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab55-142">CommonParameters</span></span>
<span data-ttu-id="9ab55-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab55-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab55-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ab55-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab55-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ab55-145">INPUTS</span></span>

## <span data-ttu-id="9ab55-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ab55-146">OUTPUTS</span></span>

### <span data-ttu-id="9ab55-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="9ab55-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="9ab55-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ab55-148">NOTES</span></span>

<span data-ttu-id="9ab55-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9ab55-149">ALIASES</span></span>

## <span data-ttu-id="9ab55-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ab55-150">RELATED LINKS</span></span>

