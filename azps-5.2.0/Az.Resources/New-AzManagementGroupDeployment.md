---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupDeployment.md
ms.openlocfilehash: a04c19df84626fd08968e1950074306dfd7cf1ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409644"
---
# <span data-ttu-id="67a79-101">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="67a79-101">New-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="67a79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a79-102">SYNOPSIS</span></span>
<span data-ttu-id="67a79-103">Создание развертывания в группе управления</span><span class="sxs-lookup"><span data-stu-id="67a79-103">Create a deployment at a management group</span></span>

## <span data-ttu-id="67a79-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67a79-104">SYNTAX</span></span>

### <span data-ttu-id="67a79-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="67a79-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67a79-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="67a79-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67a79-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="67a79-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67a79-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="67a79-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67a79-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="67a79-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67a79-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="67a79-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67a79-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="67a79-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67a79-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="67a79-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67a79-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="67a79-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67a79-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="67a79-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67a79-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="67a79-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67a79-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="67a79-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzManagementGroupDeployment [-Name <String>] -ManagementGroupId <String> -Location <String>
 [-DeploymentDebugLogLevel <String>] [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>]
 [-WhatIfExcludeChangeType <String[]>] [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67a79-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67a79-117">DESCRIPTION</span></span>
<span data-ttu-id="67a79-118">Для развертывания в группе управления будет добавлена группа **New-AzManagementGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="67a79-118">The **New-AzManagementGroupDeployment** cmdlet adds a deployment at a management group.</span></span>

<span data-ttu-id="67a79-119">Чтобы добавить развертывание в группу управления, укажите группу управления, расположение и шаблон.</span><span class="sxs-lookup"><span data-stu-id="67a79-119">To add a deployment at a management group, specify the management group, location and a template.</span></span>
<span data-ttu-id="67a79-120">Расположение указывает Диспетчеру ресурсов Azure, где будут храниться данные развертывания.</span><span class="sxs-lookup"><span data-stu-id="67a79-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="67a79-121">Шаблон — это строка JSON, которая содержит отдельные ресурсы для развертывания.</span><span class="sxs-lookup"><span data-stu-id="67a79-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="67a79-122">Шаблон содержит заме желтую параметров для требуемых ресурсов и настраиваемых значений свойств, таких как имена и размеры.</span><span class="sxs-lookup"><span data-stu-id="67a79-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="67a79-123">Чтобы использовать настраиваемый шаблон для развертывания, укажите параметр *TemplateFile* или *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="67a79-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="67a79-124">У каждого шаблона есть параметры настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="67a79-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="67a79-125">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="67a79-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="67a79-126">Кроме того, можно использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="67a79-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="67a79-127">Чтобы использовать динамические параметры, введите их в командной области или знак "минус" (-), чтобы указать параметр, и используйте клавишу TAB для циклиального перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="67a79-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="67a79-128">Значения параметров шаблона, которые вы вводите в командной области, имеют приоритет над значениями в объекте или файле с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="67a79-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="67a79-129">Чтобы добавить ресурсы в группу ресурсов, используйте **new-AzResourceGroupDeployment,** которая создает развертывание в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67a79-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="67a79-130">Чтобы добавить ресурсы в подписку, используйте **new-AzSubscriptionDeployment,** которая создает развертывание в рамках подписки, которое развертывает ресурсы на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="67a79-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="67a79-131">Чтобы добавить ресурсы в область клиента, используйте **new-AzTenantDeployment,** которая создает развертывание в области клиента.</span><span class="sxs-lookup"><span data-stu-id="67a79-131">To add resources at tenant scope, use the **New-AzTenantDeployment** which creates a deployment at tenant scope.</span></span>

## <span data-ttu-id="67a79-132">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67a79-132">EXAMPLES</span></span>

### <span data-ttu-id="67a79-133">Пример 1. Создание развертывания с помощью настраиваемой файла шаблона и параметра</span><span class="sxs-lookup"><span data-stu-id="67a79-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="67a79-134">Эта команда создает развертывание в группе управления MyMG с использованием настраиваемого шаблона и файла шаблона на диске с определенным параметром тегов.</span><span class="sxs-lookup"><span data-stu-id="67a79-134">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="67a79-135">Команда использует параметр *TemplateFile* для указания шаблона, а параметр *TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="67a79-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="67a79-136">Пример 2. Создание развертывания с помощью настраиваемых объектов шаблонов и файлов параметров</span><span class="sxs-lookup"><span data-stu-id="67a79-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="67a79-137">Эта команда создает развертывание в группе управления MyMG на основе настраиваемого шаблона и файла шаблона на диске, преобразованного в формат в памяти.</span><span class="sxs-lookup"><span data-stu-id="67a79-137">This command creates a new deployment at the management group "myMG" by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="67a79-138">Первые две команды читают текст файла шаблона на диске и преобразуют его в размер памяти.</span><span class="sxs-lookup"><span data-stu-id="67a79-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="67a79-139">Последняя команда использует параметр *TemplateObject* для указания этого параметра hashtable, а *параметр TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="67a79-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="67a79-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67a79-140">PARAMETERS</span></span>

### <span data-ttu-id="67a79-141">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67a79-141">-AsJob</span></span>
<span data-ttu-id="67a79-142">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="67a79-142">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67a79-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a79-143">-DefaultProfile</span></span>
<span data-ttu-id="67a79-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67a79-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67a79-145">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="67a79-145">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="67a79-146">Уровень журнала отлагки развертывания.</span><span class="sxs-lookup"><span data-stu-id="67a79-146">The deployment debug log level.</span></span>

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

### <span data-ttu-id="67a79-147">-Location</span><span class="sxs-lookup"><span data-stu-id="67a79-147">-Location</span></span>
<span data-ttu-id="67a79-148">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="67a79-148">The location to store deployment data.</span></span>

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

### <span data-ttu-id="67a79-149">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="67a79-149">-ManagementGroupId</span></span>
<span data-ttu-id="67a79-150">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="67a79-150">The management group ID.</span></span>

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

### <span data-ttu-id="67a79-151">-Name</span><span class="sxs-lookup"><span data-stu-id="67a79-151">-Name</span></span>
<span data-ttu-id="67a79-152">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="67a79-152">The name of the deployment it's going to create.</span></span> <span data-ttu-id="67a79-153">Если он не задан, по умолчанию заданное имя файла шаблона при его предоставлении; по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="67a79-153">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="67a79-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="67a79-154">-Pre</span></span>
<span data-ttu-id="67a79-155">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="67a79-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="67a79-156">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="67a79-156">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="67a79-157">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="67a79-157">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="67a79-158">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="67a79-158">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="67a79-159">Для неинтерационных сценариев можно предоставить функцию SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="67a79-159">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="67a79-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="67a79-160">-Tag</span></span>
<span data-ttu-id="67a79-161">Теги для развертывания.</span><span class="sxs-lookup"><span data-stu-id="67a79-161">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="67a79-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="67a79-162">-TemplateFile</span></span>
<span data-ttu-id="67a79-163">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="67a79-163">Local path to the template file.</span></span>

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

### <span data-ttu-id="67a79-164">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="67a79-164">-TemplateObject</span></span>
<span data-ttu-id="67a79-165">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="67a79-165">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="67a79-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="67a79-166">-TemplateParameterFile</span></span>
<span data-ttu-id="67a79-167">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="67a79-167">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="67a79-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="67a79-168">-TemplateParameterObject</span></span>
<span data-ttu-id="67a79-169">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="67a79-169">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="67a79-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="67a79-170">-TemplateParameterUri</span></span>
<span data-ttu-id="67a79-171">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="67a79-171">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="67a79-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="67a79-172">-TemplateUri</span></span>
<span data-ttu-id="67a79-173">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="67a79-173">Uri to the template file.</span></span>

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

### <span data-ttu-id="67a79-174">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="67a79-174">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="67a79-175">Типы изменений ресурсов, разделенные запятой, которые следует исключить из What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="67a79-175">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="67a79-176">Применимо, если за установлен переключатель -WhatIf или -Confirm.</span><span class="sxs-lookup"><span data-stu-id="67a79-176">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="67a79-177">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="67a79-177">-WhatIfResultFormat</span></span>
<span data-ttu-id="67a79-178">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="67a79-178">The What-If result format.</span></span> <span data-ttu-id="67a79-179">Применимо, если за установлен переключатель -WhatIf или -Confirm.</span><span class="sxs-lookup"><span data-stu-id="67a79-179">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="67a79-180">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67a79-180">-Confirm</span></span>
<span data-ttu-id="67a79-181">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="67a79-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a79-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a79-182">-WhatIf</span></span>
<span data-ttu-id="67a79-183">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67a79-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67a79-184">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="67a79-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a79-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a79-185">CommonParameters</span></span>
<span data-ttu-id="67a79-186">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a79-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a79-187">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67a79-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a79-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67a79-188">INPUTS</span></span>

### <span data-ttu-id="67a79-189">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="67a79-189">System.Collections.Hashtable</span></span>

### <span data-ttu-id="67a79-190">System.String</span><span class="sxs-lookup"><span data-stu-id="67a79-190">System.String</span></span>

## <span data-ttu-id="67a79-191">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67a79-191">OUTPUTS</span></span>

### <span data-ttu-id="67a79-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDвслух</span><span class="sxs-lookup"><span data-stu-id="67a79-192">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="67a79-193">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67a79-193">NOTES</span></span>

## <span data-ttu-id="67a79-194">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67a79-194">RELATED LINKS</span></span>
