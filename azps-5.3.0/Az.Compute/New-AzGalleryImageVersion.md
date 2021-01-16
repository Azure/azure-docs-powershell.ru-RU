---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509102"
---
# <span data-ttu-id="1363a-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1363a-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="1363a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1363a-102">SYNOPSIS</span></span>
<span data-ttu-id="1363a-103">Создание версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="1363a-103">Create a gallery image version.</span></span>

## <span data-ttu-id="1363a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1363a-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1363a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1363a-105">DESCRIPTION</span></span>
<span data-ttu-id="1363a-106">Создание версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="1363a-106">Create a gallery image version.</span></span>

## <span data-ttu-id="1363a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1363a-107">EXAMPLES</span></span>

### <span data-ttu-id="1363a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1363a-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="1363a-109">Создание версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="1363a-109">Create a gallery image version.</span></span>

### <span data-ttu-id="1363a-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1363a-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="1363a-111">Создайте версию изображения коллекции с шифрованием образа диска.</span><span class="sxs-lookup"><span data-stu-id="1363a-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="1363a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1363a-112">PARAMETERS</span></span>

### <span data-ttu-id="1363a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1363a-113">-AsJob</span></span>
<span data-ttu-id="1363a-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1363a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1363a-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="1363a-115">-DataDiskImage</span></span>
<span data-ttu-id="1363a-116">Изображения на диске данных.</span><span class="sxs-lookup"><span data-stu-id="1363a-116">Data disk images.</span></span>   <span data-ttu-id="1363a-117">Например: @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="1363a-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1363a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1363a-118">-DefaultProfile</span></span>
<span data-ttu-id="1363a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1363a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1363a-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="1363a-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="1363a-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="1363a-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="1363a-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="1363a-122">-GalleryName</span></span>
<span data-ttu-id="1363a-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="1363a-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="1363a-124">-Location</span><span class="sxs-lookup"><span data-stu-id="1363a-124">-Location</span></span>
<span data-ttu-id="1363a-125">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="1363a-125">Resource location</span></span>

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

### <span data-ttu-id="1363a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1363a-126">-Name</span></span>
<span data-ttu-id="1363a-127">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="1363a-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="1363a-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="1363a-128">-OSDiskImage</span></span>
<span data-ttu-id="1363a-129">Изображение диска ОС, например @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="1363a-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1363a-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="1363a-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="1363a-131">Дата окончания жизненного срока версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="1363a-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="1363a-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="1363a-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="1363a-133">Если она установлена, виртуальные машины, развернутые из последней версии определения изображения, не будут использовать эту версию изображения.</span><span class="sxs-lookup"><span data-stu-id="1363a-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="1363a-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="1363a-134">-ReplicaCount</span></span>
<span data-ttu-id="1363a-135">Количество копий версии изображения, созда необходимой для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="1363a-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="1363a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1363a-136">-ResourceGroupName</span></span>
<span data-ttu-id="1363a-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1363a-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="1363a-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="1363a-138">-SourceImageId</span></span>
<span data-ttu-id="1363a-139">Код изображения, на котором будет создана версия изображения.</span><span class="sxs-lookup"><span data-stu-id="1363a-139">The ID of the source image from which the Image Version is going to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1363a-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="1363a-140">-StorageAccountType</span></span>
<span data-ttu-id="1363a-141">Определяет тип учетной записи хранения, которая будет использоваться для хранения изображения.</span><span class="sxs-lookup"><span data-stu-id="1363a-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="1363a-142">Это свойство не является updatable (updatable).</span><span class="sxs-lookup"><span data-stu-id="1363a-142">This property is not updatable.</span></span> <span data-ttu-id="1363a-143">Доступны значения Standard_LRS, Standard_ZRS и Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="1363a-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1363a-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="1363a-144">-Tag</span></span>
<span data-ttu-id="1363a-145">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="1363a-145">Resource tags</span></span>

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

### <span data-ttu-id="1363a-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="1363a-146">-TargetRegion</span></span>
<span data-ttu-id="1363a-147">Целевые области, в которые будет реплицирована версия изображения.</span><span class="sxs-lookup"><span data-stu-id="1363a-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="1363a-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1363a-148">-Confirm</span></span>
<span data-ttu-id="1363a-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1363a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1363a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1363a-150">-WhatIf</span></span>
<span data-ttu-id="1363a-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1363a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1363a-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1363a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1363a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1363a-153">CommonParameters</span></span>
<span data-ttu-id="1363a-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1363a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1363a-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1363a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1363a-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1363a-156">INPUTS</span></span>

### <span data-ttu-id="1363a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="1363a-157">System.String</span></span>

### <span data-ttu-id="1363a-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1363a-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1363a-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1363a-159">System.Int32</span></span>

### <span data-ttu-id="1363a-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1363a-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1363a-161">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="1363a-161">System.DateTime</span></span>

### <span data-ttu-id="1363a-162">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="1363a-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="1363a-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1363a-163">OUTPUTS</span></span>

### <span data-ttu-id="1363a-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1363a-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="1363a-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1363a-165">NOTES</span></span>

## <span data-ttu-id="1363a-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1363a-166">RELATED LINKS</span></span>
