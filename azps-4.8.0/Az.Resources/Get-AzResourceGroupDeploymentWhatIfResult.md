---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentwhatifresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentWhatIfResult.md
ms.openlocfilehash: aa011c7a858f08e3528fb2cdd7d67bcff37d76d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235452"
---
# <span data-ttu-id="564a0-101">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="564a0-101">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

## <span data-ttu-id="564a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="564a0-102">SYNOPSIS</span></span>
<span data-ttu-id="564a0-103">Получает шаблон ARM What-If результат развертывания в области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="564a0-103">Gets an ARM template What-If result for a deployment at resource group scope.</span></span> 

## <span data-ttu-id="564a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="564a0-104">SYNTAX</span></span>

### <span data-ttu-id="564a0-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="564a0-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="564a0-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="564a0-106">ByTemplateObjectAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564a0-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="564a0-107">ByTemplateFileAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564a0-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="564a0-108">ByTemplateUriAndParameterObject</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564a0-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="564a0-109">ByTemplateObjectAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564a0-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="564a0-110">ByTemplateFileAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564a0-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="564a0-111">ByTemplateUriAndParameterFile</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564a0-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="564a0-112">ByTemplateObjectAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564a0-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="564a0-113">ByTemplateFileAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564a0-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="564a0-114">ByTemplateUriAndParameterUri</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564a0-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="564a0-115">ByTemplateObjectWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="564a0-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="564a0-116">ByTemplateUriWithNoParameters</span></span>
```
Get-AzResourceGroupDeploymentWhatIfResult [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-ResultFormat <WhatIfResultFormat>] [-ExcludeChangeType <String[]>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="564a0-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="564a0-117">DESCRIPTION</span></span>
<span data-ttu-id="564a0-118">Командлет **Get-AzResourceGroupDeploymentWhatIfResult** получает шаблон ARM, What-If результат для развертывания шаблона в указанной области группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="564a0-118">The **Get-AzResourceGroupDeploymentWhatIfResult** cmdlet gets the ARM template What-If result for a template deployment at the specified resource group scope.</span></span> <span data-ttu-id="564a0-119">Функция возвращает список изменений, указывающих на то, какие ресурсы будут обновляться, если развертывание применяется без внесения изменений в реальные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="564a0-119">It returns a list of changes indicating what resources will be updated if the deployment is applied without making any changes to real resources.</span></span> <span data-ttu-id="564a0-120">Чтобы задать формат возвращаемого результата, используйте параметр *ResultFormat* .</span><span class="sxs-lookup"><span data-stu-id="564a0-120">To specify the format for the returning result, use the *ResultFormat* parameter.</span></span>

## <span data-ttu-id="564a0-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="564a0-121">EXAMPLES</span></span>

### <span data-ttu-id="564a0-122">Пример 1: получение What-If результатов в области группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="564a0-122">Example 1: Get a What-If result at resource group scope</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "FullResourcePayloads"
```

<span data-ttu-id="564a0-123">Эта команда возвращает What-If результат в указанной области группы ресурсов с помощью файла настраиваемого шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="564a0-123">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="564a0-124">В команде используется параметр *ResourceGroupName* , чтобы указать группу ресурсов, в которой будет развернут шаблон.</span><span class="sxs-lookup"><span data-stu-id="564a0-124">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="564a0-125">В команде используется параметр *TemplateFile* , чтобы указать файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="564a0-125">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="564a0-126">В команде используется параметр *TemplateParameterFile* для указания файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="564a0-126">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="564a0-127">В команде используется параметр *ResultFormat* , чтобы установить для What-If результат, чтобы он включал полные полезные данные ресурсов.</span><span class="sxs-lookup"><span data-stu-id="564a0-127">The command uses the *ResultFormat* parameter to set the What-If result to include full resource payloads.</span></span>

### <span data-ttu-id="564a0-128">Пример 2: получение What-If результатов в области группы ресурсов с помощью ResourceIdOnly</span><span class="sxs-lookup"><span data-stu-id="564a0-128">Example 2: Get a What-If result at resource group scope with ResourceIdOnly</span></span>
```powershell
PS C:\> Get-AzResourceGroupDeploymentWhatIfResult `
    -DeploymentName "deploy-01" `
    -ResourceGroupName "myRG1" `
    -TemplateFile "D:\Azure\Templates\ServiceTemplate.json" `
    -TemplateParameterFile "D:\Azure\Templates\ServiceParameters.json" `
    -ResultFormat "ResourceIdOnly"
