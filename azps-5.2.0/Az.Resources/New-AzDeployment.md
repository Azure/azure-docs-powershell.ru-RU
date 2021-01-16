---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: ad5979d65565107ac071bcaac94bc178b8c36d1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409655"
---
# <span data-ttu-id="5bfb5-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5bfb5-101">New-AzDeployment</span></span>

## <span data-ttu-id="5bfb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bfb5-102">SYNOPSIS</span></span>
<span data-ttu-id="5bfb5-103">Создание развертывания</span><span class="sxs-lookup"><span data-stu-id="5bfb5-103">Create a deployment</span></span>

## <span data-ttu-id="5bfb5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5bfb5-104">SYNTAX</span></span>

### <span data-ttu-id="5bfb5-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="5bfb5-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5bfb5-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5bfb5-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5bfb5-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5bfb5-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5bfb5-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5bfb5-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5bfb5-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5bfb5-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5bfb5-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5bfb5-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bfb5-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5bfb5-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bfb5-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bfb5-117">DESCRIPTION</span></span>
<span data-ttu-id="5bfb5-118">Этот **cmdlet добавляет** развертывание в текущую область действия подписки.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="5bfb5-119">К ним относятся ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="5bfb5-120">Ресурс Azure — это объект Azure, управляемый пользователем.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="5bfb5-121">Ресурс может быть в группе ресурсов, например сервере базы данных, базе данных, веб-сайте, виртуальной машине или учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="5bfb5-122">Кроме того, это может быть ресурс уровня подписки, например определение роли, определение политики и т. д.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="5bfb5-123">Чтобы добавить ресурсы в группу ресурсов, используйте **new-AzResourceGroupDeployment,** которая создает развертывание в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="5bfb5-124">Для **выполнения нового azDeployment** создается развертывание в текущей области действия подписки, которое развертывает ресурсы на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="5bfb5-125">Чтобы добавить развертывание по подписке, укажите расположение и шаблон.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="5bfb5-126">Расположение указывает Диспетчеру ресурсов Azure, где будут храниться данные развертывания.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="5bfb5-127">Шаблон — это строка JSON, которая содержит отдельные ресурсы для развертывания.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="5bfb5-128">Шаблон содержит заметели параметров для необходимых ресурсов и настраиваемых значений свойств, таких как имена и размеры.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="5bfb5-129">Чтобы использовать настраиваемый шаблон для развертывания, укажите параметр *TemplateFile* или *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="5bfb5-130">У каждого шаблона есть параметры настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="5bfb5-131">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="5bfb5-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5bfb5-132">Кроме того, можно использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="5bfb5-133">Чтобы использовать динамические параметры, введите их в командной области или знак "минус" (-), чтобы указать параметр, и используйте клавишу TAB для циклиального перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="5bfb5-134">Значения параметров шаблона, которые вы вводите в командной подсказке, имеют приоритет над значениями в объекте или файле с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="5bfb5-135">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5bfb5-135">EXAMPLES</span></span>

### <span data-ttu-id="5bfb5-136">Пример 1. Создание развертывания с помощью настраиваемой файла шаблона и параметра</span><span class="sxs-lookup"><span data-stu-id="5bfb5-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="5bfb5-137">Эта команда создает развертывание в текущей области подписки с помощью настраиваемого шаблона и файла шаблона на диске с определенным параметром тегов.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="5bfb5-138">Команда использует параметр *TemplateFile* для указания шаблона, а параметр *TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="5bfb5-139">Параметр *TemplateVersion используется для* указания версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="5bfb5-140">Пример 2. Создание развертывания с помощью настраиваемых объектов шаблонов и файлов параметров</span><span class="sxs-lookup"><span data-stu-id="5bfb5-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="5bfb5-141">Эта команда создает новое развертывание в текущей области действия подписки с помощью настраиваемого шаблона и файла шаблона на диске, преобразованного в формат в памяти.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="5bfb5-142">Первые две команды читают текст файла шаблона на диске и преобразуют его в размер памяти.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="5bfb5-143">Последняя команда использует параметр *TemplateObject* для указания этого параметра hashtable, а *параметр TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="5bfb5-144">Параметр *TemplateVersion используется для* указания версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="5bfb5-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bfb5-145">PARAMETERS</span></span>

