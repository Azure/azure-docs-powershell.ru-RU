---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 916e2fea0e88a1409bc2586ab8b2e80b11ec1a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247040"
---
# <span data-ttu-id="9d311-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9d311-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="9d311-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d311-102">SYNOPSIS</span></span>
<span data-ttu-id="9d311-103">Добавляет развертывание Azure в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d311-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="9d311-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d311-104">SYNTAX</span></span>

### <span data-ttu-id="9d311-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d311-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9d311-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9d311-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9d311-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9d311-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9d311-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9d311-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9d311-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9d311-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9d311-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9d311-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d311-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9d311-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d311-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d311-117">DESCRIPTION</span></span>
<span data-ttu-id="9d311-118">Командлет **New-AzResourceGroupDeployment** добавляет развертывание в существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d311-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="9d311-119">Сюда входят ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="9d311-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="9d311-120">Ресурс Azure — это управляемый пользователем сущность Azure, например сервер базы данных, базу данных, веб-сайт, виртуальную машину или учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="9d311-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="9d311-121">Группа ресурсов Azure — это коллекция ресурсов Azure, которые развертываются как единые, такие как веб-сайт, сервер баз данных и базы данных, необходимые для финансового веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="9d311-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="9d311-122">Развертывание группы ресурсов использует шаблон для добавления ресурсов в группу ресурсов и их публикации, чтобы они были доступны в Azure.</span><span class="sxs-lookup"><span data-stu-id="9d311-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="9d311-123">Чтобы добавить ресурсы в группу ресурсов без использования шаблона, используйте командлет New-AzResource.</span><span class="sxs-lookup"><span data-stu-id="9d311-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="9d311-124">Чтобы добавить развертывание группы ресурсов, укажите имя существующей группы ресурсов и шаблона группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d311-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="9d311-125">Шаблон группы ресурсов — это строка JSON, представляющая группу ресурсов для сложной облачной службы, например веб-портала.</span><span class="sxs-lookup"><span data-stu-id="9d311-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="9d311-126">Шаблон включает заполнители параметров для необходимых ресурсов и настраиваемых значений свойств, например имен и размеров.</span><span class="sxs-lookup"><span data-stu-id="9d311-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="9d311-127">Вы можете найти большое количество шаблонов в галерее шаблонов Azure или создать собственные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="9d311-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="9d311-128">Чтобы создать группу ресурсов с помощью настраиваемого шаблона, укажите параметр *TemplateFile* или *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="9d311-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="9d311-129">Каждый шаблон имеет параметры для настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="9d311-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="9d311-130">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или параметр *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="9d311-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="9d311-131">Кроме того, вы можете использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="9d311-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="9d311-132">Чтобы использовать динамические параметры, введите их в командной строке или введите знак "минус" (-), чтобы обозначить параметр, и используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="9d311-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="9d311-133">Значения параметров шаблона, введенные в командной строке, имеют приоритет над значениями в объекте или файле параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="9d311-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="9d311-134">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d311-134">EXAMPLES</span></span>

### <span data-ttu-id="9d311-135">Пример 1: использование настраиваемого шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="9d311-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="9d311-136">Эта команда создает новое развертывание с помощью настраиваемого шаблона и файла шаблона на диске с параметром "Теги".</span><span class="sxs-lookup"><span data-stu-id="9d311-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="9d311-137">В команде используется параметр *TemplateFile* , чтобы указать шаблон и параметр *TemplateParameterFile* , чтобы указать файл, содержащий параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="9d311-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="9d311-138">Пример 2: использование настраиваемого объекта шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="9d311-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="9d311-139">Эта команда создает новое развертывание с помощью настраиваемого и файла шаблона на диске, преобразованного в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="9d311-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="9d311-140">Первые две команды считывают текст файла шаблона на диске и преобразуют его в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="9d311-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="9d311-141">Последняя команда использует параметр *TemplateObject* для указания Hashtable и параметра *TemplateParameterFile* для указания файла, содержащего параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="9d311-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="9d311-142">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9d311-142">Example 3</span></span>

<span data-ttu-id="9d311-143">Добавляет развертывание Azure в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d311-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="9d311-144">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="9d311-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="9d311-145">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d311-145">PARAMETERS</span></span>

