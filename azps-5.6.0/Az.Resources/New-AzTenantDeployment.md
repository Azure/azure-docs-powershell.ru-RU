---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 029e1342caeac078d98418cfc508051b04dd816f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999816"
---
# <span data-ttu-id="8ad87-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8ad87-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="8ad87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ad87-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad87-103">Создание развертывания в области клиента</span><span class="sxs-lookup"><span data-stu-id="8ad87-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="8ad87-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ad87-104">SYNTAX</span></span>

### <span data-ttu-id="8ad87-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ad87-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad87-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8ad87-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad87-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8ad87-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad87-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8ad87-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad87-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="8ad87-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad87-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8ad87-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad87-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8ad87-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad87-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8ad87-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad87-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="8ad87-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad87-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8ad87-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ad87-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8ad87-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad87-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8ad87-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad87-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="8ad87-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad87-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8ad87-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad87-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8ad87-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ad87-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="8ad87-120">ByTemplateSpecResourceId</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ad87-121">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ad87-121">DESCRIPTION</span></span>
<span data-ttu-id="8ad87-122">Для развертывания в текущей области клиента добавляется новый **cmdlet AzTenantDeployment.**</span><span class="sxs-lookup"><span data-stu-id="8ad87-122">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="8ad87-123">Чтобы добавить развертывание в клиенте, укажите расположение и шаблон.</span><span class="sxs-lookup"><span data-stu-id="8ad87-123">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="8ad87-124">Расположение указывает Диспетчеру ресурсов Azure, где будут храниться данные развертывания.</span><span class="sxs-lookup"><span data-stu-id="8ad87-124">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="8ad87-125">Шаблон — это строка JSON, которая содержит отдельные ресурсы для развертывания.</span><span class="sxs-lookup"><span data-stu-id="8ad87-125">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="8ad87-126">Шаблон содержит заме желтую параметров для требуемых ресурсов и настраиваемых значений свойств, таких как имена и размеры.</span><span class="sxs-lookup"><span data-stu-id="8ad87-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="8ad87-127">Чтобы использовать настраиваемый шаблон для развертывания, укажите параметр *TemplateFile* или *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="8ad87-127">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="8ad87-128">У каждого шаблона есть параметры настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="8ad87-128">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="8ad87-129">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="8ad87-129">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="8ad87-130">Кроме того, можно использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="8ad87-130">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="8ad87-131">Чтобы использовать динамические параметры, введите их в командной области или знак "минус" (-), чтобы указать параметр, и используйте клавишу TAB для циклиального перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="8ad87-131">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="8ad87-132">Значения параметров шаблона, которые вы вводите в командной области, имеют приоритет над значениями в объекте или файле с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="8ad87-132">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="8ad87-133">Чтобы добавить ресурсы в группу ресурсов, используйте **new-AzResourceGroupDeployment,** которая создает развертывание в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ad87-133">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="8ad87-134">Чтобы добавить ресурсы в подписку, используйте **new-AzSubscriptionDeployment,** которая создает развертывание в рамках подписки, которое развертывает ресурсы на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="8ad87-134">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="8ad87-135">Чтобы добавить ресурсы в группу управления, используйте **new-AzManagementGroupDeployment,** которая создает развертывание в группе управления.</span><span class="sxs-lookup"><span data-stu-id="8ad87-135">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="8ad87-136">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ad87-136">EXAMPLES</span></span>

### <span data-ttu-id="8ad87-137">Пример 1. Создание развертывания с помощью настраиваемой файла шаблона и параметра</span><span class="sxs-lookup"><span data-stu-id="8ad87-137">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="8ad87-138">Эта команда создает новое развертывание в текущей области клиента с использованием настраиваемого шаблона и файла шаблона на диске с определенным параметром тегов.</span><span class="sxs-lookup"><span data-stu-id="8ad87-138">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="8ad87-139">Команда использует параметр *TemplateFile* для указания шаблона, а параметр *TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="8ad87-139">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="8ad87-140">Пример 2. Создание развертывания с помощью настраиваемых объектов шаблонов и файлов параметров</span><span class="sxs-lookup"><span data-stu-id="8ad87-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="8ad87-141">Эта команда создает новое развертывание в текущем клиенте на основе настраиваемого шаблона и файла шаблона на диске, преобразованного в формат в памяти.</span><span class="sxs-lookup"><span data-stu-id="8ad87-141">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="8ad87-142">Первые две команды читают текст файла шаблона на диске и преобразуют его в размер памяти.</span><span class="sxs-lookup"><span data-stu-id="8ad87-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="8ad87-143">Последняя команда использует параметр *TemplateObject* для указания этого параметра hashtable, а *параметр TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="8ad87-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="8ad87-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ad87-144">PARAMETERS</span></span>

### <span data-ttu-id="8ad87-145">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ad87-145">-AsJob</span></span>
<span data-ttu-id="8ad87-146">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8ad87-146">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ad87-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad87-147">-DefaultProfile</span></span>
<span data-ttu-id="8ad87-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad87-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ad87-149">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="8ad87-149">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="8ad87-150">Уровень журнала отлагки развертывания.</span><span class="sxs-lookup"><span data-stu-id="8ad87-150">The deployment debug log level.</span></span>

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

