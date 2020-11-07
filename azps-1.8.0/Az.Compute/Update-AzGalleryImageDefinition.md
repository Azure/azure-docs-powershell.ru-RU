---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 338e65e4795f3b676a1f88e8a8281a41aee5a0c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901069"
---
# <span data-ttu-id="e6895-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="e6895-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="e6895-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6895-102">SYNOPSIS</span></span>
<span data-ttu-id="e6895-103">Обновите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6895-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="e6895-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6895-104">SYNTAX</span></span>

### <span data-ttu-id="e6895-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6895-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6895-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e6895-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6895-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e6895-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6895-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6895-108">DESCRIPTION</span></span>
<span data-ttu-id="e6895-109">Обновите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6895-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="e6895-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6895-110">EXAMPLES</span></span>

### <span data-ttu-id="e6895-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6895-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="e6895-112">Обновите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6895-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="e6895-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6895-113">PARAMETERS</span></span>

### <span data-ttu-id="e6895-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6895-114">-AsJob</span></span>
<span data-ttu-id="e6895-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e6895-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6895-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6895-116">-DefaultProfile</span></span>
<span data-ttu-id="e6895-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6895-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6895-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="e6895-118">-Description</span></span>
<span data-ttu-id="e6895-119">Описание ресурса, в котором определена коллекция изображений.</span><span class="sxs-lookup"><span data-stu-id="e6895-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="e6895-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="e6895-120">-DisallowedDiskType</span></span>
<span data-ttu-id="e6895-121">Недопустимые типы дисков.</span><span class="sxs-lookup"><span data-stu-id="e6895-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="e6895-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="e6895-122">-EndOfLifeDate</span></span>
<span data-ttu-id="e6895-123">Дата окончания срока действия определения изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="e6895-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="e6895-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="e6895-124">-Eula</span></span>
<span data-ttu-id="e6895-125">Лицензионное соглашение для определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6895-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="e6895-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="e6895-126">-GalleryName</span></span>
<span data-ttu-id="e6895-127">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6895-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="e6895-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6895-128">-InputObject</span></span>
<span data-ttu-id="e6895-129">Объект определения изображения в коллекции PS.</span><span class="sxs-lookup"><span data-stu-id="e6895-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="e6895-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="e6895-130">-MaximumMemory</span></span>
<span data-ttu-id="e6895-131">Максимум рекомендованной памяти</span><span class="sxs-lookup"><span data-stu-id="e6895-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="e6895-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="e6895-132">-MaximumVCPU</span></span>
<span data-ttu-id="e6895-133">Максимум рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="e6895-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="e6895-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="e6895-134">-MinimumMemory</span></span>
<span data-ttu-id="e6895-135">Минимальная рекомендуемая память</span><span class="sxs-lookup"><span data-stu-id="e6895-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="e6895-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="e6895-136">-MinimumVCPU</span></span>
<span data-ttu-id="e6895-137">Минимум рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="e6895-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="e6895-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6895-138">-Name</span></span>
<span data-ttu-id="e6895-139">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="e6895-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="e6895-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="e6895-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="e6895-141">URI заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="e6895-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="e6895-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="e6895-142">-PurchasePlanName</span></span>
<span data-ttu-id="e6895-143">ИДЕНТИФИКАТОР плана покупок.</span><span class="sxs-lookup"><span data-stu-id="e6895-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="e6895-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="e6895-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="e6895-145">КОД продукта для плана заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="e6895-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="e6895-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="e6895-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="e6895-147">Идентификатор издателя для плана покупки.</span><span class="sxs-lookup"><span data-stu-id="e6895-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="e6895-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="e6895-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="e6895-149">URI заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="e6895-149">The release note uri.</span></span>

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

### <span data-ttu-id="e6895-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6895-150">-ResourceGroupName</span></span>
<span data-ttu-id="e6895-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6895-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6895-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6895-152">-ResourceId</span></span>
<span data-ttu-id="e6895-153">Идентификатор ресурса для определения изображения</span><span class="sxs-lookup"><span data-stu-id="e6895-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="e6895-154">-Тег</span><span class="sxs-lookup"><span data-stu-id="e6895-154">-Tag</span></span>
<span data-ttu-id="e6895-155">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="e6895-155">Resource tags</span></span>

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

### <span data-ttu-id="e6895-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6895-156">-Confirm</span></span>
<span data-ttu-id="e6895-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6895-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6895-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6895-158">-WhatIf</span></span>
<span data-ttu-id="e6895-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6895-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6895-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6895-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6895-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6895-161">CommonParameters</span></span>
<span data-ttu-id="e6895-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6895-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6895-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6895-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6895-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6895-164">INPUTS</span></span>

### <span data-ttu-id="e6895-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e6895-165">System.String</span></span>

### <span data-ttu-id="e6895-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="e6895-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="e6895-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="e6895-167">System.DateTime</span></span>

### <span data-ttu-id="e6895-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6895-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e6895-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e6895-169">System.Int32</span></span>

### <span data-ttu-id="e6895-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="e6895-170">System.String[]</span></span>

## <span data-ttu-id="e6895-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6895-171">OUTPUTS</span></span>

### <span data-ttu-id="e6895-172">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="e6895-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="e6895-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6895-173">NOTES</span></span>

## <span data-ttu-id="e6895-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6895-174">RELATED LINKS</span></span>
