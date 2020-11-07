---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: 7b2a0399be6412c3e33754a8e91b1a6120b5ec9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721852"
---
# <span data-ttu-id="fbc33-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="fbc33-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="fbc33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbc33-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc33-103">Создайте определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="fbc33-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="fbc33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbc33-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>]
 [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>]
 [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbc33-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbc33-105">DESCRIPTION</span></span>
<span data-ttu-id="fbc33-106">Создайте определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="fbc33-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="fbc33-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbc33-107">EXAMPLES</span></span>

### <span data-ttu-id="fbc33-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbc33-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="fbc33-109">Создайте определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="fbc33-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="fbc33-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbc33-110">PARAMETERS</span></span>

### <span data-ttu-id="fbc33-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbc33-111">-AsJob</span></span>
<span data-ttu-id="fbc33-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fbc33-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbc33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc33-113">-DefaultProfile</span></span>
<span data-ttu-id="fbc33-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbc33-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbc33-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="fbc33-115">-Description</span></span>
<span data-ttu-id="fbc33-116">Описание ресурса, в котором определена коллекция изображений.</span><span class="sxs-lookup"><span data-stu-id="fbc33-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="fbc33-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="fbc33-117">-DisallowedDiskType</span></span>
<span data-ttu-id="fbc33-118">Недопустимые типы дисков.</span><span class="sxs-lookup"><span data-stu-id="fbc33-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="fbc33-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="fbc33-119">-EndOfLifeDate</span></span>
<span data-ttu-id="fbc33-120">Дата окончания срока действия определения изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="fbc33-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="fbc33-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="fbc33-121">-Eula</span></span>
<span data-ttu-id="fbc33-122">Лицензионное соглашение для определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="fbc33-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="fbc33-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="fbc33-123">-GalleryName</span></span>
<span data-ttu-id="fbc33-124">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="fbc33-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="fbc33-125">-Location</span><span class="sxs-lookup"><span data-stu-id="fbc33-125">-Location</span></span>
<span data-ttu-id="fbc33-126">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="fbc33-126">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc33-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="fbc33-127">-MaximumMemory</span></span>
<span data-ttu-id="fbc33-128">Максимум рекомендованной памяти</span><span class="sxs-lookup"><span data-stu-id="fbc33-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="fbc33-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="fbc33-129">-MaximumVCPU</span></span>
<span data-ttu-id="fbc33-130">Максимум рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="fbc33-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="fbc33-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="fbc33-131">-MinimumMemory</span></span>
<span data-ttu-id="fbc33-132">Минимальная рекомендуемая память</span><span class="sxs-lookup"><span data-stu-id="fbc33-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="fbc33-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="fbc33-133">-MinimumVCPU</span></span>
<span data-ttu-id="fbc33-134">Минимум рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="fbc33-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="fbc33-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fbc33-135">-Name</span></span>
<span data-ttu-id="fbc33-136">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="fbc33-136">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc33-137">-Предложение</span><span class="sxs-lookup"><span data-stu-id="fbc33-137">-Offer</span></span>
<span data-ttu-id="fbc33-138">Имя предложения определения изображения в галерее.</span><span class="sxs-lookup"><span data-stu-id="fbc33-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="fbc33-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="fbc33-139">-OsState</span></span>
<span data-ttu-id="fbc33-140">Состояние операционной системы</span><span class="sxs-lookup"><span data-stu-id="fbc33-140">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc33-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="fbc33-141">-OsType</span></span>
<span data-ttu-id="fbc33-142">Тип операционной системы</span><span class="sxs-lookup"><span data-stu-id="fbc33-142">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc33-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="fbc33-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="fbc33-144">URI заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="fbc33-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="fbc33-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fbc33-145">-Publisher</span></span>
<span data-ttu-id="fbc33-146">Имя издателя определения галереи.</span><span class="sxs-lookup"><span data-stu-id="fbc33-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="fbc33-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="fbc33-147">-PurchasePlanName</span></span>
<span data-ttu-id="fbc33-148">ИДЕНТИФИКАТОР плана покупок.</span><span class="sxs-lookup"><span data-stu-id="fbc33-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fbc33-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="fbc33-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="fbc33-150">КОД продукта для плана заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="fbc33-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fbc33-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="fbc33-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="fbc33-152">Идентификатор издателя для плана покупки.</span><span class="sxs-lookup"><span data-stu-id="fbc33-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="fbc33-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="fbc33-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="fbc33-154">URI заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="fbc33-154">The release note uri.</span></span>

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

### <span data-ttu-id="fbc33-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc33-155">-ResourceGroupName</span></span>
<span data-ttu-id="fbc33-156">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fbc33-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="fbc33-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="fbc33-157">-Sku</span></span>
<span data-ttu-id="fbc33-158">Имя SKU определения изображения галереи.</span><span class="sxs-lookup"><span data-stu-id="fbc33-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="fbc33-159">-Тег</span><span class="sxs-lookup"><span data-stu-id="fbc33-159">-Tag</span></span>
<span data-ttu-id="fbc33-160">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="fbc33-160">Resource tags</span></span>

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

### <span data-ttu-id="fbc33-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbc33-161">-Confirm</span></span>
<span data-ttu-id="fbc33-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbc33-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbc33-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbc33-163">-WhatIf</span></span>
<span data-ttu-id="fbc33-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbc33-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbc33-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbc33-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbc33-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc33-166">CommonParameters</span></span>
<span data-ttu-id="fbc33-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbc33-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc33-168">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbc33-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc33-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbc33-169">INPUTS</span></span>

### <span data-ttu-id="fbc33-170">System. String</span><span class="sxs-lookup"><span data-stu-id="fbc33-170">System.String</span></span>

### <span data-ttu-id="fbc33-171">Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="fbc33-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="fbc33-172">Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="fbc33-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="fbc33-173">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="fbc33-173">System.DateTime</span></span>

### <span data-ttu-id="fbc33-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbc33-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fbc33-175">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fbc33-175">System.Int32</span></span>

### <span data-ttu-id="fbc33-176">System. String []</span><span class="sxs-lookup"><span data-stu-id="fbc33-176">System.String[]</span></span>

## <span data-ttu-id="fbc33-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbc33-177">OUTPUTS</span></span>

### <span data-ttu-id="fbc33-178">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="fbc33-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="fbc33-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbc33-179">NOTES</span></span>

## <span data-ttu-id="fbc33-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbc33-180">RELATED LINKS</span></span>
