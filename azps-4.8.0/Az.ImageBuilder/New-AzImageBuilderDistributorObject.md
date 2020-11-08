---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079044"
---
# <span data-ttu-id="1b178-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="1b178-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="1b178-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b178-102">SYNOPSIS</span></span>
<span data-ttu-id="1b178-103">Универсальный объект распределения</span><span class="sxs-lookup"><span data-stu-id="1b178-103">Generic distribution object</span></span>

## <span data-ttu-id="1b178-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b178-104">SYNTAX</span></span>

### <span data-ttu-id="1b178-105">ManagedImageDistributor (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b178-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="1b178-106">SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="1b178-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="1b178-107">VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="1b178-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="1b178-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b178-108">DESCRIPTION</span></span>
<span data-ttu-id="1b178-109">Универсальный объект распределения</span><span class="sxs-lookup"><span data-stu-id="1b178-109">Generic distribution object</span></span>

## <span data-ttu-id="1b178-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b178-110">EXAMPLES</span></span>

### <span data-ttu-id="1b178-111">Пример 1: создание распространителя управляемых изображений</span><span class="sxs-lookup"><span data-stu-id="1b178-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="1b178-112">Эта команда создает управляемый распространитель изображений.</span><span class="sxs-lookup"><span data-stu-id="1b178-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="1b178-113">Пример 2: создание распространителя виртуальных жестких дисков</span><span class="sxs-lookup"><span data-stu-id="1b178-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="1b178-114">Эта команда создает распространитель VHD.</span><span class="sxs-lookup"><span data-stu-id="1b178-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="1b178-115">Пример 3: создание распространителя общих изображений</span><span class="sxs-lookup"><span data-stu-id="1b178-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="1b178-116">Эта команда создает распространитель общих изображений.</span><span class="sxs-lookup"><span data-stu-id="1b178-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="1b178-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b178-117">PARAMETERS</span></span>

### <span data-ttu-id="1b178-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="1b178-118">-ArtifactTag</span></span>
<span data-ttu-id="1b178-119">Теги, которые будут применяться к артефакту после его создания или обновления распространителем.</span><span class="sxs-lookup"><span data-stu-id="1b178-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

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

### <span data-ttu-id="1b178-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="1b178-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="1b178-121">Флаг, указывающий, следует ли исключить созданную версию изображения из последней.</span><span class="sxs-lookup"><span data-stu-id="1b178-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="1b178-122">Опустить, чтобы использовать значение по умолчанию (false).</span><span class="sxs-lookup"><span data-stu-id="1b178-122">Omit to use the default (false).</span></span>

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

### <span data-ttu-id="1b178-123">-GalleryImageId</span><span class="sxs-lookup"><span data-stu-id="1b178-123">-GalleryImageId</span></span>
<span data-ttu-id="1b178-124">Идентификатор ресурса для изображения коллекции общих изображений.</span><span class="sxs-lookup"><span data-stu-id="1b178-124">Resource Id of the Shared Image Gallery image.</span></span>

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

### <span data-ttu-id="1b178-125">-ImageId</span><span class="sxs-lookup"><span data-stu-id="1b178-125">-ImageId</span></span>
<span data-ttu-id="1b178-126">Идентификатор ресурса управляемого образа диска.</span><span class="sxs-lookup"><span data-stu-id="1b178-126">Resource Id of the Managed Disk Image.</span></span>

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

### <span data-ttu-id="1b178-127">-Location</span><span class="sxs-lookup"><span data-stu-id="1b178-127">-Location</span></span>
<span data-ttu-id="1b178-128">Расположение Azure для изображения, должно быть сопоставлено, если изображение уже существует.</span><span class="sxs-lookup"><span data-stu-id="1b178-128">Azure location for the image, should match if image already exists.</span></span>

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

### <span data-ttu-id="1b178-129">-ManagedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="1b178-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="1b178-130">Распространение в виде управляемого образа диска.</span><span class="sxs-lookup"><span data-stu-id="1b178-130">Distribute as a Managed Disk Image.</span></span>

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

### <span data-ttu-id="1b178-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="1b178-131">-ReplicationRegion</span></span>
<span data-ttu-id="1b178-132">Список регионов, на который будет проводиться репликация изображения.</span><span class="sxs-lookup"><span data-stu-id="1b178-132">A list of regions that the image will be replicated to.</span></span>

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

### <span data-ttu-id="1b178-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="1b178-133">-RunOutputName</span></span>
<span data-ttu-id="1b178-134">Имя, которое будет использоваться для связанного RunOutput.</span><span class="sxs-lookup"><span data-stu-id="1b178-134">The name to be used for the associated RunOutput.</span></span>

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

### <span data-ttu-id="1b178-135">-SharedImageDistributor</span><span class="sxs-lookup"><span data-stu-id="1b178-135">-SharedImageDistributor</span></span>
<span data-ttu-id="1b178-136">Распространение через коллекцию общих изображений.</span><span class="sxs-lookup"><span data-stu-id="1b178-136">Distribute via Shared Image Gallery.</span></span>

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

### <span data-ttu-id="1b178-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="1b178-137">-StorageAccountType</span></span>
<span data-ttu-id="1b178-138">Тип учетной записи хранения, которая будет использоваться для хранения общего образа.</span><span class="sxs-lookup"><span data-stu-id="1b178-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="1b178-139">Опустить, чтобы использовать значение по умолчанию (Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="1b178-139">Omit to use the default (Standard_LRS).</span></span>

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

### <span data-ttu-id="1b178-140">-VhdDistributor</span><span class="sxs-lookup"><span data-stu-id="1b178-140">-VhdDistributor</span></span>
<span data-ttu-id="1b178-141">Распространение по ВИРТУАЛЬным носителям в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1b178-141">Distribute via VHD in a storage account.</span></span>

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

### <span data-ttu-id="1b178-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b178-142">CommonParameters</span></span>
<span data-ttu-id="1b178-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b178-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b178-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b178-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b178-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b178-145">INPUTS</span></span>

## <span data-ttu-id="1b178-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b178-146">OUTPUTS</span></span>

### <span data-ttu-id="1b178-147">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. Api20200214. IImageTemplateDistributor</span><span class="sxs-lookup"><span data-stu-id="1b178-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="1b178-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b178-148">NOTES</span></span>

<span data-ttu-id="1b178-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="1b178-149">ALIASES</span></span>

## <span data-ttu-id="1b178-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b178-150">RELATED LINKS</span></span>

