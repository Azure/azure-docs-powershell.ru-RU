---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentWhatIfResult.md
ms.openlocfilehash: df199c25a210a4975eccf96f9f7aa7e6c219689c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232052"
---
# <span data-ttu-id="81cb5-101">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="81cb5-101">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="81cb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="81cb5-103">Шаблон ARM шаблон What-If для развертывания в области группы управления.</span><span class="sxs-lookup"><span data-stu-id="81cb5-103">Gets an ARM template What-If result for a deployment at management group scope.</span></span> 

## <span data-ttu-id="81cb5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="81cb5-104">SYNTAX</span></span>

### <span data-ttu-id="81cb5-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="81cb5-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81cb5-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="81cb5-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81cb5-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="81cb5-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81cb5-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="81cb5-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81cb5-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="81cb5-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81cb5-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="81cb5-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81cb5-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="81cb5-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81cb5-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="81cb5-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81cb5-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="81cb5-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81cb5-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="81cb5-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="81cb5-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="81cb5-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81cb5-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="81cb5-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzManagementGroupDeploymentWhatIfResult [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81cb5-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81cb5-117">DESCRIPTION</span></span>
<span data-ttu-id="81cb5-118">Для развертывания шаблона в указанной области группы управления ARM шаблон What-If **Get-AzManagementGroupDeploymentWhatIfResult.**</span><span class="sxs-lookup"><span data-stu-id="81cb5-118">The **Get-AzManagementGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified management group scope.</span></span> <span data-ttu-id="81cb5-119">Она возвращает список изменений, указывающий, какие ресурсы будут обновлены в случае применения развертывания, не внося изменений в реальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="81cb5-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="81cb5-120">Чтобы указать формат возвращаемго результата, используйте параметр *ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="81cb5-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="81cb5-121">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="81cb5-121">EXAMPLES</span></span>

### <span data-ttu-id="81cb5-122">Пример 1. Получите What-If результат при масштабе группы управления</span><span class="sxs-lookup"><span data-stu-id="81cb5-122">Example 1: Get a What-If result at management group scope</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="81cb5-123">Эта команда возвращает What-If результат в группе управления с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="81cb5-123">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="81cb5-124">Для указания места *хранения данных* развертывания используется параметр Location.</span><span class="sxs-lookup"><span data-stu-id="81cb5-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="81cb5-125">Для указания группы управления, в которой будет развернут шаблон, используется параметр *ManagementGroupId.*</span><span class="sxs-lookup"><span data-stu-id="81cb5-125">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="81cb5-126">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="81cb5-126">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="81cb5-127">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="81cb5-127">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="81cb5-128">Для этого используется параметр *ResultFormat* What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="81cb5-128">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="81cb5-129">Пример 2. Получите What-If в масштабе группы управления с помощью ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="81cb5-129">Example 2: Get a What-If result at management group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzManagementGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -ManagementGroupId "myManagementGroup" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="81cb5-130">Эта команда возвращает What-If результат в группе управления с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="81cb5-130">This command gets a What-If result at management group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="81cb5-131">Для указания места *хранения данных* развертывания используется параметр Location.</span><span class="sxs-lookup"><span data-stu-id="81cb5-131">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="81cb5-132">Для указания группы управления, в которой будет развернут шаблон, используется параметр *ManagementGroupId.*</span><span class="sxs-lookup"><span data-stu-id="81cb5-132">The command uses the *ManagementGroupId* parameter to specify the management group where the template will be deployed.</span></span>
<span data-ttu-id="81cb5-133">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="81cb5-133">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="81cb5-134">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="81cb5-134">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="81cb5-135">Команда использует параметр *ResultFormat,* чтобы у What-If результатов содержались только ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81cb5-135">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="81cb5-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81cb5-136">PARAMETERS</span></span>

### <span data-ttu-id="81cb5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81cb5-137">-DefaultProfile</span></span>
<span data-ttu-id="81cb5-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81cb5-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81cb5-139">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="81cb5-139">-ExcludeChangeType</span></span>
<span data-ttu-id="81cb5-140">Список изменений, разделенный запятой, для исключения из результатов What-If ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81cb5-140">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="81cb5-141">-Location</span><span class="sxs-lookup"><span data-stu-id="81cb5-141">-Location</span></span>
<span data-ttu-id="81cb5-142">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="81cb5-142">The location to store deployment data.</span></span>

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

### <span data-ttu-id="81cb5-143">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="81cb5-143">-ManagementGroupId</span></span>
<span data-ttu-id="81cb5-144">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="81cb5-144">The management group ID.</span></span>

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

### <span data-ttu-id="81cb5-145">-Name</span><span class="sxs-lookup"><span data-stu-id="81cb5-145">-Name</span></span>
<span data-ttu-id="81cb5-146">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="81cb5-146">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="81cb5-147">Если не указано иное, по умолчанию имя файла шаблона задано при его указании. по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="81cb5-147">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="81cb5-148">-Pre</span><span class="sxs-lookup"><span data-stu-id="81cb5-148">-Pre</span></span>
<span data-ttu-id="81cb5-149">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="81cb5-149">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="81cb5-150">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="81cb5-150">-ResultFormat</span></span>
<span data-ttu-id="81cb5-151">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="81cb5-151">The What-If result format.</span></span>

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

### <span data-ttu-id="81cb5-152">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="81cb5-152">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="81cb5-153">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="81cb5-153">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="81cb5-154">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="81cb5-154">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="81cb5-155">Для неинтерационных сценариев можно использовать параметр SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="81cb5-155">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="81cb5-156">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="81cb5-156">-TemplateFile</span></span>
<span data-ttu-id="81cb5-157">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="81cb5-157">Local path to the template file.</span></span>

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

### <span data-ttu-id="81cb5-158">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="81cb5-158">-TemplateObject</span></span>
<span data-ttu-id="81cb5-159">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="81cb5-159">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="81cb5-160">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="81cb5-160">-TemplateParameterFile</span></span>
<span data-ttu-id="81cb5-161">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="81cb5-161">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="81cb5-162">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="81cb5-162">-TemplateParameterObject</span></span>
<span data-ttu-id="81cb5-163">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="81cb5-163">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="81cb5-164">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="81cb5-164">-TemplateParameterUri</span></span>
<span data-ttu-id="81cb5-165">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="81cb5-165">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="81cb5-166">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="81cb5-166">-TemplateUri</span></span>
<span data-ttu-id="81cb5-167">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="81cb5-167">Uri to the template file.</span></span>

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

### <span data-ttu-id="81cb5-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81cb5-168">CommonParameters</span></span>
<span data-ttu-id="81cb5-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81cb5-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81cb5-170">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81cb5-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81cb5-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81cb5-171">INPUTS</span></span>

### <span data-ttu-id="81cb5-172">System.String</span><span class="sxs-lookup"><span data-stu-id="81cb5-172">System.String</span></span>

### <span data-ttu-id="81cb5-173">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="81cb5-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="81cb5-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81cb5-174">OUTPUTS</span></span>

### <span data-ttu-id="81cb5-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="81cb5-175">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="81cb5-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="81cb5-176">NOTES</span></span>

## <span data-ttu-id="81cb5-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81cb5-177">RELATED LINKS</span></span>
