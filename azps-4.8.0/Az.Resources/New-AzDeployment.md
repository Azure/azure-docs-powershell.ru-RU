---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 56be1071c2a6307bee28f0ce4cf13dde626df72e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077664"
---
# <span data-ttu-id="75ace-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="75ace-101">New-AzDeployment</span></span>

## <span data-ttu-id="75ace-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75ace-102">SYNOPSIS</span></span>
<span data-ttu-id="75ace-103">Создание развертывания</span><span class="sxs-lookup"><span data-stu-id="75ace-103">Create a deployment</span></span>

## <span data-ttu-id="75ace-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75ace-104">SYNTAX</span></span>

### <span data-ttu-id="75ace-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75ace-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ace-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="75ace-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ace-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="75ace-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ace-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="75ace-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ace-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="75ace-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ace-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="75ace-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ace-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="75ace-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ace-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="75ace-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ace-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="75ace-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ace-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="75ace-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ace-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="75ace-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ace-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="75ace-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ace-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75ace-117">DESCRIPTION</span></span>
<span data-ttu-id="75ace-118">Командлет **New-AzDeployment** добавляет развертывание в текущую область подписки.</span><span class="sxs-lookup"><span data-stu-id="75ace-118">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="75ace-119">Сюда входят ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="75ace-119">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="75ace-120">Ресурс Azure — это управляемая пользователем сущность Azure.</span><span class="sxs-lookup"><span data-stu-id="75ace-120">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="75ace-121">Ресурс может находиться в группе ресурсов, например на сервере базы данных, базе данных, веб-сайте, виртуальной машине или учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="75ace-121">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="75ace-122">Или это может быть ресурс уровня подписки, например определение роли, определение политики и т. д.</span><span class="sxs-lookup"><span data-stu-id="75ace-122">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="75ace-123">Чтобы добавить ресурсы в группу ресурсов, используйте **New-AzResourceGroupDeployment** , который создает развертывание в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75ace-123">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="75ace-124">Командлет **New-AzDeployment** создает развертывание в текущей области подписки, которое развертывает ресурсы уровня подписки.</span><span class="sxs-lookup"><span data-stu-id="75ace-124">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="75ace-125">Чтобы добавить развертывание на подписку, укажите расположение и шаблон.</span><span class="sxs-lookup"><span data-stu-id="75ace-125">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="75ace-126">Расположение указывает диспетчеру ресурсов Azure, где хранятся данные развертывания.</span><span class="sxs-lookup"><span data-stu-id="75ace-126">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="75ace-127">Шаблон — это строка JSON, содержащая отдельные ресурсы для развертывания.</span><span class="sxs-lookup"><span data-stu-id="75ace-127">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="75ace-128">Шаблон включает заполнители параметров для необходимых ресурсов и настраиваемых значений свойств, например имен и размеров.</span><span class="sxs-lookup"><span data-stu-id="75ace-128">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="75ace-129">Чтобы использовать настраиваемый шаблон для развертывания, укажите параметр *TemplateFile* или *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="75ace-129">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="75ace-130">Каждый шаблон имеет параметры для настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="75ace-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="75ace-131">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или параметр *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="75ace-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="75ace-132">Кроме того, вы можете использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="75ace-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="75ace-133">Чтобы использовать динамические параметры, введите их в командной строке или введите знак "минус" (-), чтобы обозначить параметр, и используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="75ace-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="75ace-134">Значения параметров шаблона, введенные в командной строке, имеют приоритет над значениями в объекте или файле параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="75ace-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="75ace-135">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75ace-135">EXAMPLES</span></span>

### <span data-ttu-id="75ace-136">Пример 1: использование настраиваемого шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="75ace-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="75ace-137">Эта команда создает новое развертывание в текущей области подписки с помощью настраиваемого шаблона и файла шаблона на диске с параметром "Теги".</span><span class="sxs-lookup"><span data-stu-id="75ace-137">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="75ace-138">В команде используется параметр *TemplateFile* , чтобы указать шаблон и параметр *TemplateParameterFile* , чтобы указать файл, содержащий параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="75ace-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="75ace-139">Для указания версии шаблона используется параметр *TemplateVersion* .</span><span class="sxs-lookup"><span data-stu-id="75ace-139">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="75ace-140">Пример 2: использование настраиваемого объекта шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="75ace-140">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="75ace-141">Эта команда создает новое развертывание в текущей области подписки с помощью настраиваемого шаблона и файла шаблона на диске, преобразованного в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="75ace-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="75ace-142">Первые две команды считывают текст файла шаблона на диске и преобразуют его в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="75ace-142">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="75ace-143">Последняя команда использует параметр *TemplateObject* , чтобы указать эту хэш-таблицу, а параметр *TemplateParameterFile* — для указания файла, содержащего параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="75ace-143">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="75ace-144">Для указания версии шаблона используется параметр *TemplateVersion* .</span><span class="sxs-lookup"><span data-stu-id="75ace-144">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="75ace-145">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75ace-145">PARAMETERS</span></span>

