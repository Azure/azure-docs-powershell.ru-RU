---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTenantDeployment.md
ms.openlocfilehash: 38f46b8805b8e259b086e5c5a78e929112dca83a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912163"
---
# <span data-ttu-id="b8b55-101">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="b8b55-101">New-AzTenantDeployment</span></span>

## <span data-ttu-id="b8b55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8b55-102">SYNOPSIS</span></span>
<span data-ttu-id="b8b55-103">Создание развертывания в области клиента</span><span class="sxs-lookup"><span data-stu-id="b8b55-103">Create a deployment at tenant scope</span></span>

## <span data-ttu-id="b8b55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8b55-104">SYNTAX</span></span>

### <span data-ttu-id="b8b55-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8b55-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b55-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b8b55-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8b55-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b8b55-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8b55-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="b8b55-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8b55-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b8b55-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8b55-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b8b55-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b55-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="b8b55-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b55-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b8b55-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8b55-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b8b55-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b55-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="b8b55-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b55-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b8b55-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8b55-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="b8b55-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzTenantDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8b55-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8b55-117">DESCRIPTION</span></span>
<span data-ttu-id="b8b55-118">Командлет **New-AzTenantDeployment** добавляет развертывание в текущую область клиента.</span><span class="sxs-lookup"><span data-stu-id="b8b55-118">The **New-AzTenantDeployment** cmdlet adds a deployment at the current tenant scope.</span></span>

<span data-ttu-id="b8b55-119">Чтобы добавить развертывание в область клиента, укажите расположение и шаблон.</span><span class="sxs-lookup"><span data-stu-id="b8b55-119">To add a deployment at tenant scope, specify the location and a template.</span></span>
<span data-ttu-id="b8b55-120">Расположение указывает диспетчеру ресурсов Azure, где хранятся данные развертывания.</span><span class="sxs-lookup"><span data-stu-id="b8b55-120">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="b8b55-121">Шаблон — это строка JSON, содержащая отдельные ресурсы для развертывания.</span><span class="sxs-lookup"><span data-stu-id="b8b55-121">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="b8b55-122">Шаблон включает заполнители параметров для необходимых ресурсов и настраиваемых значений свойств, например имен и размеров.</span><span class="sxs-lookup"><span data-stu-id="b8b55-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="b8b55-123">Чтобы использовать настраиваемый шаблон для развертывания, укажите параметр *TemplateFile* или *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="b8b55-123">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="b8b55-124">Каждый шаблон имеет параметры для настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="b8b55-124">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="b8b55-125">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или параметр *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="b8b55-125">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="b8b55-126">Кроме того, вы можете использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="b8b55-126">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="b8b55-127">Чтобы использовать динамические параметры, введите их в командной строке или введите знак "минус" (-), чтобы обозначить параметр, и используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="b8b55-127">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="b8b55-128">Значения параметров шаблона, введенные в командной строке, имеют приоритет над значениями в объекте или файле параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="b8b55-128">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

<span data-ttu-id="b8b55-129">Чтобы добавить ресурсы в группу ресурсов, используйте **New-AzResourceGroupDeployment** , который создает развертывание в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8b55-129">To add resources to a resource group, use the **New-AzResourceGroupDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="b8b55-130">Чтобы добавить ресурсы в подписку, используйте **New-AzSubscriptionDeployment** , который создает развертывание в области подписки, которое развертывает ресурсы уровня подписки.</span><span class="sxs-lookup"><span data-stu-id="b8b55-130">To add resources to a subscription, use the **New-AzSubscriptionDeployment** which creates a deployment at subscription scope, which deploys subscription level resources.</span></span>
<span data-ttu-id="b8b55-131">Чтобы добавить ресурсы в группу управления, используйте **New-AzManagementGroupDeployment** , который создает развертывание в группе управления.</span><span class="sxs-lookup"><span data-stu-id="b8b55-131">To add resources at a management group, use the **New-AzManagementGroupDeployment** which creates a deployment at a management group.</span></span>

## <span data-ttu-id="b8b55-132">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8b55-132">EXAMPLES</span></span>

