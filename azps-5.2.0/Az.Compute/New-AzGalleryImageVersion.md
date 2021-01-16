---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409076"
---
# <span data-ttu-id="f28fc-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f28fc-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="f28fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f28fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f28fc-103">Создание версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="f28fc-103">Create a gallery image version.</span></span>

## <span data-ttu-id="f28fc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f28fc-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f28fc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f28fc-105">DESCRIPTION</span></span>
<span data-ttu-id="f28fc-106">Создание версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="f28fc-106">Create a gallery image version.</span></span>

## <span data-ttu-id="f28fc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f28fc-107">EXAMPLES</span></span>

### <span data-ttu-id="f28fc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f28fc-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="f28fc-109">Создание версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="f28fc-109">Create a gallery image version.</span></span>

### <span data-ttu-id="f28fc-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f28fc-110">Example 2</span></span>
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

<span data-ttu-id="f28fc-111">Создайте версию изображения коллекции с шифрованием образа диска.</span><span class="sxs-lookup"><span data-stu-id="f28fc-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="f28fc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f28fc-112">PARAMETERS</span></span>

### <span data-ttu-id="f28fc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f28fc-113">-AsJob</span></span>
<span data-ttu-id="f28fc-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f28fc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f28fc-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="f28fc-115">-DataDiskImage</span></span>
<span data-ttu-id="f28fc-116">Изображения на диске данных.</span><span class="sxs-lookup"><span data-stu-id="f28fc-116">Data disk images.</span></span>   <span data-ttu-id="f28fc-117">Например: @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="f28fc-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="f28fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f28fc-118">-DefaultProfile</span></span>
<span data-ttu-id="f28fc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f28fc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f28fc-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f28fc-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="f28fc-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="f28fc-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="f28fc-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="f28fc-122">-GalleryName</span></span>
<span data-ttu-id="f28fc-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="f28fc-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="f28fc-124">-Location</span><span class="sxs-lookup"><span data-stu-id="f28fc-124">-Location</span></span>
<span data-ttu-id="f28fc-125">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="f28fc-125">Resource location</span></span>

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

### <span data-ttu-id="f28fc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f28fc-126">-Name</span></span>
<span data-ttu-id="f28fc-127">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="f28fc-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="f28fc-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="f28fc-128">-OSDiskImage</span></span>
<span data-ttu-id="f28fc-129">Изображение диска ОС, например @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span><span class="sxs-lookup"><span data-stu-id="f28fc-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="f28fc-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="f28fc-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="f28fc-131">Дата окончания жизненного срока версии коллекции изображений.</span><span class="sxs-lookup"><span data-stu-id="f28fc-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="f28fc-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="f28fc-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="f28fc-133">Если она установлена, виртуальные машины, развернутые из последней версии определения изображения, не будут использовать эту версию изображения.</span><span class="sxs-lookup"><span data-stu-id="f28fc-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="f28fc-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="f28fc-134">-ReplicaCount</span></span>
<span data-ttu-id="f28fc-135">Количество копий версии изображения, созда необходимой для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="f28fc-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="f28fc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f28fc-136">-ResourceGroupName</span></span>
<span data-ttu-id="f28fc-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f28fc-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="f28fc-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="f28fc-138">-SourceImageId</span></span>
<span data-ttu-id="f28fc-139">Код изображения, на котором будет создана версия изображения.</span><span class="sxs-lookup"><span data-stu-id="f28fc-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="f28fc-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f28fc-140">-StorageAccountType</span></span>
<span data-ttu-id="f28fc-141">Определяет тип учетной записи хранения, которая будет использоваться для хранения изображения.</span><span class="sxs-lookup"><span data-stu-id="f28fc-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="f28fc-142">Это свойство не может быть updatable.</span><span class="sxs-lookup"><span data-stu-id="f28fc-142">This property is not updatable.</span></span> <span data-ttu-id="f28fc-143">Доступны значения Standard_LRS, Standard_ZRS и Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="f28fc-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="f28fc-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="f28fc-144">-Tag</span></span>
<span data-ttu-id="f28fc-145">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="f28fc-145">Resource tags</span></span>

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

### <span data-ttu-id="f28fc-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="f28fc-146">-TargetRegion</span></span>
<span data-ttu-id="f28fc-147">Целевые области, в которые будет реплицирована версия изображения.</span><span class="sxs-lookup"><span data-stu-id="f28fc-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="f28fc-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f28fc-148">-Confirm</span></span>
<span data-ttu-id="f28fc-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f28fc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f28fc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f28fc-150">-WhatIf</span></span>
<span data-ttu-id="f28fc-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f28fc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f28fc-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f28fc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f28fc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f28fc-153">CommonParameters</span></span>
<span data-ttu-id="f28fc-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f28fc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f28fc-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f28fc-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f28fc-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f28fc-156">INPUTS</span></span>

### <span data-ttu-id="f28fc-157">System.String</span><span class="sxs-lookup"><span data-stu-id="f28fc-157">System.String</span></span>

### <span data-ttu-id="f28fc-158">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f28fc-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f28fc-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f28fc-159">System.Int32</span></span>

### <span data-ttu-id="f28fc-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f28fc-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f28fc-161">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="f28fc-161">System.DateTime</span></span>

### <span data-ttu-id="f28fc-162">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="f28fc-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="f28fc-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f28fc-163">OUTPUTS</span></span>

### <span data-ttu-id="f28fc-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f28fc-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="f28fc-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f28fc-165">NOTES</span></span>

## <span data-ttu-id="f28fc-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f28fc-166">RELATED LINKS</span></span>