### <span data-ttu-id="75ace-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="75ace-146">-ApiVersion</span></span>
<span data-ttu-id="75ace-147">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75ace-147">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="75ace-148">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="75ace-148">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="75ace-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75ace-149">-AsJob</span></span>
<span data-ttu-id="75ace-150">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="75ace-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="75ace-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ace-151">-DefaultProfile</span></span>
<span data-ttu-id="75ace-152">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75ace-152">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75ace-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="75ace-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="75ace-154">Уровень журнала отладки развертывания.</span><span class="sxs-lookup"><span data-stu-id="75ace-154">The deployment debug log level.</span></span>

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

### <span data-ttu-id="75ace-155">-Location</span><span class="sxs-lookup"><span data-stu-id="75ace-155">-Location</span></span>
<span data-ttu-id="75ace-156">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="75ace-156">The location to store deployment data.</span></span>

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

### <span data-ttu-id="75ace-157">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75ace-157">-Name</span></span>
<span data-ttu-id="75ace-158">Имя развертывания, которое будет создано.</span><span class="sxs-lookup"><span data-stu-id="75ace-158">The name of the deployment it's going to create.</span></span> <span data-ttu-id="75ace-159">Если не указано, по умолчанию используется имя файла шаблона, когда указан файл шаблона; по умолчанию — текущее время, когда указан объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="75ace-159">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="75ace-160">-Pre</span><span class="sxs-lookup"><span data-stu-id="75ace-160">-Pre</span></span>
<span data-ttu-id="75ace-161">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="75ace-161">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="75ace-162">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="75ace-162">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="75ace-163">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="75ace-163">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="75ace-164">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="75ace-164">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="75ace-165">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="75ace-165">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="75ace-166">-Тег</span><span class="sxs-lookup"><span data-stu-id="75ace-166">-Tag</span></span>
<span data-ttu-id="75ace-167">Теги, помещаемые в развертывание.</span><span class="sxs-lookup"><span data-stu-id="75ace-167">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="75ace-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="75ace-168">-TemplateFile</span></span>
<span data-ttu-id="75ace-169">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="75ace-169">Local path to the template file.</span></span>

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

### <span data-ttu-id="75ace-170">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="75ace-170">-TemplateObject</span></span>
<span data-ttu-id="75ace-171">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="75ace-171">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="75ace-172">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="75ace-172">-TemplateParameterFile</span></span>
<span data-ttu-id="75ace-173">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="75ace-173">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="75ace-174">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="75ace-174">-TemplateParameterObject</span></span>
<span data-ttu-id="75ace-175">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="75ace-175">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="75ace-176">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="75ace-176">-TemplateParameterUri</span></span>
<span data-ttu-id="75ace-177">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="75ace-177">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="75ace-178">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="75ace-178">-TemplateUri</span></span>
<span data-ttu-id="75ace-179">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="75ace-179">Uri to the template file.</span></span>

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

### <span data-ttu-id="75ace-180">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="75ace-180">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="75ace-181">Типы изменения ресурсов, разделенные запятыми, которые будут исключены из результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="75ace-181">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="75ace-182">Применимо, если установлен параметр-WhatIf или-Confirm.</span><span class="sxs-lookup"><span data-stu-id="75ace-182">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="75ace-183">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="75ace-183">-WhatIfResultFormat</span></span>
<span data-ttu-id="75ace-184">Формат результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="75ace-184">The What-If result format.</span></span>

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

### <span data-ttu-id="75ace-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75ace-185">-Confirm</span></span>
<span data-ttu-id="75ace-186">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75ace-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75ace-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ace-187">-WhatIf</span></span>
<span data-ttu-id="75ace-188">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75ace-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75ace-189">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75ace-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75ace-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ace-190">CommonParameters</span></span>
<span data-ttu-id="75ace-191">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75ace-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ace-192">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75ace-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ace-193">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75ace-193">INPUTS</span></span>

### <span data-ttu-id="75ace-194">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="75ace-194">System.Collections.Hashtable</span></span>

### <span data-ttu-id="75ace-195">System. String</span><span class="sxs-lookup"><span data-stu-id="75ace-195">System.String</span></span>

## <span data-ttu-id="75ace-196">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75ace-196">OUTPUTS</span></span>

### <span data-ttu-id="75ace-197">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="75ace-197">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="75ace-198">Пуск</span><span class="sxs-lookup"><span data-stu-id="75ace-198">NOTES</span></span>

## <span data-ttu-id="75ace-199">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75ace-199">RELATED LINKS</span></span>
