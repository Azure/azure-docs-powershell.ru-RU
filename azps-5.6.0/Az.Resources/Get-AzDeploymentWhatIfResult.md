---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 725984f8893b7373ded513b0d7242d9ec4bd0c6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985662"
---
# <span data-ttu-id="ffdfa-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="ffdfa-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="ffdfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffdfa-102">SYNOPSIS</span></span>
<span data-ttu-id="ffdfa-103">Шаблоны What-If для развертывания в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-103">Gets a template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="ffdfa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ffdfa-104">SYNTAX</span></span>

### <span data-ttu-id="ffdfa-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffdfa-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ffdfa-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ffdfa-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="ffdfa-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ffdfa-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ffdfa-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="ffdfa-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ffdfa-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ffdfa-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="ffdfa-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ffdfa-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffdfa-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="ffdfa-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffdfa-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffdfa-117">DESCRIPTION</span></span>
<span data-ttu-id="ffdfa-118">Для развертывания шаблона в текущей области подписки ARM шаблон What-If **Get-AzDeploymentWhatIfResult.**</span><span class="sxs-lookup"><span data-stu-id="ffdfa-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="ffdfa-119">Она возвращает список изменений, указывающий, какие ресурсы будут обновлены при применении развертывания, не внося никаких изменений в реальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="ffdfa-120">Чтобы указать формат возвращаемго результата, используйте параметр *ResultFormat.*</span><span class="sxs-lookup"><span data-stu-id="ffdfa-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="ffdfa-121">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ffdfa-121">EXAMPLES</span></span>

### <span data-ttu-id="ffdfa-122">Пример 1. Получите What-If по области действия подписки</span><span class="sxs-lookup"><span data-stu-id="ffdfa-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="ffdfa-123">Эта команда возвращает What-If текущую область действия подписки с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="ffdfa-124">Для указания места *хранения* данных развертывания используется параметр Location.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="ffdfa-125">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="ffdfa-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="ffdfa-126">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="ffdfa-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="ffdfa-127">Для этого используется параметр *ResultFormat* What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="ffdfa-128">Пример 2. Получите результат What-If области действия подписки с ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="ffdfa-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="ffdfa-129">Эта команда возвращает What-If текущую область действия подписки с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="ffdfa-130">Для указания места *хранения* данных развертывания используется параметр Location.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="ffdfa-131">Для указания файла шаблона используется параметр *TemplateFile.*</span><span class="sxs-lookup"><span data-stu-id="ffdfa-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="ffdfa-132">Для указания файла *параметра шаблона используется параметр TemplateParameterFile.*</span><span class="sxs-lookup"><span data-stu-id="ffdfa-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="ffdfa-133">Команда использует параметр *ResultFormat,* чтобы у What-If результатов содержались только ИД ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="ffdfa-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffdfa-134">PARAMETERS</span></span>

### <span data-ttu-id="ffdfa-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffdfa-135">-DefaultProfile</span></span>
<span data-ttu-id="ffdfa-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffdfa-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="ffdfa-137">-ExcludeChangeType</span></span>
<span data-ttu-id="ffdfa-138">Список изменений, разделенный запятой, для исключения из результатов What-If ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="ffdfa-139">-Location</span><span class="sxs-lookup"><span data-stu-id="ffdfa-139">-Location</span></span>
<span data-ttu-id="ffdfa-140">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="ffdfa-141">-Name</span><span class="sxs-lookup"><span data-stu-id="ffdfa-141">-Name</span></span>
<span data-ttu-id="ffdfa-142">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="ffdfa-143">Если не указано иное, по умолчанию имя файла шаблона задано при его указании. по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="ffdfa-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="ffdfa-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="ffdfa-144">-Pre</span></span>
<span data-ttu-id="ffdfa-145">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ffdfa-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="ffdfa-146">-ResultFormat</span></span>
<span data-ttu-id="ffdfa-147">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-147">The What-If result format.</span></span>

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

### <span data-ttu-id="ffdfa-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="ffdfa-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="ffdfa-149">Пропускает динамическую обработку параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="ffdfa-150">При проверке пользователю будет предложено в качестве значения пропустить отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не был привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="ffdfa-151">Для неинтерационных сценариев можно использовать параметр SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="ffdfa-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ffdfa-152">-TemplateFile</span></span>
<span data-ttu-id="ffdfa-153">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-153">Local path to the template file.</span></span> <span data-ttu-id="ffdfa-154">Поддерживаемый тип файла шаблона: json и bicep.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-154">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="ffdfa-155">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="ffdfa-155">-TemplateObject</span></span>
<span data-ttu-id="ffdfa-156">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-156">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="ffdfa-157">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ffdfa-157">-TemplateParameterFile</span></span>
<span data-ttu-id="ffdfa-158">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-158">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="ffdfa-159">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="ffdfa-159">-TemplateParameterObject</span></span>
<span data-ttu-id="ffdfa-160">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-160">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="ffdfa-161">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="ffdfa-161">-TemplateParameterUri</span></span>
<span data-ttu-id="ffdfa-162">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-162">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="ffdfa-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="ffdfa-163">-TemplateUri</span></span>
<span data-ttu-id="ffdfa-164">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-164">Uri to the template file.</span></span>

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

### <span data-ttu-id="ffdfa-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffdfa-165">CommonParameters</span></span>
<span data-ttu-id="ffdfa-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffdfa-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffdfa-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffdfa-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffdfa-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffdfa-168">INPUTS</span></span>

### <span data-ttu-id="ffdfa-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ffdfa-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ffdfa-170">System.String</span><span class="sxs-lookup"><span data-stu-id="ffdfa-170">System.String</span></span>

## <span data-ttu-id="ffdfa-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ffdfa-171">OUTPUTS</span></span>

### <span data-ttu-id="ffdfa-172">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="ffdfa-172">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="ffdfa-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ffdfa-173">NOTES</span></span>

## <span data-ttu-id="ffdfa-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffdfa-174">RELATED LINKS</span></span>