```

<span data-ttu-id="564a0-129">Эта команда возвращает What-If результат в указанной области группы ресурсов с помощью файла настраиваемого шаблона и файла параметров на диске.</span><span class="sxs-lookup"><span data-stu-id="564a0-129">This command gets a What-If result at the specified resource group scope by using a custom template file and a parameter file on disk.</span></span>
<span data-ttu-id="564a0-130">В команде используется параметр *ResourceGroupName* , чтобы указать группу ресурсов, в которой будет развернут шаблон.</span><span class="sxs-lookup"><span data-stu-id="564a0-130">The command uses the *ResourceGroupName* parameter to specify a resource group where the template will be deployed.</span></span>
<span data-ttu-id="564a0-131">В команде используется параметр *TemplateFile* , чтобы указать файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="564a0-131">The command uses the *TemplateFile* parameter to specify a template file.</span></span>
<span data-ttu-id="564a0-132">В команде используется параметр *TemplateParameterFile* для указания файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="564a0-132">The command uses the *TemplateParameterFile* parameter to specify a template parameter file.</span></span>
<span data-ttu-id="564a0-133">В команде используется параметр *ResultFormat* , чтобы сделать так, чтобы в качестве What-If выдержались только идентификаторы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="564a0-133">The command uses the *ResultFormat* parameter to set the What-If result to only contain resource IDs.</span></span>

## <span data-ttu-id="564a0-134">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="564a0-134">PARAMETERS</span></span>

### <span data-ttu-id="564a0-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="564a0-135">-ApiVersion</span></span>
<span data-ttu-id="564a0-136">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="564a0-136">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="564a0-137">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="564a0-137">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="564a0-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564a0-138">-DefaultProfile</span></span>
<span data-ttu-id="564a0-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="564a0-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="564a0-140">-ExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="564a0-140">-ExcludeChangeType</span></span>
<span data-ttu-id="564a0-141">Типы изменения ресурсов, разделенные запятыми, которые будут исключены из результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="564a0-141">Comma-separated resource change types to be excluded from What-If results.</span></span>

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

### <span data-ttu-id="564a0-142">Режим</span><span class="sxs-lookup"><span data-stu-id="564a0-142">-Mode</span></span>
<span data-ttu-id="564a0-143">Режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="564a0-143">The deployment mode.</span></span>

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

### <span data-ttu-id="564a0-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="564a0-144">-Name</span></span>
<span data-ttu-id="564a0-145">Имя развертывания, которое будет создано.</span><span class="sxs-lookup"><span data-stu-id="564a0-145">The name of the deployment it's going to create.</span></span> <span data-ttu-id="564a0-146">Если не указано, по умолчанию используется имя файла шаблона, когда указан файл шаблона; по умолчанию — текущее время, когда указан объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="564a0-146">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="564a0-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="564a0-147">-Pre</span></span>
<span data-ttu-id="564a0-148">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="564a0-148">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="564a0-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="564a0-149">-ResourceGroupName</span></span>
<span data-ttu-id="564a0-150">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="564a0-150">The resource group name.</span></span>

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

### <span data-ttu-id="564a0-151">-ResultFormat</span><span class="sxs-lookup"><span data-stu-id="564a0-151">-ResultFormat</span></span>
<span data-ttu-id="564a0-152">Формат результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="564a0-152">The What-If result format.</span></span>

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

### <span data-ttu-id="564a0-153">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="564a0-153">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="564a0-154">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="564a0-154">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="564a0-155">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="564a0-155">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="564a0-156">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="564a0-156">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="564a0-157">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="564a0-157">-TemplateFile</span></span>
<span data-ttu-id="564a0-158">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="564a0-158">Local path to the template file.</span></span>

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

### <span data-ttu-id="564a0-159">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="564a0-159">-TemplateObject</span></span>
<span data-ttu-id="564a0-160">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="564a0-160">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="564a0-161">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="564a0-161">-TemplateParameterFile</span></span>
<span data-ttu-id="564a0-162">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="564a0-162">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="564a0-163">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="564a0-163">-TemplateParameterObject</span></span>
<span data-ttu-id="564a0-164">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="564a0-164">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="564a0-165">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="564a0-165">-TemplateParameterUri</span></span>
<span data-ttu-id="564a0-166">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="564a0-166">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="564a0-167">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="564a0-167">-TemplateUri</span></span>
<span data-ttu-id="564a0-168">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="564a0-168">Uri to the template file.</span></span>

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

### <span data-ttu-id="564a0-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564a0-169">CommonParameters</span></span>
<span data-ttu-id="564a0-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="564a0-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564a0-171">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="564a0-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564a0-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="564a0-172">INPUTS</span></span>

### <span data-ttu-id="564a0-173">System. String</span><span class="sxs-lookup"><span data-stu-id="564a0-173">System.String</span></span>

### <span data-ttu-id="564a0-174">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="564a0-174">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="564a0-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="564a0-175">System.Collections.Hashtable</span></span>

## <span data-ttu-id="564a0-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="564a0-176">OUTPUTS</span></span>

### <span data-ttu-id="564a0-177">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. развертывания. PSWhatIfOperationResult</span><span class="sxs-lookup"><span data-stu-id="564a0-177">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.Deployments.PSWhatIfOperationResult</span></span>

## <span data-ttu-id="564a0-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="564a0-178">NOTES</span></span>

## <span data-ttu-id="564a0-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="564a0-179">RELATED LINKS</span></span>
