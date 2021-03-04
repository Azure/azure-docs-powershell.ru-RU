---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: fbfb0a10016d81edcffeb62580b1ca0ff9b5b341
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957571"
---
# <span data-ttu-id="41826-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="41826-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="41826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41826-102">SYNOPSIS</span></span>
<span data-ttu-id="41826-103">Создание определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="41826-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="41826-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41826-104">SYNTAX</span></span>

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

## <span data-ttu-id="41826-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41826-105">DESCRIPTION</span></span>
<span data-ttu-id="41826-106">Создание определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="41826-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="41826-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41826-107">EXAMPLES</span></span>

### <span data-ttu-id="41826-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41826-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="41826-109">Создание определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="41826-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="41826-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41826-110">PARAMETERS</span></span>

### <span data-ttu-id="41826-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41826-111">-AsJob</span></span>
<span data-ttu-id="41826-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="41826-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41826-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41826-113">-DefaultProfile</span></span>
<span data-ttu-id="41826-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41826-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41826-115">-Description</span><span class="sxs-lookup"><span data-stu-id="41826-115">-Description</span></span>
<span data-ttu-id="41826-116">Описание ресурса определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="41826-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="41826-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="41826-117">-DisallowedDiskType</span></span>
<span data-ttu-id="41826-118">Диски всех этих типов.</span><span class="sxs-lookup"><span data-stu-id="41826-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="41826-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="41826-119">-EndOfLifeDate</span></span>
<span data-ttu-id="41826-120">Дата окончания жизненного времени в коллекции "Определение изображения"</span><span class="sxs-lookup"><span data-stu-id="41826-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="41826-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="41826-121">-Eula</span></span>
<span data-ttu-id="41826-122">Соглашение Eula об определении изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="41826-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="41826-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="41826-123">-GalleryName</span></span>
<span data-ttu-id="41826-124">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="41826-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="41826-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="41826-125">-HyperVGeneration</span></span>
<span data-ttu-id="41826-126">Генерация гипервизора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="41826-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="41826-127">Применимо только к дискам ОС.</span><span class="sxs-lookup"><span data-stu-id="41826-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="41826-128">Допустимые значения: V1 и V2.</span><span class="sxs-lookup"><span data-stu-id="41826-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="41826-129">-Location</span><span class="sxs-lookup"><span data-stu-id="41826-129">-Location</span></span>
<span data-ttu-id="41826-130">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="41826-130">Resource location</span></span>

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

### <span data-ttu-id="41826-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="41826-131">-MaximumMemory</span></span>
<span data-ttu-id="41826-132">Максимальное значение рекомендуемой памяти</span><span class="sxs-lookup"><span data-stu-id="41826-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="41826-133">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="41826-133">-MaximumVCPU</span></span>
<span data-ttu-id="41826-134">Максимальное значение рекомендуемого ядра ЦП</span><span class="sxs-lookup"><span data-stu-id="41826-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="41826-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="41826-135">-MinimumMemory</span></span>
<span data-ttu-id="41826-136">Минимальная рекомендуемая память</span><span class="sxs-lookup"><span data-stu-id="41826-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="41826-137">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="41826-137">-MinimumVCPU</span></span>
<span data-ttu-id="41826-138">Минимальное рекомендуемое ядро ЦП</span><span class="sxs-lookup"><span data-stu-id="41826-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="41826-139">-Name</span><span class="sxs-lookup"><span data-stu-id="41826-139">-Name</span></span>
<span data-ttu-id="41826-140">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="41826-140">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="41826-141">-Offer</span><span class="sxs-lookup"><span data-stu-id="41826-141">-Offer</span></span>
<span data-ttu-id="41826-142">Имя предложения "Определение изображения коллекции".</span><span class="sxs-lookup"><span data-stu-id="41826-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="41826-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="41826-143">-OsState</span></span>
<span data-ttu-id="41826-144">Состояние ОС</span><span class="sxs-lookup"><span data-stu-id="41826-144">The state of OS</span></span>

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

### <span data-ttu-id="41826-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="41826-145">-OsType</span></span>
<span data-ttu-id="41826-146">Тип ОС</span><span class="sxs-lookup"><span data-stu-id="41826-146">The type of OS</span></span>

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

### <span data-ttu-id="41826-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="41826-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="41826-148">URI заявления о конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="41826-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="41826-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="41826-149">-Publisher</span></span>
<span data-ttu-id="41826-150">Имя издателя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="41826-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="41826-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="41826-151">-PurchasePlanName</span></span>
<span data-ttu-id="41826-152">ИД плана покупки.</span><span class="sxs-lookup"><span data-stu-id="41826-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="41826-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="41826-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="41826-154">ИД продукта для плана покупки.</span><span class="sxs-lookup"><span data-stu-id="41826-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="41826-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="41826-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="41826-156">ИД издателя для плана покупки.</span><span class="sxs-lookup"><span data-stu-id="41826-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="41826-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="41826-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="41826-158">URI заметки о выпуске.</span><span class="sxs-lookup"><span data-stu-id="41826-158">The release note uri.</span></span>

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

### <span data-ttu-id="41826-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41826-159">-ResourceGroupName</span></span>
<span data-ttu-id="41826-160">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41826-160">The name of the resource group.</span></span>

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

### <span data-ttu-id="41826-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="41826-161">-Sku</span></span>
<span data-ttu-id="41826-162">Имя SKU определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="41826-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="41826-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="41826-163">-Tag</span></span>
<span data-ttu-id="41826-164">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="41826-164">Resource tags</span></span>

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

### <span data-ttu-id="41826-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41826-165">-Confirm</span></span>
<span data-ttu-id="41826-166">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="41826-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41826-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41826-167">-WhatIf</span></span>
<span data-ttu-id="41826-168">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41826-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41826-169">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="41826-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41826-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41826-170">CommonParameters</span></span>
<span data-ttu-id="41826-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41826-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41826-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41826-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41826-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41826-173">INPUTS</span></span>

### <span data-ttu-id="41826-174">System.String</span><span class="sxs-lookup"><span data-stu-id="41826-174">System.String</span></span>

### <span data-ttu-id="41826-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="41826-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="41826-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="41826-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="41826-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="41826-177">System.DateTime</span></span>

### <span data-ttu-id="41826-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="41826-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="41826-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="41826-179">System.Int32</span></span>

### <span data-ttu-id="41826-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="41826-180">System.String[]</span></span>

## <span data-ttu-id="41826-181">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41826-181">OUTPUTS</span></span>

### <span data-ttu-id="41826-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="41826-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="41826-183">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41826-183">NOTES</span></span>

## <span data-ttu-id="41826-184">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41826-184">RELATED LINKS</span></span>