### <span data-ttu-id="5bfb5-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bfb5-146">-AsJob</span></span>
<span data-ttu-id="5bfb5-147">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5bfb5-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bfb5-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bfb5-148">-DefaultProfile</span></span>
<span data-ttu-id="5bfb5-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bfb5-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="5bfb5-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="5bfb5-151">Уровень журнала отлагки развертывания.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-151">The deployment debug log level.</span></span>

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

### <span data-ttu-id="5bfb5-152">-Location</span><span class="sxs-lookup"><span data-stu-id="5bfb5-152">-Location</span></span>
<span data-ttu-id="5bfb5-153">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-153">The location to store deployment data.</span></span>

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

### <span data-ttu-id="5bfb5-154">-Name</span><span class="sxs-lookup"><span data-stu-id="5bfb5-154">-Name</span></span>
<span data-ttu-id="5bfb5-155">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-155">The name of the deployment it's going to create.</span></span> <span data-ttu-id="5bfb5-156">Если он не задан, по умолчанию заданное имя файла шаблона при его предоставлении; по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="5bfb5-156">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="5bfb5-157">-Pre</span><span class="sxs-lookup"><span data-stu-id="5bfb5-157">-Pre</span></span>
<span data-ttu-id="5bfb5-158">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-158">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5bfb5-159">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="5bfb5-159">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="5bfb5-160">Пропускает динамическую обработку параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-160">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="5bfb5-161">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-161">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="5bfb5-162">Для неинтерационных сценариев можно предоставить функцию SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-162">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="5bfb5-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="5bfb5-163">-Tag</span></span>
<span data-ttu-id="5bfb5-164">Теги для развертывания.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-164">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="5bfb5-165">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5bfb5-165">-TemplateFile</span></span>
<span data-ttu-id="5bfb5-166">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-166">Local path to the template file.</span></span>

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

### <span data-ttu-id="5bfb5-167">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="5bfb5-167">-TemplateObject</span></span>
<span data-ttu-id="5bfb5-168">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-168">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="5bfb5-169">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5bfb5-169">-TemplateParameterFile</span></span>
<span data-ttu-id="5bfb5-170">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-170">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="5bfb5-171">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="5bfb5-171">-TemplateParameterObject</span></span>
<span data-ttu-id="5bfb5-172">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-172">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="5bfb5-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="5bfb5-173">-TemplateParameterUri</span></span>
<span data-ttu-id="5bfb5-174">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-174">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="5bfb5-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="5bfb5-175">-TemplateUri</span></span>
<span data-ttu-id="5bfb5-176">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-176">Uri to the template file.</span></span>

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

### <span data-ttu-id="5bfb5-177">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="5bfb5-177">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="5bfb5-178">Типы изменений ресурсов, разделенные запятой, которые следует исключить из What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-178">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="5bfb5-179">Применимо, если за установлен переключатель -WhatIf или -Confirm.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="5bfb5-180">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="5bfb5-180">-WhatIfResultFormat</span></span>
<span data-ttu-id="5bfb5-181">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-181">The What-If result format.</span></span>

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

### <span data-ttu-id="5bfb5-182">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bfb5-182">-Confirm</span></span>
<span data-ttu-id="5bfb5-183">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bfb5-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bfb5-184">-WhatIf</span></span>
<span data-ttu-id="5bfb5-185">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bfb5-186">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bfb5-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bfb5-187">CommonParameters</span></span>
<span data-ttu-id="5bfb5-188">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bfb5-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bfb5-189">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bfb5-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bfb5-190">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bfb5-190">INPUTS</span></span>

### <span data-ttu-id="5bfb5-191">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5bfb5-191">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5bfb5-192">System.String</span><span class="sxs-lookup"><span data-stu-id="5bfb5-192">System.String</span></span>

## <span data-ttu-id="5bfb5-193">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5bfb5-193">OUTPUTS</span></span>

### <span data-ttu-id="5bfb5-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="5bfb5-194">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5bfb5-195">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5bfb5-195">NOTES</span></span>

## <span data-ttu-id="5bfb5-196">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bfb5-196">RELATED LINKS</span></span>