---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 681cbc620a5c6067102dfe2a67f20dd9edc42046
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240032"
---
# <span data-ttu-id="320c7-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="320c7-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="320c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="320c7-102">SYNOPSIS</span></span>
<span data-ttu-id="320c7-103">Изменяет спецификацию шаблона.</span><span class="sxs-lookup"><span data-stu-id="320c7-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="320c7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="320c7-104">SYNTAX</span></span>

### <span data-ttu-id="320c7-105">FromJsonStringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="320c7-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="320c7-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="320c7-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320c7-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="320c7-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320c7-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="320c7-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320c7-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="320c7-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320c7-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="320c7-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320c7-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="320c7-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="320c7-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="320c7-112">DESCRIPTION</span></span>
<span data-ttu-id="320c7-113">Изменяет спецификацию Templace. Если спецификация шаблона с указанным именем или определенной версией еще не существует, она будет создана.</span><span class="sxs-lookup"><span data-stu-id="320c7-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="320c7-114">При изменении содержимого шаблона шаблона ARM спецификации шаблона его содержимое может быть либо из необработанных строк JSON (с помощью набора параметров **UpdateVersionByNameFromJsonParameterSet),** либо из указанного файла JSON (с помощью **параметра UpdateVersionByNameFromJsonFileParameterSet).**</span><span class="sxs-lookup"><span data-stu-id="320c7-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="320c7-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="320c7-115">EXAMPLES</span></span>

### <span data-ttu-id="320c7-116">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="320c7-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="320c7-117">Изменяет версию "v1.0" спецификации шаблона с именем "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="320c7-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="320c7-118">В указанной версии $templateJson как содержимое шаблона ARM версии.</span><span class="sxs-lookup"><span data-stu-id="320c7-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="320c7-119">Если корневой спецификации шаблона или версии еще не существует, они будут созданы.</span><span class="sxs-lookup"><span data-stu-id="320c7-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="320c7-120">**Примечания.**</span><span class="sxs-lookup"><span data-stu-id="320c7-120">**Notes:**</span></span> 

* <span data-ttu-id="320c7-121">Шаблон ARM в этом примере не имеет никакого никакого ресурса, так как он не содержит фактических ресурсов.</span><span class="sxs-lookup"><span data-stu-id="320c7-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="320c7-122">Расположение является требоваться только в том случае, если шаблон спецификации еще не существует</span><span class="sxs-lookup"><span data-stu-id="320c7-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="320c7-123">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="320c7-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="320c7-124">Изменяет версию "v2.0" спецификации шаблона с именем "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="320c7-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="320c7-125">В качестве содержимого шаблона для указанной версии будет "myTemplateContent.jsARM".</span><span class="sxs-lookup"><span data-stu-id="320c7-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="320c7-126">Если корневой спецификации шаблона или версии еще не существует, они будут созданы.</span><span class="sxs-lookup"><span data-stu-id="320c7-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="320c7-127">**Примечание.** Расположение является требоваться только в том случае, если шаблон спецификации еще не существует</span><span class="sxs-lookup"><span data-stu-id="320c7-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="320c7-128">Пример 3.</span><span class="sxs-lookup"><span data-stu-id="320c7-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="320c7-129">Изменяет описание шаблона "MyTemplateSpec" в группе ресурсов myRG.</span><span class="sxs-lookup"><span data-stu-id="320c7-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="320c7-130">Если спецификация шаблона еще не существует, она будет создана.</span><span class="sxs-lookup"><span data-stu-id="320c7-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="320c7-131">**Примечание.** Расположение является требоваться только в том случае, если шаблон спецификации еще не существует</span><span class="sxs-lookup"><span data-stu-id="320c7-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="320c7-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="320c7-132">PARAMETERS</span></span>

### <span data-ttu-id="320c7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320c7-133">-DefaultProfile</span></span>
<span data-ttu-id="320c7-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="320c7-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="320c7-135">-Description</span><span class="sxs-lookup"><span data-stu-id="320c7-135">-Description</span></span>
<span data-ttu-id="320c7-136">Описание спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="320c7-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="320c7-137">-DisplayName</span></span>
<span data-ttu-id="320c7-138">Отображаемая имя спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="320c7-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-139">-Location</span><span class="sxs-lookup"><span data-stu-id="320c7-139">-Location</span></span>
<span data-ttu-id="320c7-140">Расположение спецификации шаблона. Требуется только в том случае, если спецификация шаблона еще не существует.</span><span class="sxs-lookup"><span data-stu-id="320c7-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="320c7-141">-Name</span><span class="sxs-lookup"><span data-stu-id="320c7-141">-Name</span></span>
<span data-ttu-id="320c7-142">Имя спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="320c7-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320c7-143">-ResourceGroupName</span></span>
<span data-ttu-id="320c7-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="320c7-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="320c7-145">-ResourceId</span></span>
<span data-ttu-id="320c7-146">Полное имя ресурса спецификации шаблона. Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="320c7-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="320c7-147">-Tag</span></span>
<span data-ttu-id="320c7-148">Количество тегов для спецификации шаблона и версии</span><span class="sxs-lookup"><span data-stu-id="320c7-148">Hashtable of tags for the template spec and/or version</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="320c7-149">-TemplateFile</span></span>
<span data-ttu-id="320c7-150">Путь к локальному шаблону Диспетчера ресурсов Azure, который является JSON-файлом.</span><span class="sxs-lookup"><span data-stu-id="320c7-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="320c7-151">-TemplateJson</span></span>
<span data-ttu-id="320c7-152">Шаблон Диспетчера ресурсов Azure с использованием JSON.</span><span class="sxs-lookup"><span data-stu-id="320c7-152">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-153">-Version</span><span class="sxs-lookup"><span data-stu-id="320c7-153">-Version</span></span>
<span data-ttu-id="320c7-154">Версия спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="320c7-154">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="320c7-155">-VersionDescription</span></span>
<span data-ttu-id="320c7-156">Описание версии.</span><span class="sxs-lookup"><span data-stu-id="320c7-156">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320c7-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="320c7-157">-Confirm</span></span>
<span data-ttu-id="320c7-158">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320c7-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320c7-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320c7-159">-WhatIf</span></span>
<span data-ttu-id="320c7-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320c7-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="320c7-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="320c7-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320c7-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320c7-162">CommonParameters</span></span>
<span data-ttu-id="320c7-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320c7-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320c7-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="320c7-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320c7-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="320c7-165">INPUTS</span></span>

### <span data-ttu-id="320c7-166">System.String</span><span class="sxs-lookup"><span data-stu-id="320c7-166">System.String</span></span>

## <span data-ttu-id="320c7-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="320c7-167">OUTPUTS</span></span>

### <span data-ttu-id="320c7-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="320c7-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="320c7-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="320c7-169">NOTES</span></span>

## <span data-ttu-id="320c7-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="320c7-170">RELATED LINKS</span></span>
