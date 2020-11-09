---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 8ef13dd067cd0cf1161e3aa58b52a961fe90a949
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247069"
---
# <span data-ttu-id="3a3e7-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3a3e7-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="3a3e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a3e7-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3e7-103">Создайте версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-103">Create a gallery image version.</span></span>

## <span data-ttu-id="3a3e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a3e7-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a3e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a3e7-105">DESCRIPTION</span></span>
<span data-ttu-id="3a3e7-106">Создайте версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-106">Create a gallery image version.</span></span>

## <span data-ttu-id="3a3e7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a3e7-107">EXAMPLES</span></span>

### <span data-ttu-id="3a3e7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a3e7-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="3a3e7-109">Создайте версию картинки из коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-109">Create a gallery image version.</span></span>

### <span data-ttu-id="3a3e7-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3a3e7-110">Example 2</span></span>
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

<span data-ttu-id="3a3e7-111">Создайте версию с изображением коллекции с шифрованием дисков.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="3a3e7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a3e7-112">PARAMETERS</span></span>

### <span data-ttu-id="3a3e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a3e7-113">-AsJob</span></span>
<span data-ttu-id="3a3e7-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3a3e7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a3e7-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="3a3e7-115">-DataDiskImage</span></span>
<span data-ttu-id="3a3e7-116">Образы дисков данных.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-116">Data disk images.</span></span>   <span data-ttu-id="3a3e7-117">Например, @ {Source = @ {ID =<source_id>}; LUN = 1; SizeInGB = 100; HostCaching = "только для чтения"}</span><span class="sxs-lookup"><span data-stu-id="3a3e7-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="3a3e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3e7-118">-DefaultProfile</span></span>
<span data-ttu-id="3a3e7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a3e7-120">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3a3e7-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="3a3e7-121">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="3a3e7-122">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="3a3e7-122">-GalleryName</span></span>
<span data-ttu-id="3a3e7-123">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="3a3e7-124">-Location</span><span class="sxs-lookup"><span data-stu-id="3a3e7-124">-Location</span></span>
<span data-ttu-id="3a3e7-125">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="3a3e7-125">Resource location</span></span>

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

### <span data-ttu-id="3a3e7-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a3e7-126">-Name</span></span>
<span data-ttu-id="3a3e7-127">Имя версии изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="3a3e7-128">-OSDiskImage</span><span class="sxs-lookup"><span data-stu-id="3a3e7-128">-OSDiskImage</span></span>
<span data-ttu-id="3a3e7-129">Образ диска ОС, например @ {Source = @ {ID =<source_id>}; SizeInGB = 100; HostCaching = "только для чтения"}</span><span class="sxs-lookup"><span data-stu-id="3a3e7-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

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

### <span data-ttu-id="3a3e7-130">-PublishingProfileEndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="3a3e7-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="3a3e7-131">Дата окончания срока действия версии изображения в галерее.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="3a3e7-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="3a3e7-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="3a3e7-133">Если задано значение, виртуальные машины, развернутые из последней версии определения образа, не будут использовать эту версию изображения.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="3a3e7-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3a3e7-134">-ReplicaCount</span></span>
<span data-ttu-id="3a3e7-135">Число реплик для версии изображения, создаваемой для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="3a3e7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3e7-136">-ResourceGroupName</span></span>
<span data-ttu-id="3a3e7-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a3e7-138">-SourceImageId</span><span class="sxs-lookup"><span data-stu-id="3a3e7-138">-SourceImageId</span></span>
<span data-ttu-id="3a3e7-139">Идентификатор исходного изображения, из которого будет создана версия изображения.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="3a3e7-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3a3e7-140">-StorageAccountType</span></span>
<span data-ttu-id="3a3e7-141">Указывает тип учетной записи хранения, которая будет использоваться для хранения изображения.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="3a3e7-142">Это свойство не является обновляемым.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-142">This property is not updatable.</span></span> <span data-ttu-id="3a3e7-143">Доступные значения: Standard_LRS, Standard_ZRS и Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-143">Available values are Standard_LRS, Standard_ZRS and Premium_LRS.</span></span>

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

### <span data-ttu-id="3a3e7-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="3a3e7-144">-Tag</span></span>
<span data-ttu-id="3a3e7-145">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="3a3e7-145">Resource tags</span></span>

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

### <span data-ttu-id="3a3e7-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="3a3e7-146">-TargetRegion</span></span>
<span data-ttu-id="3a3e7-147">Целевые области, на которые должна быть реплицирована версия изображения.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="3a3e7-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a3e7-148">-Confirm</span></span>
<span data-ttu-id="3a3e7-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a3e7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a3e7-150">-WhatIf</span></span>
<span data-ttu-id="3a3e7-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a3e7-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a3e7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3e7-153">CommonParameters</span></span>
<span data-ttu-id="3a3e7-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3e7-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a3e7-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3e7-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a3e7-156">INPUTS</span></span>

### <span data-ttu-id="3a3e7-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3a3e7-157">System.String</span></span>

### <span data-ttu-id="3a3e7-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3a3e7-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3a3e7-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3a3e7-159">System.Int32</span></span>

### <span data-ttu-id="3a3e7-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3a3e7-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3a3e7-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="3a3e7-161">System.DateTime</span></span>

### <span data-ttu-id="3a3e7-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="3a3e7-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="3a3e7-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a3e7-163">OUTPUTS</span></span>

### <span data-ttu-id="3a3e7-164">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="3a3e7-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="3a3e7-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a3e7-165">NOTES</span></span>

## <span data-ttu-id="3a3e7-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a3e7-166">RELATED LINKS</span></span>