### <span data-ttu-id="b8b55-133">Пример 1: использование настраиваемого шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="b8b55-133">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="b8b55-134">Эта команда создает новое развертывание в текущей области клиента с помощью настраиваемого шаблона и файла шаблона на диске.</span><span class="sxs-lookup"><span data-stu-id="b8b55-134">This command creates a new deployment at the current tenant scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="b8b55-135">В команде используется параметр *TemplateFile* , чтобы указать шаблон и параметр *TemplateParameterFile* , чтобы указать файл, содержащий параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="b8b55-135">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="b8b55-136">Пример 2: использование настраиваемого объекта шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="b8b55-136">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\OrgParams.json"
```

<span data-ttu-id="b8b55-137">Эта команда создает новое развертывание в текущем клиенте с помощью настраиваемого шаблона и файла шаблона на диске, преобразованного в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="b8b55-137">This command creates a new deployment at the current tenant by using a custom template and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="b8b55-138">Первые две команды считывают текст файла шаблона на диске и преобразуют его в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="b8b55-138">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="b8b55-139">Последняя команда использует параметр *TemplateObject* , чтобы указать эту хэш-таблицу, а параметр *TemplateParameterFile* — для указания файла, содержащего параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="b8b55-139">The last command uses the *TemplateObject* parameter to specify this hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="b8b55-140">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8b55-140">PARAMETERS</span></span>

### <span data-ttu-id="b8b55-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b8b55-141">-ApiVersion</span></span>
<span data-ttu-id="b8b55-142">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8b55-142">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b8b55-143">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="b8b55-143">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8b55-144">-AsJob</span></span>
<span data-ttu-id="b8b55-145">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b8b55-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8b55-146">-DefaultProfile</span></span>
<span data-ttu-id="b8b55-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8b55-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-148">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="b8b55-148">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="b8b55-149">Уровень журнала отладки развертывания.</span><span class="sxs-lookup"><span data-stu-id="b8b55-149">The deployment debug log level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-150">-Location</span><span class="sxs-lookup"><span data-stu-id="b8b55-150">-Location</span></span>
<span data-ttu-id="b8b55-151">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="b8b55-151">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-152">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8b55-152">-Name</span></span>
<span data-ttu-id="b8b55-153">Имя развертывания, которое будет создано.</span><span class="sxs-lookup"><span data-stu-id="b8b55-153">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="b8b55-154">Действительно только при использовании шаблона.</span><span class="sxs-lookup"><span data-stu-id="b8b55-154">Only valid when a template is used.</span></span>
<span data-ttu-id="b8b55-155">При использовании шаблона, если пользователь не указывает имя развертывания, используйте текущее время, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="b8b55-155">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="b8b55-156">-Pre</span></span>
<span data-ttu-id="b8b55-157">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="b8b55-157">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-158">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="b8b55-158">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="b8b55-159">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="b8b55-159">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="b8b55-160">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="b8b55-160">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="b8b55-161">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="b8b55-161">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-162">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b8b55-162">-TemplateFile</span></span>
<span data-ttu-id="b8b55-163">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="b8b55-163">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-164">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="b8b55-164">-TemplateObject</span></span>
<span data-ttu-id="b8b55-165">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="b8b55-165">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-166">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b8b55-166">-TemplateParameterFile</span></span>
<span data-ttu-id="b8b55-167">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="b8b55-167">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="b8b55-168">-TemplateParameterObject</span></span>
<span data-ttu-id="b8b55-169">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="b8b55-169">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-170">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="b8b55-170">-TemplateParameterUri</span></span>
<span data-ttu-id="b8b55-171">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="b8b55-171">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-172">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="b8b55-172">-TemplateUri</span></span>
<span data-ttu-id="b8b55-173">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="b8b55-173">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8b55-174">-Confirm</span></span>
<span data-ttu-id="b8b55-175">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8b55-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8b55-176">-WhatIf</span></span>
<span data-ttu-id="b8b55-177">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8b55-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8b55-178">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8b55-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8b55-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8b55-179">CommonParameters</span></span>
<span data-ttu-id="b8b55-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8b55-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8b55-181">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8b55-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8b55-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8b55-182">INPUTS</span></span>

### <span data-ttu-id="b8b55-183">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b8b55-183">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b8b55-184">System. String</span><span class="sxs-lookup"><span data-stu-id="b8b55-184">System.String</span></span>

## <span data-ttu-id="b8b55-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8b55-185">OUTPUTS</span></span>

### <span data-ttu-id="b8b55-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b8b55-186">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b8b55-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8b55-187">NOTES</span></span>

## <span data-ttu-id="b8b55-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8b55-188">RELATED LINKS</span></span>
