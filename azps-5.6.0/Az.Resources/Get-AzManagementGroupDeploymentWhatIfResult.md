---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 981d9e771a988a4166f542854959b38e140d2061
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971848"
---
# <span data-ttu-id="4a258-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="4a258-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="4a258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a258-102">SYNOPSIS</span></span>
<span data-ttu-id="4a258-103">Шаблон, What-If для развертывания в масштабе группы управления.</span><span class="sxs-lookup"><span data-stu-id="4a258-103">Gets a template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="4a258-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a258-104">SYNTAX</span></span>

### <span data-ttu-id="4a258-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a258-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a258-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a258-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a258-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a258-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a258-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a258-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a258-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a258-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a258-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a258-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a258-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a258-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a258-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a258-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a258-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a258-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a258-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a258-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a258-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4a258-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a258-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="4a258-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a258-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a258-117">DESCRIPTION</span></span>
<span data-ttu-id="4a258-118">Для развертывания шаблона в указанной области группы управления ARM шаблон What-If **Get-AzManagementGroupDeploymentWhatIfResult.**</span><span class="sxs-lookup"><span data-stu-id="4a258-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="4a258-119">Она возвращает список изменений, указывающий, какие ресурсы будут обновлены при применении развертывания, не внося никаких изменений в реальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="4a258-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="4a258-120">Чтобы указать формат возвращаемго результата, используйте параметр *ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="4a258-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="4a258-121">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a258-121">EXAMPLES</span></span>

### <span data-ttu-id="4a258-122">Пример 1. Получите What-If результат при масштабе группы управления</span><span class="sxs-lookup"><span data-stu-id="4a258-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="4a258-123">Эта команда возвращает What-If результат в группе управления с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="4a258-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="4a258-124">Для указания места *хранения* данных развертывания используется параметр Location.</span><span class="sxs-lookup"><span data-stu-id="4a258-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="4a258-125">Для указания группы управления, в которой будет развернут шаблон, используется параметр *ManagementGroupId.*</span><span class="sxs-lookup"><span data-stu-id="4a258-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="4a258-126">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="4a258-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="4a258-127">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="4a258-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="4a258-128">Команда использует параметр *ResultFormat* для What-If результатов для полной загрузки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a258-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="4a258-129">Пример 2. Получите What-If в масштабе группы управления с помощью ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="4a258-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="4a258-130">Эта команда возвращает What-If результат в группе управления с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="4a258-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="4a258-131">Для указания места *хранения* данных развертывания используется параметр Location.</span><span class="sxs-lookup"><span data-stu-id="4a258-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="4a258-132">Для указания группы управления, в которой будет развернут шаблон, используется параметр *ManagementGroupId.*</span><span class="sxs-lookup"><span data-stu-id="4a258-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="4a258-133">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="4a258-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="4a258-134">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="4a258-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="4a258-135">Команда использует параметр *ResultFormat,* чтобы у What-If результатов содержались только ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a258-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="4a258-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a258-136">PARAMETERS</span></span>

### <span data-ttu-id="4a258-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a258-137">-DefaultProfile</span></span>
<span data-ttu-id="4a258-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a258-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a258-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="4a258-139">-ExcludeChangeType</span></span>
<span data-ttu-id="4a258-140">Список типов изменений, разделенных запятой, которые нужно исключить из What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="4a258-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="4a258-141">-Location</span><span class="sxs-lookup"><span data-stu-id="4a258-141">-Location</span></span>
<span data-ttu-id="4a258-142">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="4a258-142">The location to store deployment data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a258-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4a258-143">-ManagementGroupId</span></span>
<span data-ttu-id="4a258-144">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="4a258-144">The management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a258-145">-Name</span><span class="sxs-lookup"><span data-stu-id="4a258-145">-Name</span></span>
<span data-ttu-id="4a258-146">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="4a258-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="4a258-147">Если он не задан, по умолчанию заданное имя файла шаблона при его предоставлении; по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="4a258-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a258-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="4a258-148">-Pre</span></span>
<span data-ttu-id="4a258-149">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="4a258-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4a258-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="4a258-150">-ResultFormat</span></span>
<span data-ttu-id="4a258-151">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="4a258-151">The What-If result format.</span></span>

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

### <span data-ttu-id="4a258-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="4a258-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="4a258-153">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="4a258-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="4a258-154">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="4a258-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="4a258-155">Для неинтерационных сценариев можно использовать параметр SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="4a258-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="4a258-156">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="4a258-156">-TemplateFile</span></span>
<span data-ttu-id="4a258-157">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="4a258-157">Local path to the template file.</span></span> <span data-ttu-id="4a258-158">Поддерживаемый тип файла шаблона: json и bicep.</span><span class="sxs-lookup"><span data-stu-id="4a258-158">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="4a258-159">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="4a258-159">-TemplateObject</span></span>
<span data-ttu-id="4a258-160">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="4a258-160">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="4a258-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="4a258-161">-TemplateParameterFile</span></span>
<span data-ttu-id="4a258-162">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="4a258-162">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="4a258-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="4a258-163">-TemplateParameterObject</span></span>
<span data-ttu-id="4a258-164">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="4a258-164">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="4a258-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="4a258-165">-TemplateParameterUri</span></span>
<span data-ttu-id="4a258-166">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="4a258-166">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="4a258-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="4a258-167">-TemplateUri</span></span>
<span data-ttu-id="4a258-168">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="4a258-168">Uri to the template file.</span></span>

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

### <span data-ttu-id="4a258-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a258-169">CommonParameters</span></span>
<span data-ttu-id="4a258-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a258-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a258-171">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a258-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a258-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a258-172">INPUTS</span></span>

### <span data-ttu-id="4a258-173">System.String</span><span class="sxs-lookup"><span data-stu-id="4a258-173">System.String</span></span>

### <span data-ttu-id="4a258-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a258-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a258-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a258-175">OUTPUTS</span></span>

### <span data-ttu-id="4a258-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="4a258-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="4a258-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a258-177">NOTES</span></span>

## <span data-ttu-id="4a258-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a258-178">RELATED LINKS</span></span>
