---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentWhatIfResult.md
ms.openlocfilehash: 8e25d83eda64bb9705829ff0a8b1dd40d6055953
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505247"
---
# <span data-ttu-id="eaba8-101">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="eaba8-101">Get-AzTenantDeploymentWhatIfResult</span></span>

## <span data-ttu-id="eaba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaba8-102">SYNOPSIS</span></span>
<span data-ttu-id="eaba8-103">Возвращает шаблон ARM шаблон What-If для развертывания в области клиента.</span><span class="sxs-lookup"><span data-stu-id="eaba8-103">Gets an ARM template What-If result for a deployment at tenant scope.</span></span> 

## <span data-ttu-id="eaba8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eaba8-104">SYNTAX</span></span>

### <span data-ttu-id="eaba8-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eaba8-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="eaba8-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="eaba8-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="eaba8-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="eaba8-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="eaba8-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="eaba8-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="eaba8-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="eaba8-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="eaba8-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="eaba8-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaba8-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="eaba8-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzTenantDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaba8-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaba8-117">DESCRIPTION</span></span>
<span data-ttu-id="eaba8-118">Для развертывания шаблона в указанной области клиента ARM What-If шаблона **Get-AzTenantDeploymentWhatIfResult.**</span><span class="sxs-lookup"><span data-stu-id="eaba8-118">The **Get-AzTenantDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified tenant scope.</span></span> <span data-ttu-id="eaba8-119">Она возвращает список изменений, указывающий, какие ресурсы будут обновлены в случае применения развертывания, не внося изменений в реальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="eaba8-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="eaba8-120">Чтобы указать формат возвращаемго результата, используйте параметр *ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="eaba8-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="eaba8-121">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eaba8-121">EXAMPLES</span></span>

### <span data-ttu-id="eaba8-122">Пример 1. Получите What-If в области клиента</span><span class="sxs-lookup"><span data-stu-id="eaba8-122">Example 1: Get a What-If result at tenant scope</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="eaba8-123">Эта команда возвращает What-If в клиенте с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="eaba8-123">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="eaba8-124">Для указания места *хранения* данных развертывания используется параметр Location.</span><span class="sxs-lookup"><span data-stu-id="eaba8-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="eaba8-125">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="eaba8-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="eaba8-126">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="eaba8-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="eaba8-127">Для этого используется параметр *ResultFormat* What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="eaba8-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="eaba8-128">Пример 2. Получите What-If в области клиента с Помощью ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="eaba8-128">Example 2: Get a What-If result at tenant scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzTenantDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="eaba8-129">Эта команда возвращает What-If в клиенте с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="eaba8-129">This command gets a What-If result at tenant scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="eaba8-130">Для указания места *хранения* данных развертывания используется параметр Location.</span><span class="sxs-lookup"><span data-stu-id="eaba8-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="eaba8-131">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="eaba8-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="eaba8-132">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="eaba8-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="eaba8-133">Команда использует параметр *ResultFormat,* чтобы у What-If результатов содержались только ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eaba8-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="eaba8-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaba8-134">PARAMETERS</span></span>

### <span data-ttu-id="eaba8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaba8-135">-DefaultProfile</span></span>
<span data-ttu-id="eaba8-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eaba8-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaba8-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="eaba8-137">-ExcludeChangeType</span></span>
<span data-ttu-id="eaba8-138">Список типов изменений, разделенных запятой, которые нужно исключить из What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="eaba8-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="eaba8-139">-Location</span><span class="sxs-lookup"><span data-stu-id="eaba8-139">-Location</span></span>
<span data-ttu-id="eaba8-140">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="eaba8-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="eaba8-141">-Name</span><span class="sxs-lookup"><span data-stu-id="eaba8-141">-Name</span></span>
<span data-ttu-id="eaba8-142">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="eaba8-142">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="eaba8-143">Если не указано иное, по умолчанию имя файла шаблона задано при его указании. по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="eaba8-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="eaba8-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="eaba8-144">-Pre</span></span>
<span data-ttu-id="eaba8-145">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="eaba8-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="eaba8-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="eaba8-146">-ResultFormat</span></span>
<span data-ttu-id="eaba8-147">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="eaba8-147">The What-If result format.</span></span>

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

### <span data-ttu-id="eaba8-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="eaba8-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="eaba8-149">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="eaba8-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="eaba8-150">При проверке пользователю будет предложено в качестве значения пропустить отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не был привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="eaba8-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="eaba8-151">Для неинтерационных сценариев можно использовать параметр SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="eaba8-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="eaba8-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="eaba8-152">-TemplateFile</span></span>
<span data-ttu-id="eaba8-153">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="eaba8-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="eaba8-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="eaba8-154">-TemplateObject</span></span>
<span data-ttu-id="eaba8-155">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="eaba8-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="eaba8-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="eaba8-156">-TemplateParameterFile</span></span>
<span data-ttu-id="eaba8-157">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="eaba8-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="eaba8-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="eaba8-158">-TemplateParameterObject</span></span>
<span data-ttu-id="eaba8-159">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="eaba8-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="eaba8-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="eaba8-160">-TemplateParameterUri</span></span>
<span data-ttu-id="eaba8-161">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="eaba8-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="eaba8-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="eaba8-162">-TemplateUri</span></span>
<span data-ttu-id="eaba8-163">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="eaba8-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="eaba8-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaba8-164">CommonParameters</span></span>
<span data-ttu-id="eaba8-165">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaba8-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaba8-166">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eaba8-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaba8-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eaba8-167">INPUTS</span></span>

### <span data-ttu-id="eaba8-168">System.String</span><span class="sxs-lookup"><span data-stu-id="eaba8-168">System.String</span></span>

### <span data-ttu-id="eaba8-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="eaba8-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eaba8-170">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eaba8-170">OUTPUTS</span></span>

### <span data-ttu-id="eaba8-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="eaba8-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="eaba8-172">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eaba8-172">NOTES</span></span>

## <span data-ttu-id="eaba8-173">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaba8-173">RELATED LINKS</span></span>
