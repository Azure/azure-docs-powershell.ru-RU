---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 42f68065fb5a1785d0f9a243d0165bc72125743d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953080"
---
# <span data-ttu-id="5ce63-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="5ce63-101">New-AzDeployment</span></span>

## <span data-ttu-id="5ce63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ce63-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce63-103">Создание развертывания</span><span class="sxs-lookup"><span data-stu-id="5ce63-103">Create a deployment</span></span>

## <span data-ttu-id="5ce63-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ce63-104">SYNTAX</span></span>

### <span data-ttu-id="5ce63-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ce63-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce63-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5ce63-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce63-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5ce63-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce63-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="5ce63-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce63-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="5ce63-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce63-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5ce63-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce63-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5ce63-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce63-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="5ce63-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce63-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="5ce63-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce63-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5ce63-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ce63-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5ce63-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce63-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="5ce63-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce63-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="5ce63-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce63-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5ce63-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce63-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="5ce63-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce63-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="5ce63-120">ByTemplateSpecResourceId</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>]
 [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-AsJob]
 [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ce63-121">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ce63-121">DESCRIPTION</span></span>
<span data-ttu-id="5ce63-122">Этот **cmdlet добавляет** развертывание в текущую область действия подписки.</span><span class="sxs-lookup"><span data-stu-id="5ce63-122">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="5ce63-123">К ним относятся ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="5ce63-123">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="5ce63-124">Ресурс Azure — это объект Azure, управляемый пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ce63-124">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="5ce63-125">Ресурс может быть в группе ресурсов, например на сервере базы данных, базе данных, веб-сайте, виртуальной машине или учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5ce63-125">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="5ce63-126">Кроме того, это может быть ресурс уровня подписки, например определение роли, определение политики и т. д.</span><span class="sxs-lookup"><span data-stu-id="5ce63-126">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="5ce63-127">Чтобы добавить ресурсы в группу ресурсов, используйте **new-AzResourceGroupDeployment,** которая создает развертывание в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ce63-127">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="5ce63-128">Для **выполнения нового azDeployment** создается развертывание в текущей области действия подписки, которое развертывает ресурсы на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="5ce63-128">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span>

<span data-ttu-id="5ce63-129">Чтобы добавить развертывание в подписку, укажите расположение и шаблон.</span><span class="sxs-lookup"><span data-stu-id="5ce63-129">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="5ce63-130">Расположение указывает Диспетчеру ресурсов Azure, где будут храниться данные развертывания.</span><span class="sxs-lookup"><span data-stu-id="5ce63-130">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="5ce63-131">Шаблон — это строка JSON, которая содержит отдельные ресурсы для развертывания.</span><span class="sxs-lookup"><span data-stu-id="5ce63-131">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="5ce63-132">Шаблон содержит заметели параметров для необходимых ресурсов и настраиваемых значений свойств, таких как имена и размеры.</span><span class="sxs-lookup"><span data-stu-id="5ce63-132">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="5ce63-133">Чтобы использовать настраиваемый шаблон для развертывания, укажите параметр *TemplateFile* или *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="5ce63-133">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="5ce63-134">У каждого шаблона есть параметры настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="5ce63-134">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="5ce63-135">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="5ce63-135">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="5ce63-136">Кроме того, можно использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="5ce63-136">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="5ce63-137">Чтобы использовать динамические параметры, введите их в командной области или знак "минус" (-), чтобы указать параметр, и используйте клавишу TAB для циклиального перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="5ce63-137">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="5ce63-138">Значения параметров шаблона, которые вы вводите в командной подсказке, имеют приоритет над значениями в объекте или файле с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="5ce63-138">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="5ce63-139">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ce63-139">EXAMPLES</span></span>

### <span data-ttu-id="5ce63-140">Пример 1. Создание развертывания с помощью настраиваемой файла шаблона и параметра</span><span class="sxs-lookup"><span data-stu-id="5ce63-140">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="5ce63-141">Эта команда создает развертывание в текущей области подписки с помощью настраиваемого шаблона и файла шаблона на диске с определенным параметром тегов.</span><span class="sxs-lookup"><span data-stu-id="5ce63-141">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="5ce63-142">Команда использует параметр *TemplateFile* для указания шаблона, а параметр *TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="5ce63-142">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="5ce63-143">Параметр *TemplateVersion используется для* указания версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="5ce63-143">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

### <span data-ttu-id="5ce63-144">Пример 2. Развертывание шаблона, храняного в неугодной учетной записи хранения, с помощью маркера URI и SAS</span><span class="sxs-lookup"><span data-stu-id="5ce63-144">Example 2: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```
PS C:\> New-AzDeployment -Location "West US" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="5ce63-145">Эта команда создает развертывание с использованием шаблона TemplateUri, который не является общедоступным и требует на доступ параметра token, который будет предоставляться с помощью параметра QueryString.</span><span class="sxs-lookup"><span data-stu-id="5ce63-145">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="5ce63-146">Эта команда будет эффективно работать с шаблоном по https://example.com/example.json?foo URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="5ce63-146">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="5ce63-147">Это может быть использовано, если вы хотите использовать шаблон в учетной записи хранения, предоставляя токен SAS в качестве QueryString.</span><span class="sxs-lookup"><span data-stu-id="5ce63-147">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

### <span data-ttu-id="5ce63-148">Пример 3. Создание развертывания с помощью настраиваемых объектов шаблонов и файлов параметров</span><span class="sxs-lookup"><span data-stu-id="5ce63-148">Example 3: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json" -TemplateVersion "2.1"
```

<span data-ttu-id="5ce63-149">Эта команда создает новое развертывание в текущей области действия подписки с помощью настраиваемого шаблона и файла шаблона на диске, преобразованного в формат в памяти.</span><span class="sxs-lookup"><span data-stu-id="5ce63-149">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="5ce63-150">Первые две команды читают текст файла шаблона на диске и преобразуют его в размер памяти.</span><span class="sxs-lookup"><span data-stu-id="5ce63-150">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="5ce63-151">Последняя команда использует параметр *TemplateObject* для указания этого параметра hashtable, а *параметр TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="5ce63-151">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="5ce63-152">Параметр *TemplateVersion используется для* указания версии шаблона.</span><span class="sxs-lookup"><span data-stu-id="5ce63-152">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="5ce63-153">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ce63-153">PARAMETERS</span></span>

### <span data-ttu-id="5ce63-154">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ce63-154">-AsJob</span></span>
<span data-ttu-id="5ce63-155">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5ce63-155">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ce63-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce63-156">-DefaultProfile</span></span>
<span data-ttu-id="5ce63-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ce63-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ce63-158">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="5ce63-158">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="5ce63-159">Уровень журнала отлагки развертывания.</span><span class="sxs-lookup"><span data-stu-id="5ce63-159">The deployment debug log level.</span></span>

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

### <span data-ttu-id="5ce63-160">-Location</span><span class="sxs-lookup"><span data-stu-id="5ce63-160">-Location</span></span>
<span data-ttu-id="5ce63-161">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="5ce63-161">The location to store deployment data.</span></span>

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

### <span data-ttu-id="5ce63-162">-Name</span><span class="sxs-lookup"><span data-stu-id="5ce63-162">-Name</span></span>
<span data-ttu-id="5ce63-163">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="5ce63-163">The name of the deployment it's going to create.</span></span> <span data-ttu-id="5ce63-164">Если не указано иное, по умолчанию имя файла шаблона задано при его указании. по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="5ce63-164">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="5ce63-165">-Pre</span><span class="sxs-lookup"><span data-stu-id="5ce63-165">-Pre</span></span>
<span data-ttu-id="5ce63-166">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="5ce63-166">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5ce63-167">-QueryString</span><span class="sxs-lookup"><span data-stu-id="5ce63-167">-QueryString</span></span>
<span data-ttu-id="5ce63-168">Строка запроса (например, токен SAS), которая будет использоваться с параметром TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="5ce63-168">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="5ce63-169">Будет использоваться в случае связанных шаблонов</span><span class="sxs-lookup"><span data-stu-id="5ce63-169">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="5ce63-170">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="5ce63-170">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="5ce63-171">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="5ce63-171">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="5ce63-172">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="5ce63-172">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="5ce63-173">Для неинтерационных сценариев можно предоставить функцию SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="5ce63-173">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="5ce63-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ce63-174">-Tag</span></span>
<span data-ttu-id="5ce63-175">Теги для развертывания.</span><span class="sxs-lookup"><span data-stu-id="5ce63-175">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="5ce63-176">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="5ce63-176">-TemplateFile</span></span>
<span data-ttu-id="5ce63-177">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="5ce63-177">Local path to the template file.</span></span> <span data-ttu-id="5ce63-178">Поддерживаемый тип файла шаблона: json и bicep.</span><span class="sxs-lookup"><span data-stu-id="5ce63-178">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="5ce63-179">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="5ce63-179">-TemplateObject</span></span>
<span data-ttu-id="5ce63-180">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="5ce63-180">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="5ce63-181">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="5ce63-181">-TemplateParameterFile</span></span>
<span data-ttu-id="5ce63-182">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="5ce63-182">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="5ce63-183">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="5ce63-183">-TemplateParameterObject</span></span>
<span data-ttu-id="5ce63-184">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="5ce63-184">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="5ce63-185">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="5ce63-185">-TemplateParameterUri</span></span>
<span data-ttu-id="5ce63-186">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="5ce63-186">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="5ce63-187">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="5ce63-187">-TemplateSpecId</span></span>
<span data-ttu-id="5ce63-188">ИД ресурса шаблонаSpec, который нужно развернуть.</span><span class="sxs-lookup"><span data-stu-id="5ce63-188">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="5ce63-189">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="5ce63-189">-TemplateUri</span></span>
<span data-ttu-id="5ce63-190">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="5ce63-190">Uri to the template file.</span></span>

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

### <span data-ttu-id="5ce63-191">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="5ce63-191">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="5ce63-192">Типы изменений ресурсов, разделенные запятой, которые следует исключить из What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="5ce63-192">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="5ce63-193">Применимо, если за установлен переключатель -WhatIf или -Confirm.</span><span class="sxs-lookup"><span data-stu-id="5ce63-193">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="5ce63-194">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="5ce63-194">-WhatIfResultFormat</span></span>
<span data-ttu-id="5ce63-195">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="5ce63-195">The What-If result format.</span></span>

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

### <span data-ttu-id="5ce63-196">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ce63-196">-Confirm</span></span>
<span data-ttu-id="5ce63-197">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ce63-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ce63-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce63-198">-WhatIf</span></span>
<span data-ttu-id="5ce63-199">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ce63-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ce63-200">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5ce63-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ce63-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce63-201">CommonParameters</span></span>
<span data-ttu-id="5ce63-202">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ce63-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce63-203">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ce63-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce63-204">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ce63-204">INPUTS</span></span>

### <span data-ttu-id="5ce63-205">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5ce63-205">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5ce63-206">System.String</span><span class="sxs-lookup"><span data-stu-id="5ce63-206">System.String</span></span>

## <span data-ttu-id="5ce63-207">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ce63-207">OUTPUTS</span></span>

### <span data-ttu-id="5ce63-208">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="5ce63-208">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5ce63-209">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ce63-209">NOTES</span></span>

## <span data-ttu-id="5ce63-210">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ce63-210">RELATED LINKS</span></span>
