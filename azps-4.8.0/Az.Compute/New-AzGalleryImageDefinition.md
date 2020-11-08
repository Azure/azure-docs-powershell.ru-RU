---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: aaba7580e2ffd00a2e5a9e61dd087e6af6359513
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079124"
---
# <span data-ttu-id="6d18b-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="6d18b-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="6d18b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d18b-102">SYNOPSIS</span></span>
<span data-ttu-id="6d18b-103">Создайте определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="6d18b-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="6d18b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d18b-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d18b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d18b-105">DESCRIPTION</span></span>
<span data-ttu-id="6d18b-106">Создайте определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="6d18b-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="6d18b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d18b-107">EXAMPLES</span></span>

### <span data-ttu-id="6d18b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d18b-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="6d18b-109">Создайте определение изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="6d18b-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="6d18b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d18b-110">PARAMETERS</span></span>

### <span data-ttu-id="6d18b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d18b-111">-AsJob</span></span>
<span data-ttu-id="6d18b-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6d18b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d18b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d18b-113">-DefaultProfile</span></span>
<span data-ttu-id="6d18b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d18b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d18b-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="6d18b-115">-Description</span></span>
<span data-ttu-id="6d18b-116">Описание ресурса, в котором определена коллекция изображений.</span><span class="sxs-lookup"><span data-stu-id="6d18b-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="6d18b-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="6d18b-117">-DisallowedDiskType</span></span>
<span data-ttu-id="6d18b-118">Недопустимые типы дисков.</span><span class="sxs-lookup"><span data-stu-id="6d18b-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="6d18b-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="6d18b-119">-EndOfLifeDate</span></span>
<span data-ttu-id="6d18b-120">Дата окончания срока действия определения изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="6d18b-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="6d18b-121">-EULA</span><span class="sxs-lookup"><span data-stu-id="6d18b-121">-Eula</span></span>
<span data-ttu-id="6d18b-122">Лицензионное соглашение для определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="6d18b-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="6d18b-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="6d18b-123">-GalleryName</span></span>
<span data-ttu-id="6d18b-124">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="6d18b-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="6d18b-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="6d18b-125">-HyperVGeneration</span></span>
<span data-ttu-id="6d18b-126">Создание гипервизора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d18b-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="6d18b-127">Применимо только к дискам ОС.</span><span class="sxs-lookup"><span data-stu-id="6d18b-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="6d18b-128">Допустимые значения: v1 и v2.</span><span class="sxs-lookup"><span data-stu-id="6d18b-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="6d18b-129">-Location</span><span class="sxs-lookup"><span data-stu-id="6d18b-129">-Location</span></span>
<span data-ttu-id="6d18b-130">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="6d18b-130">Resource location</span></span>

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

### <span data-ttu-id="6d18b-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="6d18b-131">-MaximumMemory</span></span>
<span data-ttu-id="6d18b-132">Максимум рекомендованной памяти</span><span class="sxs-lookup"><span data-stu-id="6d18b-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="6d18b-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="6d18b-133">-MaximumVCPU</span></span>
<span data-ttu-id="6d18b-134">Максимум рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="6d18b-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="6d18b-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="6d18b-135">-MinimumMemory</span></span>
<span data-ttu-id="6d18b-136">Минимальная рекомендуемая память</span><span class="sxs-lookup"><span data-stu-id="6d18b-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="6d18b-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="6d18b-137">-MinimumVCPU</span></span>
<span data-ttu-id="6d18b-138">Минимум рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="6d18b-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="6d18b-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d18b-139">-Name</span></span>
<span data-ttu-id="6d18b-140">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="6d18b-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="6d18b-141">-Предложение</span><span class="sxs-lookup"><span data-stu-id="6d18b-141">-Offer</span></span>
<span data-ttu-id="6d18b-142">Имя предложения определения изображения в галерее.</span><span class="sxs-lookup"><span data-stu-id="6d18b-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="6d18b-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="6d18b-143">-OsState</span></span>
<span data-ttu-id="6d18b-144">Состояние операционной системы</span><span class="sxs-lookup"><span data-stu-id="6d18b-144">The state of OS</span></span>

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

### <span data-ttu-id="6d18b-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="6d18b-145">-OsType</span></span>
<span data-ttu-id="6d18b-146">Тип операционной системы</span><span class="sxs-lookup"><span data-stu-id="6d18b-146">The type of OS</span></span>

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

### <span data-ttu-id="6d18b-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="6d18b-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="6d18b-148">URI заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="6d18b-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="6d18b-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6d18b-149">-Publisher</span></span>
<span data-ttu-id="6d18b-150">Имя издателя определения галереи.</span><span class="sxs-lookup"><span data-stu-id="6d18b-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="6d18b-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="6d18b-151">-PurchasePlanName</span></span>
<span data-ttu-id="6d18b-152">ИДЕНТИФИКАТОР плана покупок.</span><span class="sxs-lookup"><span data-stu-id="6d18b-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="6d18b-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="6d18b-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="6d18b-154">КОД продукта для плана заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="6d18b-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="6d18b-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="6d18b-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="6d18b-156">Идентификатор издателя для плана покупки.</span><span class="sxs-lookup"><span data-stu-id="6d18b-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="6d18b-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="6d18b-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="6d18b-158">URI заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="6d18b-158">The release note uri.</span></span>

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

### <span data-ttu-id="6d18b-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d18b-159">-ResourceGroupName</span></span>
<span data-ttu-id="6d18b-160">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d18b-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="6d18b-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="6d18b-161">-Sku</span></span>
<span data-ttu-id="6d18b-162">Имя SKU определения изображения галереи.</span><span class="sxs-lookup"><span data-stu-id="6d18b-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="6d18b-163">-Тег</span><span class="sxs-lookup"><span data-stu-id="6d18b-163">-Tag</span></span>
<span data-ttu-id="6d18b-164">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="6d18b-164">Resource tags</span></span>

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

### <span data-ttu-id="6d18b-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d18b-165">-Confirm</span></span>
<span data-ttu-id="6d18b-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d18b-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d18b-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d18b-167">-WhatIf</span></span>
<span data-ttu-id="6d18b-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d18b-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d18b-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d18b-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d18b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d18b-170">CommonParameters</span></span>
<span data-ttu-id="6d18b-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d18b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d18b-172">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d18b-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d18b-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d18b-173">INPUTS</span></span>

### <span data-ttu-id="6d18b-174">System. String</span><span class="sxs-lookup"><span data-stu-id="6d18b-174">System.String</span></span>

### <span data-ttu-id="6d18b-175">Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="6d18b-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="6d18b-176">Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="6d18b-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="6d18b-177">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="6d18b-177">System.DateTime</span></span>

### <span data-ttu-id="6d18b-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6d18b-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6d18b-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6d18b-179">System.Int32</span></span>

### <span data-ttu-id="6d18b-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="6d18b-180">System.String[]</span></span>

## <span data-ttu-id="6d18b-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d18b-181">OUTPUTS</span></span>

### <span data-ttu-id="6d18b-182">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="6d18b-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="6d18b-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d18b-183">NOTES</span></span>

## <span data-ttu-id="6d18b-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d18b-184">RELATED LINKS</span></span>
