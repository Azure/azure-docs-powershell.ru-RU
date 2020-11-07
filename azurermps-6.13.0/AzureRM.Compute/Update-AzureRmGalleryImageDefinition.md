---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 445029c41e27cce14bff2ac14d826adf28f3c9ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731981"
---
# <span data-ttu-id="26077-101">Update-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="26077-101">Update-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="26077-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26077-102">SYNOPSIS</span></span>
<span data-ttu-id="26077-103">Обновите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="26077-103">Update a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26077-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26077-104">SYNTAX</span></span>

### <span data-ttu-id="26077-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26077-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26077-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="26077-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26077-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="26077-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26077-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26077-108">DESCRIPTION</span></span>
<span data-ttu-id="26077-109">Обновите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="26077-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="26077-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26077-110">EXAMPLES</span></span>

### <span data-ttu-id="26077-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26077-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="26077-112">Обновите определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="26077-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="26077-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26077-113">PARAMETERS</span></span>

### <span data-ttu-id="26077-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26077-114">-AsJob</span></span>
<span data-ttu-id="26077-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="26077-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26077-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26077-116">-DefaultProfile</span></span>
<span data-ttu-id="26077-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26077-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26077-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="26077-118">-Description</span></span>
<span data-ttu-id="26077-119">Описание ресурса, в котором определена коллекция изображений.</span><span class="sxs-lookup"><span data-stu-id="26077-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="26077-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="26077-120">-DisallowedDiskType</span></span>
<span data-ttu-id="26077-121">Недопустимые типы дисков.</span><span class="sxs-lookup"><span data-stu-id="26077-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="26077-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="26077-122">-EndOfLifeDate</span></span>
<span data-ttu-id="26077-123">Дата окончания срока действия определения изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="26077-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="26077-124">-EULA</span><span class="sxs-lookup"><span data-stu-id="26077-124">-Eula</span></span>
<span data-ttu-id="26077-125">Лицензионное соглашение для определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="26077-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="26077-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="26077-126">-GalleryName</span></span>
<span data-ttu-id="26077-127">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="26077-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="26077-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26077-128">-InputObject</span></span>
<span data-ttu-id="26077-129">Объект определения изображения в коллекции PS.</span><span class="sxs-lookup"><span data-stu-id="26077-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="26077-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="26077-130">-MaximumMemory</span></span>
<span data-ttu-id="26077-131">Максимум рекомендованной памяти</span><span class="sxs-lookup"><span data-stu-id="26077-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="26077-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="26077-132">-MaximumVCPU</span></span>
<span data-ttu-id="26077-133">Максимум рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="26077-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="26077-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="26077-134">-MinimumMemory</span></span>
<span data-ttu-id="26077-135">Минимальная рекомендуемая память</span><span class="sxs-lookup"><span data-stu-id="26077-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="26077-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="26077-136">-MinimumVCPU</span></span>
<span data-ttu-id="26077-137">Минимум рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="26077-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="26077-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26077-138">-Name</span></span>
<span data-ttu-id="26077-139">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="26077-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="26077-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="26077-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="26077-141">URI заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="26077-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="26077-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="26077-142">-PurchasePlanName</span></span>
<span data-ttu-id="26077-143">ИДЕНТИФИКАТОР плана покупок.</span><span class="sxs-lookup"><span data-stu-id="26077-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="26077-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="26077-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="26077-145">КОД продукта для плана заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="26077-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="26077-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="26077-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="26077-147">Идентификатор издателя для плана покупки.</span><span class="sxs-lookup"><span data-stu-id="26077-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="26077-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="26077-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="26077-149">URI заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="26077-149">The release note uri.</span></span>

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

### <span data-ttu-id="26077-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26077-150">-ResourceGroupName</span></span>
<span data-ttu-id="26077-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26077-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="26077-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26077-152">-ResourceId</span></span>
<span data-ttu-id="26077-153">Идентификатор ресурса для определения изображения</span><span class="sxs-lookup"><span data-stu-id="26077-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="26077-154">-Тег</span><span class="sxs-lookup"><span data-stu-id="26077-154">-Tag</span></span>
<span data-ttu-id="26077-155">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="26077-155">Resource tags</span></span>

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

### <span data-ttu-id="26077-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26077-156">-Confirm</span></span>
<span data-ttu-id="26077-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26077-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26077-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26077-158">-WhatIf</span></span>
<span data-ttu-id="26077-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26077-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26077-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26077-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26077-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26077-161">CommonParameters</span></span>
<span data-ttu-id="26077-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26077-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26077-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26077-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26077-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26077-164">INPUTS</span></span>

### <span data-ttu-id="26077-165">System. String</span><span class="sxs-lookup"><span data-stu-id="26077-165">System.String</span></span>

### <span data-ttu-id="26077-166">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="26077-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="26077-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="26077-167">System.DateTime</span></span>

### <span data-ttu-id="26077-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="26077-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="26077-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="26077-169">System.Int32</span></span>

### <span data-ttu-id="26077-170">System. String []</span><span class="sxs-lookup"><span data-stu-id="26077-170">System.String[]</span></span>

## <span data-ttu-id="26077-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26077-171">OUTPUTS</span></span>

### <span data-ttu-id="26077-172">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="26077-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="26077-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="26077-173">NOTES</span></span>

## <span data-ttu-id="26077-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26077-174">RELATED LINKS</span></span>
