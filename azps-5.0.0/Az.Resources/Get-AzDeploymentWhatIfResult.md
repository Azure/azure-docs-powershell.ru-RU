---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentWhatIfResult.md
ms.openlocfilehash: 0ad3df8e010beec777bd059bbef708774570792d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245901"
---
# <span data-ttu-id="66c7e-101">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="66c7e-101">Get-AzDeploymentWhatIfResult</span></span>

## <span data-ttu-id="66c7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="66c7e-103">Получает шаблон ARM What-If результат развертывания в области подписки.</span><span class="sxs-lookup"><span data-stu-id="66c7e-103">Gets an ARM template What-If result for a deployment at subscription scope.</span></span> 

## <span data-ttu-id="66c7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66c7e-104">SYNTAX</span></span>

### <span data-ttu-id="66c7e-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66c7e-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="66c7e-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="66c7e-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="66c7e-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="66c7e-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="66c7e-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="66c7e-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="66c7e-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="66c7e-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="66c7e-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="66c7e-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c7e-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="66c7e-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzDeploymentWhatIfResult [-Name <String>] -Location <String> [-ResultFormat <WhatIfResultFormat>]
 [-ExcludeChangeType <String[]>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66c7e-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66c7e-117">DESCRIPTION</span></span>
<span data-ttu-id="66c7e-118">Командлет **Get-AzDeploymentWhatIfResult** получает шаблон ARM, What-If результат развертывания шаблона в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="66c7e-118">The **Get-AzDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the current subscription scope.</span></span> <span data-ttu-id="66c7e-119">Функция возвращает список изменений, указывающих на то, какие ресурсы будут обновляться, если развертывание применяется без внесения изменений в реальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="66c7e-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="66c7e-120">Чтобы задать формат возвращаемого результата, используйте параметр *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="66c7e-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="66c7e-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66c7e-121">EXAMPLES</span></span>

### <span data-ttu-id="66c7e-122">Пример 1: получение результата What-If в области подписки</span><span class="sxs-lookup"><span data-stu-id="66c7e-122">Example 1: Get a What-If result at subscription scope</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="66c7e-123">Эта команда возвращает What-If результат в текущей области подписки с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="66c7e-123">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="66c7e-124">В команде параметр *Location* используется для указания места хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="66c7e-124">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="66c7e-125">В команде используется параметр *TemplateFile* , чтобы указать файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="66c7e-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="66c7e-126">В команде используется параметр *TemplateParameterFile* для указания файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="66c7e-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="66c7e-127">В команде используется параметр *ResultFormat* , чтобы установить для What-If результат, чтобы он включал полные полезные данные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66c7e-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="66c7e-128">Пример 2: получение результата What-If в области подписки с помощью ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="66c7e-128">Example 2: Get a What-If result at subscription scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -Location "West US" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="66c7e-129">Эта команда возвращает What-If результат в текущей области подписки с помощью настраиваемого файла шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="66c7e-129">This command gets a What-If result at the current subscription scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="66c7e-130">В команде параметр *Location* используется для указания места хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="66c7e-130">The command uses the *Location* parameter to specify where to store the deployment data.</span></span>
<span data-ttu-id="66c7e-131">В команде используется параметр *TemplateFile* , чтобы указать файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="66c7e-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="66c7e-132">В команде используется параметр *TemplateParameterFile* для указания файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="66c7e-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="66c7e-133">В команде используется параметр *ResultFormat* , чтобы сделать так, чтобы в качестве What-If выдержались только идентификаторы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="66c7e-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="66c7e-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66c7e-134">PARAMETERS</span></span>

### <span data-ttu-id="66c7e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c7e-135">-DefaultProfile</span></span>
<span data-ttu-id="66c7e-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66c7e-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66c7e-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="66c7e-137">-ExcludeChangeType</span></span>
<span data-ttu-id="66c7e-138">Список типов изменения ресурсов, разделенных запятыми, которые будут исключены из результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="66c7e-138">Comma-separated list of resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="66c7e-139">-Location</span><span class="sxs-lookup"><span data-stu-id="66c7e-139">-Location</span></span>
<span data-ttu-id="66c7e-140">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="66c7e-140">The location to store deployment data.</span></span>

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

### <span data-ttu-id="66c7e-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66c7e-141">-Name</span></span>
<span data-ttu-id="66c7e-142">Имя развертывания, которое будет создано.</span><span class="sxs-lookup"><span data-stu-id="66c7e-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="66c7e-143">Если не указано, по умолчанию используется имя файла шаблона, когда указан файл шаблона; по умолчанию — текущее время, когда указан объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="66c7e-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="66c7e-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="66c7e-144">-Pre</span></span>
<span data-ttu-id="66c7e-145">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="66c7e-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="66c7e-146">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="66c7e-146">-ResultFormat</span></span>
<span data-ttu-id="66c7e-147">Формат результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="66c7e-147">The What-If result format.</span></span>

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

### <span data-ttu-id="66c7e-148">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="66c7e-148">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="66c7e-149">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="66c7e-149">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="66c7e-150">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="66c7e-150">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="66c7e-151">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="66c7e-151">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="66c7e-152">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="66c7e-152">-TemplateFile</span></span>
<span data-ttu-id="66c7e-153">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="66c7e-153">Local path to the template file.</span></span>

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

### <span data-ttu-id="66c7e-154">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="66c7e-154">-TemplateObject</span></span>
<span data-ttu-id="66c7e-155">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="66c7e-155">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="66c7e-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="66c7e-156">-TemplateParameterFile</span></span>
<span data-ttu-id="66c7e-157">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="66c7e-157">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="66c7e-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="66c7e-158">-TemplateParameterObject</span></span>
<span data-ttu-id="66c7e-159">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="66c7e-159">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="66c7e-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="66c7e-160">-TemplateParameterUri</span></span>
<span data-ttu-id="66c7e-161">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="66c7e-161">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="66c7e-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="66c7e-162">-TemplateUri</span></span>
<span data-ttu-id="66c7e-163">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="66c7e-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="66c7e-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c7e-164">CommonParameters</span></span>
<span data-ttu-id="66c7e-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66c7e-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c7e-166">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66c7e-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c7e-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66c7e-167">INPUTS</span></span>

### <span data-ttu-id="66c7e-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="66c7e-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="66c7e-169">System. String</span><span class="sxs-lookup"><span data-stu-id="66c7e-169">System.String</span></span>

## <span data-ttu-id="66c7e-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66c7e-170">OUTPUTS</span></span>

### <span data-ttu-id="66c7e-171">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. развертывания. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="66c7e-171">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="66c7e-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="66c7e-172">NOTES</span></span>

## <span data-ttu-id="66c7e-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66c7e-173">RELATED LINKS</span></span>