### <span data-ttu-id="8ad87-151">-Location</span><span class="sxs-lookup"><span data-stu-id="8ad87-151">-Location</span></span>
<span data-ttu-id="8ad87-152">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="8ad87-152">The location to store deployment data.</span></span>

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

### <span data-ttu-id="8ad87-153">-Name</span><span class="sxs-lookup"><span data-stu-id="8ad87-153">-Name</span></span>
<span data-ttu-id="8ad87-154">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="8ad87-154">The name of the deployment it's going to create.</span></span> <span data-ttu-id="8ad87-155">Если не указано иное, по умолчанию имя файла шаблона задано при его указании. по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="8ad87-155">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="8ad87-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="8ad87-156">-Pre</span></span>
<span data-ttu-id="8ad87-157">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="8ad87-157">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8ad87-158">-QueryString</span><span class="sxs-lookup"><span data-stu-id="8ad87-158">-QueryString</span></span>
<span data-ttu-id="8ad87-159">Строка запроса (например, токен SAS), которая будет использоваться с параметром TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="8ad87-159">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="8ad87-160">Будет использоваться в случае связанных шаблонов</span><span class="sxs-lookup"><span data-stu-id="8ad87-160">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="8ad87-161">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="8ad87-161">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="8ad87-162">Пропускает динамическую обработку параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="8ad87-162">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="8ad87-163">При проверке пользователю будет предложено в качестве значения пропустить отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не был привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="8ad87-163">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="8ad87-164">Для неинтерационных сценариев можно использовать параметр SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="8ad87-164">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="8ad87-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="8ad87-165">-Tag</span></span>
<span data-ttu-id="8ad87-166">Теги для развертывания.</span><span class="sxs-lookup"><span data-stu-id="8ad87-166">The tags to put on the deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad87-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8ad87-167">-TemplateFile</span></span>
<span data-ttu-id="8ad87-168">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="8ad87-168">Local path to the template file.</span></span> <span data-ttu-id="8ad87-169">Поддерживаемый тип файла шаблона: json и bicep.</span><span class="sxs-lookup"><span data-stu-id="8ad87-169">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="8ad87-170">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="8ad87-170">-TemplateObject</span></span>
<span data-ttu-id="8ad87-171">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="8ad87-171">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="8ad87-172">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8ad87-172">-TemplateParameterFile</span></span>
<span data-ttu-id="8ad87-173">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="8ad87-173">A file that has the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile, ByTemplateSpecResourceIdAndParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad87-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8ad87-174">-TemplateParameterObject</span></span>
<span data-ttu-id="8ad87-175">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="8ad87-175">A hash table which represents the parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject, ByTemplateSpecResourceIdAndParamsObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad87-176">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8ad87-176">-TemplateParameterUri</span></span>
<span data-ttu-id="8ad87-177">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="8ad87-177">Uri to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri, ByTemplateSpecResourceIdAndParamsUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad87-178">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="8ad87-178">-TemplateSpecId</span></span>
<span data-ttu-id="8ad87-179">ИД ресурса шаблонаSpec, который нужно развернуть.</span><span class="sxs-lookup"><span data-stu-id="8ad87-179">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParamsObject, ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ad87-180">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8ad87-180">-TemplateUri</span></span>
<span data-ttu-id="8ad87-181">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="8ad87-181">Uri to the template file.</span></span>

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

### <span data-ttu-id="8ad87-182">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="8ad87-182">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="8ad87-183">Типы изменений ресурсов, разделенные запятой, которые следует исключить из What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="8ad87-183">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="8ad87-184">Применимо, если за установлен переключатель -WhatIf или -Confirm.</span><span class="sxs-lookup"><span data-stu-id="8ad87-184">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="8ad87-185">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="8ad87-185">-WhatIfResultFormat</span></span>
<span data-ttu-id="8ad87-186">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="8ad87-186">The What-If result format.</span></span> <span data-ttu-id="8ad87-187">Применимо, если за установлен переключатель -WhatIf или -Confirm.</span><span class="sxs-lookup"><span data-stu-id="8ad87-187">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="8ad87-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ad87-188">-Confirm</span></span>
<span data-ttu-id="8ad87-189">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8ad87-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ad87-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ad87-190">-WhatIf</span></span>
<span data-ttu-id="8ad87-191">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ad87-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ad87-192">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ad87-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ad87-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad87-193">CommonParameters</span></span>
<span data-ttu-id="8ad87-194">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ad87-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad87-195">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ad87-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad87-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ad87-196">INPUTS</span></span>

### <span data-ttu-id="8ad87-197">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8ad87-197">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8ad87-198">System.String</span><span class="sxs-lookup"><span data-stu-id="8ad87-198">System.String</span></span>

## <span data-ttu-id="8ad87-199">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ad87-199">OUTPUTS</span></span>

### <span data-ttu-id="8ad87-200">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="8ad87-200">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8ad87-201">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ad87-201">NOTES</span></span>

## <span data-ttu-id="8ad87-202">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ad87-202">RELATED LINKS</span></span>
