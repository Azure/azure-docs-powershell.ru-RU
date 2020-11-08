---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: ff2911c1fd8e49e5057c13c086f68a2b3489ad2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247038"
---
# <span data-ttu-id="96911-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="96911-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="96911-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96911-102">SYNOPSIS</span></span>
<span data-ttu-id="96911-103">Изменяет спецификацию шаблона.</span><span class="sxs-lookup"><span data-stu-id="96911-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="96911-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96911-104">SYNTAX</span></span>

### <span data-ttu-id="96911-105">FromJsonStringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96911-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96911-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96911-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96911-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="96911-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96911-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="96911-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96911-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96911-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96911-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="96911-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96911-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="96911-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96911-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96911-112">DESCRIPTION</span></span>
<span data-ttu-id="96911-113">Изменяет спецификацию Templace. Если спецификация шаблона с указанным именем и (или) определенной версией еще не существует, она будет создана.</span><span class="sxs-lookup"><span data-stu-id="96911-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="96911-114">При изменении содержимого шаблона ARM версии спецификации содержимое может либо поступать из необработанной строки JSON (с использованием параметра **UpdateVersionByNameFromJsonParameterSet** ), либо из указанного JSON-файла (с использованием **UpdateVersionByNameFromJsonFileParameterSet** Set).</span><span class="sxs-lookup"><span data-stu-id="96911-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="96911-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96911-115">EXAMPLES</span></span>

### <span data-ttu-id="96911-116">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="96911-116">Example 1:</span></span>
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

<span data-ttu-id="96911-117">Изменяет версию "v 1.0" спецификации шаблона с именем "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="96911-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="96911-118">Указанная версия будет $templateJson в качестве содержимого шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="96911-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="96911-119">Если спецификации корневого шаблона и (или) версии еще не существуют, они будут созданы.</span><span class="sxs-lookup"><span data-stu-id="96911-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="96911-120">**Пуск**</span><span class="sxs-lookup"><span data-stu-id="96911-120">**Notes:**</span></span> 

* <span data-ttu-id="96911-121">Шаблон ARM в примере является отсутствием операций, так как он не содержит реальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96911-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="96911-122">Расположение требуется только в том случае, если спецификация шаблона еще не существует</span><span class="sxs-lookup"><span data-stu-id="96911-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="96911-123">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="96911-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="96911-124">Изменяет версию "v 2.0" спецификации шаблона с именем "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="96911-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="96911-125">Указанная версия будет содержать содержимое из локального файла "myTemplateContent.json" в качестве содержимого шаблона ARM для версии.</span><span class="sxs-lookup"><span data-stu-id="96911-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="96911-126">Если спецификации корневого шаблона и (или) версии еще не существуют, они будут созданы.</span><span class="sxs-lookup"><span data-stu-id="96911-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="96911-127">**Примечание.** Расположение требуется только в том случае, если спецификация шаблона еще не существует</span><span class="sxs-lookup"><span data-stu-id="96911-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="96911-128">Пример 3:</span><span class="sxs-lookup"><span data-stu-id="96911-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="96911-129">Изменение описания спецификации шаблона с именем "myTemplateSpec" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="96911-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="96911-130">Если спецификаций шаблона еще не существует, она будет создана.</span><span class="sxs-lookup"><span data-stu-id="96911-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="96911-131">**Примечание.** Расположение требуется только в том случае, если спецификация шаблона еще не существует</span><span class="sxs-lookup"><span data-stu-id="96911-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="96911-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96911-132">PARAMETERS</span></span>

### <span data-ttu-id="96911-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96911-133">-DefaultProfile</span></span>
<span data-ttu-id="96911-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96911-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96911-135">-Описание</span><span class="sxs-lookup"><span data-stu-id="96911-135">-Description</span></span>
<span data-ttu-id="96911-136">Описание спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="96911-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="96911-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="96911-137">-DisplayName</span></span>
<span data-ttu-id="96911-138">Отображаемое имя спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="96911-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="96911-139">-Location</span><span class="sxs-lookup"><span data-stu-id="96911-139">-Location</span></span>
<span data-ttu-id="96911-140">Расположение спецификации шаблона. Требуется только в том случае, если спецификация шаблона еще не существует.</span><span class="sxs-lookup"><span data-stu-id="96911-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="96911-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96911-141">-Name</span></span>
<span data-ttu-id="96911-142">Название спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="96911-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="96911-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96911-143">-ResourceGroupName</span></span>
<span data-ttu-id="96911-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96911-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="96911-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96911-145">-ResourceId</span></span>
<span data-ttu-id="96911-146">Полный идентификатор ресурса спецификации шаблона. Пример:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="96911-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="96911-147">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="96911-147">-TemplateFile</span></span>
<span data-ttu-id="96911-148">Путь к файлу для JSON файла шаблона локального диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="96911-148">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="96911-149">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="96911-149">-TemplateJson</span></span>
<span data-ttu-id="96911-150">JSON шаблона диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="96911-150">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="96911-151">-Version</span><span class="sxs-lookup"><span data-stu-id="96911-151">-Version</span></span>
<span data-ttu-id="96911-152">Версия спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="96911-152">The version of the template spec.</span></span>

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

### <span data-ttu-id="96911-153">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="96911-153">-VersionDescription</span></span>
<span data-ttu-id="96911-154">Описание версии.</span><span class="sxs-lookup"><span data-stu-id="96911-154">The description of the version.</span></span>

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

### <span data-ttu-id="96911-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96911-155">-Confirm</span></span>
<span data-ttu-id="96911-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96911-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96911-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96911-157">-WhatIf</span></span>
<span data-ttu-id="96911-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96911-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96911-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96911-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96911-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96911-160">CommonParameters</span></span>
<span data-ttu-id="96911-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96911-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96911-162">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96911-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96911-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96911-163">INPUTS</span></span>

### <span data-ttu-id="96911-164">System. String</span><span class="sxs-lookup"><span data-stu-id="96911-164">System.String</span></span>

## <span data-ttu-id="96911-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96911-165">OUTPUTS</span></span>

### <span data-ttu-id="96911-166">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="96911-166">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="96911-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="96911-167">NOTES</span></span>

## <span data-ttu-id="96911-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96911-168">RELATED LINKS</span></span>
