---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: 09b0a1a6691b4c3d491d15d226fb8260fb7ae00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316415"
---
# <span data-ttu-id="0b803-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0b803-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="0b803-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b803-102">SYNOPSIS</span></span>
<span data-ttu-id="0b803-103">Получает шаблон ARM What-If результат развертывания в области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b803-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="0b803-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b803-104">SYNTAX</span></span>

### <span data-ttu-id="0b803-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b803-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b803-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0b803-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b803-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0b803-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b803-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="0b803-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b803-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0b803-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b803-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0b803-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b803-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="0b803-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b803-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0b803-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b803-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0b803-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b803-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="0b803-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b803-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0b803-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b803-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="0b803-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b803-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b803-117">DESCRIPTION</span></span>
<span data-ttu-id="0b803-118">Командлет **Get-AzResourceGroupDeploymentWhatIfResult** получает шаблон ARM, What-If результат для развертывания шаблона в указанной области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b803-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="0b803-119">Функция возвращает список изменений, указывающих на то, какие ресурсы будут обновляться, если развертывание применяется без внесения изменений в реальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="0b803-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="0b803-120">Чтобы задать формат возвращаемого результата, используйте параметр *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="0b803-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="0b803-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b803-121">EXAMPLES</span></span>

### <span data-ttu-id="0b803-122">Пример 1: получение What-If результатов в области группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0b803-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="0b803-123">Эта команда возвращает What-If результат в указанной области группы ресурсов с помощью файла настраиваемого шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="0b803-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="0b803-124">В команде используется параметр *ResourceGroupName* , чтобы указать группу ресурсов, в которой будет развернут шаблон.</span><span class="sxs-lookup"><span data-stu-id="0b803-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="0b803-125">В команде используется параметр *TemplateFile* , чтобы указать файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b803-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="0b803-126">В команде используется параметр *TemplateParameterFile* для указания файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b803-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="0b803-127">В команде используется параметр *ResultFormat* , чтобы установить для What-If результат, чтобы он включал полные полезные данные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b803-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="0b803-128">Пример 2: получение What-If результатов в области группы ресурсов с помощью ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="0b803-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="0b803-129">Эта команда возвращает What-If результат в указанной области группы ресурсов с помощью файла настраиваемого шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="0b803-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="0b803-130">В команде используется параметр *ResourceGroupName* , чтобы указать группу ресурсов, в которой будет развернут шаблон.</span><span class="sxs-lookup"><span data-stu-id="0b803-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="0b803-131">В команде используется параметр *TemplateFile* , чтобы указать файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b803-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="0b803-132">В команде используется параметр *TemplateParameterFile* для указания файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b803-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="0b803-133">В команде используется параметр *ResultFormat* , чтобы сделать так, чтобы в качестве What-If выдержались только идентификаторы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b803-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="0b803-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b803-134">PARAMETERS</span></span>

### <span data-ttu-id="0b803-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b803-135">-DefaultProfile</span></span>
<span data-ttu-id="0b803-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b803-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b803-137">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="0b803-137">-ExcludeChangeType</span></span>
<span data-ttu-id="0b803-138">Типы изменения ресурсов, разделенные запятыми, которые будут исключены из результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="0b803-138">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="0b803-139">Режим</span><span class="sxs-lookup"><span data-stu-id="0b803-139">-Mode</span></span>
<span data-ttu-id="0b803-140">Режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="0b803-140">The deployment mode.</span></span>

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

### <span data-ttu-id="0b803-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b803-141">-Name</span></span>
<span data-ttu-id="0b803-142">Имя развертывания, которое будет создано.</span><span class="sxs-lookup"><span data-stu-id="0b803-142">The name of the deployment it's going to create.</span></span> <span data-ttu-id="0b803-143">Если не указано, по умолчанию используется имя файла шаблона, когда указан файл шаблона; по умолчанию — текущее время, когда указан объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="0b803-143">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="0b803-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="0b803-144">-Pre</span></span>
<span data-ttu-id="0b803-145">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="0b803-145">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0b803-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b803-146">-ResourceGroupName</span></span>
<span data-ttu-id="0b803-147">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b803-147">The resource group name.</span></span>

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

### <span data-ttu-id="0b803-148">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="0b803-148">-ResultFormat</span></span>
<span data-ttu-id="0b803-149">Формат результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="0b803-149">The What-If result format.</span></span>

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

### <span data-ttu-id="0b803-150">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="0b803-150">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="0b803-151">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="0b803-151">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="0b803-152">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="0b803-152">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="0b803-153">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="0b803-153">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="0b803-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0b803-154">-TemplateFile</span></span>
<span data-ttu-id="0b803-155">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b803-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="0b803-156">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="0b803-156">-TemplateObject</span></span>
<span data-ttu-id="0b803-157">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="0b803-157">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="0b803-158">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0b803-158">-TemplateParameterFile</span></span>
<span data-ttu-id="0b803-159">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b803-159">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="0b803-160">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="0b803-160">-TemplateParameterObject</span></span>
<span data-ttu-id="0b803-161">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="0b803-161">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="0b803-162">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="0b803-162">-TemplateParameterUri</span></span>
<span data-ttu-id="0b803-163">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b803-163">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="0b803-164">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="0b803-164">-TemplateUri</span></span>
<span data-ttu-id="0b803-165">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b803-165">Uri to the template file.</span></span>

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

### <span data-ttu-id="0b803-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b803-166">CommonParameters</span></span>
<span data-ttu-id="0b803-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b803-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b803-168">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b803-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b803-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b803-169">INPUTS</span></span>

### <span data-ttu-id="0b803-170">System. String</span><span class="sxs-lookup"><span data-stu-id="0b803-170">System.String</span></span>

### <span data-ttu-id="0b803-171">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="0b803-171">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="0b803-172">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b803-172">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b803-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b803-173">OUTPUTS</span></span>

### <span data-ttu-id="0b803-174">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. развертывания. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="0b803-174">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="0b803-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b803-175">NOTES</span></span>

## <span data-ttu-id="0b803-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b803-176">RELATED LINKS</span></span>
