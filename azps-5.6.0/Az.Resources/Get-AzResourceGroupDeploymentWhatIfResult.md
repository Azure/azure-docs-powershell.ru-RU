---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 1b45c08f2906f3b1bec827a7f870d2c901bbb2b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963800"
---
# <span data-ttu-id="bd883-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="bd883-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="bd883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd883-102">SYNOPSIS</span></span>
<span data-ttu-id="bd883-103">Шаблон, What-If для развертывания в области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd883-103">Gets a template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="bd883-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd883-104">SYNTAX</span></span>

### <span data-ttu-id="bd883-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="bd883-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd883-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="bd883-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd883-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="bd883-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd883-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="bd883-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd883-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="bd883-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd883-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="bd883-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd883-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="bd883-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd883-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="bd883-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd883-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="bd883-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd883-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="bd883-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd883-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="bd883-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd883-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="bd883-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd883-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd883-117">DESCRIPTION</span></span>
<span data-ttu-id="bd883-118">Для развертывания шаблона в указанной области для группы ресурсов ARM What-If результат шаблона **Get-AzResourceGroupDeploymentWhatIfResult.**</span><span class="sxs-lookup"><span data-stu-id="bd883-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="bd883-119">Она возвращает список изменений, указывающий, какие ресурсы будут обновлены в случае применения развертывания, не внося изменений в реальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="bd883-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="bd883-120">Чтобы указать формат возвращаемго результата, используйте параметр *ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="bd883-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="bd883-121">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd883-121">EXAMPLES</span></span>

### <span data-ttu-id="bd883-122">Пример 1. Получить What-If в области действия группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bd883-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="bd883-123">Эта команда возвращает What-If к заданной области группы ресурсов, используя файл настраиваемого шаблона и файл параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="bd883-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="bd883-124">Для указания группы ресурсов, в которой будет развернут шаблон, используется параметр *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="bd883-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="bd883-125">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="bd883-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="bd883-126">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="bd883-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="bd883-127">Команда использует параметр *ResultFormat* для What-If результатов для полной загрузки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd883-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="bd883-128">Пример 2. Получите What-If в области группы ресурсов с помощью ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="bd883-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="bd883-129">Эта команда возвращает What-If к заданной области группы ресурсов, используя файл настраиваемого шаблона и файл параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="bd883-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="bd883-130">Для указания группы ресурсов, в которой будет развернут шаблон, используется параметр *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="bd883-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="bd883-131">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="bd883-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="bd883-132">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="bd883-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="bd883-133">Команда использует параметр *ResultFormat,* чтобы у What-If результатов содержались только ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd883-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="bd883-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd883-134">PARAMETERS</span></span>

### <span data-ttu-id="bd883-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd883-135">-DefaultProfile</span></span>
<span data-ttu-id="bd883-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd883-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd883-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="bd883-137">-ExcludeChangeType</span></span>
<span data-ttu-id="bd883-138">Типы изменений ресурсов, разделенные запятой, которые следует исключить из What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="bd883-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-139">-Mode</span><span class="sxs-lookup"><span data-stu-id="bd883-139">-Mode</span></span>
<span data-ttu-id="bd883-140">Режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="bd883-140">The deployment mode.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-141">-Name</span><span class="sxs-lookup"><span data-stu-id="bd883-141">-Name</span></span>
<span data-ttu-id="bd883-142">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="bd883-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="bd883-143">Если не указано иное, по умолчанию имя файла шаблона задано при его указании. по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="bd883-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="bd883-144">-Pre</span></span>
<span data-ttu-id="bd883-145">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="bd883-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bd883-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd883-146">-ResourceGroupName</span></span>
<span data-ttu-id="bd883-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd883-147">The resource group name.</span></span>

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

### <span data-ttu-id="bd883-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="bd883-148">-ResultFormat</span></span>
<span data-ttu-id="bd883-149">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="bd883-149">The What-If result format.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.WhatIfResultFormat
Parameter Sets: (All)
Aliases:
Accepted values: ResourceIdOnly, FullResourcePayloads

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="bd883-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="bd883-151">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="bd883-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="bd883-152">При проверке пользователю будет предложено в качестве значения пропустить отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не был привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="bd883-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="bd883-153">Для неинтерационных сценариев можно использовать параметр SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="bd883-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="bd883-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="bd883-154">-TemplateFile</span></span>
<span data-ttu-id="bd883-155">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="bd883-155">Local path to the template file.</span></span> <span data-ttu-id="bd883-156">Поддерживаемый тип файла шаблона: json и bicep.</span><span class="sxs-lookup"><span data-stu-id="bd883-156">Supported template file type: json and bicep.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-157">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="bd883-157">-TemplateObject</span></span>
<span data-ttu-id="bd883-158">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="bd883-158">A hash table which represents the template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-159">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="bd883-159">-TemplateParameterFile</span></span>
<span data-ttu-id="bd883-160">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="bd883-160">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-161">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="bd883-161">-TemplateParameterObject</span></span>
<span data-ttu-id="bd883-162">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="bd883-162">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-163">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="bd883-163">-TemplateParameterUri</span></span>
<span data-ttu-id="bd883-164">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="bd883-164">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-165">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="bd883-165">-TemplateUri</span></span>
<span data-ttu-id="bd883-166">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="bd883-166">Uri to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd883-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd883-167">CommonParameters</span></span>
<span data-ttu-id="bd883-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd883-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd883-169">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd883-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd883-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd883-170">INPUTS</span></span>

### <span data-ttu-id="bd883-171">System.String</span><span class="sxs-lookup"><span data-stu-id="bd883-171">System.String</span></span>

### <span data-ttu-id="bd883-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="bd883-172">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="bd883-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd883-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bd883-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd883-174">OUTPUTS</span></span>

### <span data-ttu-id="bd883-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="bd883-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="bd883-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd883-176">NOTES</span></span>

## <span data-ttu-id="bd883-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd883-177">RELATED LINKS</span></span>
