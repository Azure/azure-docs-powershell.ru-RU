---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397620"
---
# <span data-ttu-id="ceba8-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="ceba8-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="ceba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceba8-102">SYNOPSIS</span></span>
<span data-ttu-id="ceba8-103">Обновление определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="ceba8-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="ceba8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ceba8-104">SYNTAX</span></span>

### <span data-ttu-id="ceba8-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ceba8-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceba8-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ceba8-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ceba8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ceba8-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ceba8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceba8-108">DESCRIPTION</span></span>
<span data-ttu-id="ceba8-109">Обновление определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="ceba8-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="ceba8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ceba8-110">EXAMPLES</span></span>

### <span data-ttu-id="ceba8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ceba8-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="ceba8-112">Обновление определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="ceba8-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="ceba8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceba8-113">PARAMETERS</span></span>

### <span data-ttu-id="ceba8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ceba8-114">-AsJob</span></span>
<span data-ttu-id="ceba8-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ceba8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ceba8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceba8-116">-DefaultProfile</span></span>
<span data-ttu-id="ceba8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ceba8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceba8-118">-Description</span><span class="sxs-lookup"><span data-stu-id="ceba8-118">-Description</span></span>
<span data-ttu-id="ceba8-119">Описание ресурса определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="ceba8-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="ceba8-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="ceba8-120">-DisallowedDiskType</span></span>
<span data-ttu-id="ceba8-121">Диски всех этих типов.</span><span class="sxs-lookup"><span data-stu-id="ceba8-121">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceba8-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="ceba8-122">-EndOfLifeDate</span></span>
<span data-ttu-id="ceba8-123">Дата окончания жизненного времени в определении изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="ceba8-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="ceba8-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="ceba8-124">-Eula</span></span>
<span data-ttu-id="ceba8-125">Соглашение Eula об определении изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="ceba8-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="ceba8-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="ceba8-126">-GalleryName</span></span>
<span data-ttu-id="ceba8-127">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="ceba8-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="ceba8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ceba8-128">-InputObject</span></span>
<span data-ttu-id="ceba8-129">Объект определения изображения в коллекции PS.</span><span class="sxs-lookup"><span data-stu-id="ceba8-129">The PS Gallery Image Definition Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceba8-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="ceba8-130">-MaximumMemory</span></span>
<span data-ttu-id="ceba8-131">Максимальное значение рекомендуемой памяти</span><span class="sxs-lookup"><span data-stu-id="ceba8-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="ceba8-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="ceba8-132">-MaximumVCPU</span></span>
<span data-ttu-id="ceba8-133">Максимальное значение рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="ceba8-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ceba8-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="ceba8-134">-MinimumMemory</span></span>
<span data-ttu-id="ceba8-135">Минимальная рекомендуемая память</span><span class="sxs-lookup"><span data-stu-id="ceba8-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="ceba8-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="ceba8-136">-MinimumVCPU</span></span>
<span data-ttu-id="ceba8-137">Минимальное рекомендуемое ядро ЦП</span><span class="sxs-lookup"><span data-stu-id="ceba8-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ceba8-138">-Name</span><span class="sxs-lookup"><span data-stu-id="ceba8-138">-Name</span></span>
<span data-ttu-id="ceba8-139">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="ceba8-139">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceba8-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="ceba8-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="ceba8-141">URI заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="ceba8-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="ceba8-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="ceba8-142">-PurchasePlanName</span></span>
<span data-ttu-id="ceba8-143">ИД плана покупки.</span><span class="sxs-lookup"><span data-stu-id="ceba8-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ceba8-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="ceba8-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="ceba8-145">ИД продукта для плана покупки.</span><span class="sxs-lookup"><span data-stu-id="ceba8-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ceba8-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ceba8-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="ceba8-147">ИД издателя для плана покупки.</span><span class="sxs-lookup"><span data-stu-id="ceba8-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ceba8-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="ceba8-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="ceba8-149">URI заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="ceba8-149">The release note uri.</span></span>

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

### <span data-ttu-id="ceba8-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceba8-150">-ResourceGroupName</span></span>
<span data-ttu-id="ceba8-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ceba8-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="ceba8-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ceba8-152">-ResourceId</span></span>
<span data-ttu-id="ceba8-153">ИД ресурса для определения изображения</span><span class="sxs-lookup"><span data-stu-id="ceba8-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="ceba8-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="ceba8-154">-Tag</span></span>
<span data-ttu-id="ceba8-155">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="ceba8-155">Resource tags</span></span>

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

### <span data-ttu-id="ceba8-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceba8-156">-Confirm</span></span>
<span data-ttu-id="ceba8-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceba8-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceba8-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceba8-158">-WhatIf</span></span>
<span data-ttu-id="ceba8-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceba8-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceba8-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ceba8-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceba8-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceba8-161">CommonParameters</span></span>
<span data-ttu-id="ceba8-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceba8-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceba8-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ceba8-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceba8-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ceba8-164">INPUTS</span></span>

### <span data-ttu-id="ceba8-165">System.String</span><span class="sxs-lookup"><span data-stu-id="ceba8-165">System.String</span></span>

### <span data-ttu-id="ceba8-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="ceba8-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="ceba8-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="ceba8-167">System.DateTime</span></span>

### <span data-ttu-id="ceba8-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ceba8-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ceba8-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ceba8-169">System.Int32</span></span>

### <span data-ttu-id="ceba8-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ceba8-170">System.String[]</span></span>

## <span data-ttu-id="ceba8-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ceba8-171">OUTPUTS</span></span>

### <span data-ttu-id="ceba8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="ceba8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="ceba8-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ceba8-173">NOTES</span></span>

## <span data-ttu-id="ceba8-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ceba8-174">RELATED LINKS</span></span>
