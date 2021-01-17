---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 2d0eb49a46e0d6fbbe02d145e42195d059c5176f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399268"
---
# <span data-ttu-id="56d27-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="56d27-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="56d27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56d27-102">SYNOPSIS</span></span>
<span data-ttu-id="56d27-103">Создание спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="56d27-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="56d27-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56d27-104">SYNTAX</span></span>

### <span data-ttu-id="56d27-105">FromJsonStringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56d27-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56d27-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="56d27-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56d27-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56d27-107">DESCRIPTION</span></span>
<span data-ttu-id="56d27-108">Создает новую версию шаблона с указанным содержимым ARM шаблона.</span><span class="sxs-lookup"><span data-stu-id="56d27-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="56d27-109">Содержимое может быть либо из необработанных строк JSON (с помощью набора параметров **FromJsonStringParameterSet),** либо из указанного файла JSON (с помощью набора параметров **FromJsonFileParameterSet).**</span><span class="sxs-lookup"><span data-stu-id="56d27-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="56d27-110">Если корневая спецификация шаблона не существует, она будет создана вместе с версией Шаблон спецификации.</span><span class="sxs-lookup"><span data-stu-id="56d27-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="56d27-111">Если спецификация шаблона уже существует с указанным именем, она и указанная версия будут обновлены (все другие существующие версии будут сохранены).</span><span class="sxs-lookup"><span data-stu-id="56d27-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="56d27-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56d27-112">EXAMPLES</span></span>

### <span data-ttu-id="56d27-113">Пример 1.</span><span class="sxs-lookup"><span data-stu-id="56d27-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="56d27-114">Создает новую версию спецификации шаблона "версия 1.0" в шаблоне Spec с именем myTemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="56d27-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="56d27-115">В указанной версии $templateJson как содержимое шаблона ARM версии.</span><span class="sxs-lookup"><span data-stu-id="56d27-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="56d27-116">**Примечание.** Шаблон ARM в этом примере не имеет никакого никакого ресурса, так как он не содержит фактических ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56d27-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="56d27-117">Пример 2.</span><span class="sxs-lookup"><span data-stu-id="56d27-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="56d27-118">Создает новую версию спецификации шаблона "версия 2.0" в шаблоне Spec с именем myTemplateSpec.</span><span class="sxs-lookup"><span data-stu-id="56d27-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="56d27-119">В качестве содержимого шаблона для указанной версии будет "myTemplateContent.jsARM".</span><span class="sxs-lookup"><span data-stu-id="56d27-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="56d27-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56d27-120">PARAMETERS</span></span>

### <span data-ttu-id="56d27-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d27-121">-DefaultProfile</span></span>
<span data-ttu-id="56d27-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56d27-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56d27-123">-Description</span><span class="sxs-lookup"><span data-stu-id="56d27-123">-Description</span></span>
<span data-ttu-id="56d27-124">Описание спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="56d27-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="56d27-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="56d27-125">-DisplayName</span></span>
<span data-ttu-id="56d27-126">Отображаемая имя спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="56d27-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="56d27-127">-Force</span><span class="sxs-lookup"><span data-stu-id="56d27-127">-Force</span></span>
<span data-ttu-id="56d27-128">Не спрашивайте подтверждения при переописи существующей версии.</span><span class="sxs-lookup"><span data-stu-id="56d27-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="56d27-129">-Location</span><span class="sxs-lookup"><span data-stu-id="56d27-129">-Location</span></span>
<span data-ttu-id="56d27-130">Расположение спецификации шаблона. Требуется только в том случае, если спецификация шаблона еще не существует.</span><span class="sxs-lookup"><span data-stu-id="56d27-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="56d27-131">-Name</span><span class="sxs-lookup"><span data-stu-id="56d27-131">-Name</span></span>
<span data-ttu-id="56d27-132">Имя спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="56d27-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="56d27-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56d27-133">-ResourceGroupName</span></span>
<span data-ttu-id="56d27-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56d27-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="56d27-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="56d27-135">-Tag</span></span>
<span data-ttu-id="56d27-136">Количество тегов для нового шаблона спецификаций ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56d27-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="56d27-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="56d27-137">-TemplateFile</span></span>
<span data-ttu-id="56d27-138">Путь к локальному шаблону Диспетчера ресурсов Azure, который является JSON-файлом.</span><span class="sxs-lookup"><span data-stu-id="56d27-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d27-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="56d27-139">-TemplateJson</span></span>
<span data-ttu-id="56d27-140">Шаблон Диспетчера ресурсов Azure JSON.</span><span class="sxs-lookup"><span data-stu-id="56d27-140">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d27-141">-Версия</span><span class="sxs-lookup"><span data-stu-id="56d27-141">-Version</span></span>
<span data-ttu-id="56d27-142">Версия спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="56d27-142">The version of the template spec.</span></span>

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

### <span data-ttu-id="56d27-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="56d27-143">-VersionDescription</span></span>
<span data-ttu-id="56d27-144">Описание версии.</span><span class="sxs-lookup"><span data-stu-id="56d27-144">The description of the version.</span></span>

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

### <span data-ttu-id="56d27-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56d27-145">-Confirm</span></span>
<span data-ttu-id="56d27-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d27-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d27-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d27-147">-WhatIf</span></span>
<span data-ttu-id="56d27-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d27-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56d27-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56d27-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d27-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d27-150">CommonParameters</span></span>
<span data-ttu-id="56d27-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d27-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d27-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56d27-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d27-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56d27-153">INPUTS</span></span>

### <span data-ttu-id="56d27-154">System.String</span><span class="sxs-lookup"><span data-stu-id="56d27-154">System.String</span></span>

## <span data-ttu-id="56d27-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56d27-155">OUTPUTS</span></span>

### <span data-ttu-id="56d27-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="56d27-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="56d27-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56d27-157">NOTES</span></span>

## <span data-ttu-id="56d27-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56d27-158">RELATED LINKS</span></span>