### <span data-ttu-id="9d311-146">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d311-146">-AsJob</span></span>
<span data-ttu-id="9d311-147">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9d311-147">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d311-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d311-148">-DefaultProfile</span></span>
<span data-ttu-id="9d311-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9d311-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d311-150">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="9d311-150">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="9d311-151">Задает уровень журнала отладки.</span><span class="sxs-lookup"><span data-stu-id="9d311-151">Specifies a debug log level.</span></span>
<span data-ttu-id="9d311-152">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9d311-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d311-153">RequestContent</span><span class="sxs-lookup"><span data-stu-id="9d311-153">RequestContent</span></span>
- <span data-ttu-id="9d311-154">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="9d311-154">ResponseContent</span></span>
- <span data-ttu-id="9d311-155">Весь</span><span class="sxs-lookup"><span data-stu-id="9d311-155">All</span></span>
- <span data-ttu-id="9d311-156">Ничего</span><span class="sxs-lookup"><span data-stu-id="9d311-156">None</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RequestContent, ResponseContent, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d311-157">-Force</span><span class="sxs-lookup"><span data-stu-id="9d311-157">-Force</span></span>
<span data-ttu-id="9d311-158">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9d311-158">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9d311-159">Режим</span><span class="sxs-lookup"><span data-stu-id="9d311-159">-Mode</span></span>
<span data-ttu-id="9d311-160">Задает режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="9d311-160">Specifies the deployment mode.</span></span> <span data-ttu-id="9d311-161">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9d311-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d311-162">Завершено: в режиме завершения диспетчер ресурсов удаляет ресурсы, которые существуют в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="9d311-162">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="9d311-163">Инкремент. в инкрементном режиме диспетчер ресурсов оставляет неизменные ресурсы, которые есть в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="9d311-163">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d311-164">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d311-164">-Name</span></span>
<span data-ttu-id="9d311-165">Имя развертывания, которое будет создано.</span><span class="sxs-lookup"><span data-stu-id="9d311-165">The name of the deployment it's going to create.</span></span> <span data-ttu-id="9d311-166">Если не указано, по умолчанию используется имя файла шаблона, когда указан файл шаблона; по умолчанию — текущее время, когда указан объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="9d311-166">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="9d311-167">-Pre</span><span class="sxs-lookup"><span data-stu-id="9d311-167">-Pre</span></span>
<span data-ttu-id="9d311-168">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="9d311-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9d311-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d311-169">-ResourceGroupName</span></span>
<span data-ttu-id="9d311-170">Указывает имя группы ресурсов для развертывания.</span><span class="sxs-lookup"><span data-stu-id="9d311-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="9d311-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="9d311-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="9d311-172">Откат к успешному развертыванию с указанным именем в группе ресурсов не следует использовать, если используется параметр-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="9d311-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d311-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="9d311-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="9d311-174">Откат к последнему успешному развертыванию в группе ресурсов не отображается, если используется значение-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="9d311-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="9d311-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="9d311-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="9d311-176">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="9d311-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="9d311-177">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="9d311-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="9d311-178">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="9d311-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="9d311-179">-Тег</span><span class="sxs-lookup"><span data-stu-id="9d311-179">-Tag</span></span>
<span data-ttu-id="9d311-180">Теги, помещаемые в развертывание.</span><span class="sxs-lookup"><span data-stu-id="9d311-180">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="9d311-181">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9d311-181">-TemplateFile</span></span>
<span data-ttu-id="9d311-182">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="9d311-182">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="9d311-183">Это может быть настраиваемый шаблон или шаблон коллекции, сохраненный в формате JSON, например созданный с помощью командлета **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="9d311-183">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="9d311-184">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="9d311-184">-TemplateObject</span></span>
<span data-ttu-id="9d311-185">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="9d311-185">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="9d311-186">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9d311-186">-TemplateParameterFile</span></span>
<span data-ttu-id="9d311-187">Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="9d311-187">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="9d311-188">Если шаблон имеет параметры, необходимо указать значения параметров с помощью параметра *TemplateParameterFile* или параметра *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="9d311-188">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="9d311-189">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="9d311-189">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="9d311-190">Чтобы использовать динамические параметры, введите знак "минус" (-), чтобы обозначить имя параметра, а затем используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="9d311-190">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="9d311-191">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="9d311-191">-TemplateParameterObject</span></span>
<span data-ttu-id="9d311-192">Указывает хэш-таблицу имен и значений параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="9d311-192">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="9d311-193">Чтобы получить справку по хэш-таблицам в Windows PowerShell, введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="9d311-193">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="9d311-194">Если у шаблона есть параметры, необходимо указать значения параметров.</span><span class="sxs-lookup"><span data-stu-id="9d311-194">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="9d311-195">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="9d311-195">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="9d311-196">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="9d311-196">-TemplateParameterUri</span></span>
<span data-ttu-id="9d311-197">Задает универсальный код ресурса (URI) файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="9d311-197">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="9d311-198">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="9d311-198">-TemplateUri</span></span>
<span data-ttu-id="9d311-199">Задает универсальный код ресурса (URI) для файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="9d311-199">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="9d311-200">Этот файл может быть настраиваемым шаблоном или шаблоном коллекции, сохраненным в формате JSON, например с помощью команды **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="9d311-200">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="9d311-201">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="9d311-201">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="9d311-202">Типы изменения ресурсов, разделенные запятыми, которые будут исключены из результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="9d311-202">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="9d311-203">Применимо, если установлен параметр-WhatIf или-Confirm.</span><span class="sxs-lookup"><span data-stu-id="9d311-203">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="9d311-204">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="9d311-204">-WhatIfResultFormat</span></span>
<span data-ttu-id="9d311-205">Формат результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="9d311-205">The What-If result format.</span></span>

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

### <span data-ttu-id="9d311-206">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d311-206">-Confirm</span></span>
<span data-ttu-id="9d311-207">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9d311-207">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d311-208">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d311-208">-WhatIf</span></span>
<span data-ttu-id="9d311-209">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9d311-209">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d311-210">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9d311-210">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d311-211">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d311-211">CommonParameters</span></span>
<span data-ttu-id="9d311-212">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d311-212">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d311-213">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d311-213">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d311-214">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d311-214">INPUTS</span></span>

### <span data-ttu-id="9d311-215">System. String</span><span class="sxs-lookup"><span data-stu-id="9d311-215">System.String</span></span>

### <span data-ttu-id="9d311-216">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="9d311-216">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="9d311-217">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9d311-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9d311-218">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d311-218">OUTPUTS</span></span>

### <span data-ttu-id="9d311-219">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9d311-219">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="9d311-220">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d311-220">NOTES</span></span>

## <span data-ttu-id="9d311-221">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d311-221">RELATED LINKS</span></span>

[<span data-ttu-id="9d311-222">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9d311-222">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="9d311-223">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="9d311-223">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="9d311-224">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9d311-224">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="9d311-225">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9d311-225">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="9d311-226">Остановить-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9d311-226">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="9d311-227">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9d311-227">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)