---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247041"
---
# <span data-ttu-id="2fad8-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="2fad8-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="2fad8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fad8-102">SYNOPSIS</span></span>
<span data-ttu-id="2fad8-103">Создает новую спецификацию шаблона.</span><span class="sxs-lookup"><span data-stu-id="2fad8-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="2fad8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fad8-104">SYNTAX</span></span>

### <span data-ttu-id="2fad8-105">FromJsonStringParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2fad8-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fad8-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fad8-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fad8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fad8-107">DESCRIPTION</span></span>
<span data-ttu-id="2fad8-108">Создает новую версию спецификации шаблона с указанным содержимым шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="2fad8-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="2fad8-109">Содержимое может либо поступать из необработанной строки JSON (с использованием параметра **FromJsonStringParameterSet** Set), либо из указанного JSON-файла (с использованием **FromJsonFileParameterSet** Set).</span><span class="sxs-lookup"><span data-stu-id="2fad8-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="2fad8-110">Если спецификация корневого шаблона еще не существует, она будет создана вместе с версией спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="2fad8-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="2fad8-111">Если спецификация шаблона с указанным именем уже существует, она будет обновлена (все существующие версии будут сохранены).</span><span class="sxs-lookup"><span data-stu-id="2fad8-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="2fad8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fad8-112">EXAMPLES</span></span>

### <span data-ttu-id="2fad8-113">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="2fad8-113">Example 1:</span></span>
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

<span data-ttu-id="2fad8-114">Создает новую спецификацию шаблона "v 1.0" в спецификации шаблона с именем "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="2fad8-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="2fad8-115">Указанная версия будет $templateJson в качестве содержимого шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="2fad8-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="2fad8-116">**Примечание.** Шаблон ARM в примере является отсутствием операций, так как он не содержит реальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fad8-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="2fad8-117">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="2fad8-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="2fad8-118">Создает новую спецификацию шаблона "v 2.0" в спецификации шаблона с именем "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="2fad8-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="2fad8-119">Указанная версия будет содержать содержимое из локального файла "myTemplateContent.json" в качестве содержимого шаблона ARM для версии.</span><span class="sxs-lookup"><span data-stu-id="2fad8-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="2fad8-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fad8-120">PARAMETERS</span></span>

### <span data-ttu-id="2fad8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fad8-121">-DefaultProfile</span></span>
<span data-ttu-id="2fad8-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fad8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fad8-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="2fad8-123">-Description</span></span>
<span data-ttu-id="2fad8-124">Описание спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="2fad8-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="2fad8-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2fad8-125">-DisplayName</span></span>
<span data-ttu-id="2fad8-126">Отображаемое имя спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="2fad8-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="2fad8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="2fad8-127">-Force</span></span>
<span data-ttu-id="2fad8-128">Не запрашивать подтверждение при перезаписи существующей версии.</span><span class="sxs-lookup"><span data-stu-id="2fad8-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="2fad8-129">-Location</span><span class="sxs-lookup"><span data-stu-id="2fad8-129">-Location</span></span>
<span data-ttu-id="2fad8-130">Расположение спецификации шаблона. Требуется только в том случае, если спецификация шаблона еще не существует.</span><span class="sxs-lookup"><span data-stu-id="2fad8-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="2fad8-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fad8-131">-Name</span></span>
<span data-ttu-id="2fad8-132">Название спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="2fad8-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="2fad8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fad8-133">-ResourceGroupName</span></span>
<span data-ttu-id="2fad8-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fad8-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="2fad8-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2fad8-135">-TemplateFile</span></span>
<span data-ttu-id="2fad8-136">Путь к файлу для JSON файла шаблона локального диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2fad8-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="2fad8-137">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="2fad8-137">-TemplateJson</span></span>
<span data-ttu-id="2fad8-138">JSON шаблона диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2fad8-138">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="2fad8-139">-Version</span><span class="sxs-lookup"><span data-stu-id="2fad8-139">-Version</span></span>
<span data-ttu-id="2fad8-140">Версия спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="2fad8-140">The version of the template spec.</span></span>

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

### <span data-ttu-id="2fad8-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="2fad8-141">-VersionDescription</span></span>
<span data-ttu-id="2fad8-142">Описание версии.</span><span class="sxs-lookup"><span data-stu-id="2fad8-142">The description of the version.</span></span>

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

### <span data-ttu-id="2fad8-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fad8-143">-Confirm</span></span>
<span data-ttu-id="2fad8-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fad8-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fad8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fad8-145">-WhatIf</span></span>
<span data-ttu-id="2fad8-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fad8-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fad8-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fad8-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fad8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fad8-148">CommonParameters</span></span>
<span data-ttu-id="2fad8-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fad8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fad8-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fad8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fad8-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fad8-151">INPUTS</span></span>

### <span data-ttu-id="2fad8-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2fad8-152">System.String</span></span>

## <span data-ttu-id="2fad8-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fad8-153">OUTPUTS</span></span>

### <span data-ttu-id="2fad8-154">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="2fad8-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="2fad8-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fad8-155">NOTES</span></span>

## <span data-ttu-id="2fad8-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fad8-156">RELATED LINKS</span></span>
