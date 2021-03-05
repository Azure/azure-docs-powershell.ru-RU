---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 3403900fafae1615f8253b4d5671e497a1d507f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978152"
---
# <span data-ttu-id="e3453-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e3453-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="e3453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3453-102">SYNOPSIS</span></span>
<span data-ttu-id="e3453-103">Добавляет развертывание Azure в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3453-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="e3453-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e3453-104">SYNTAX</span></span>

### <span data-ttu-id="e3453-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3453-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3453-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3453-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3453-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3453-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-109">ByTemplateSpecResourceIdAndParamsObject</span><span class="sxs-lookup"><span data-stu-id="e3453-109">ByTemplateSpecResourceIdAndParamsObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterObject <Hashtable> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-110">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3453-110">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-111">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3453-111">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-112">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3453-112">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-113">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="e3453-113">ByTemplateSpecResourceIdAndParams</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterFile <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-114">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e3453-114">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-115">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e3453-115">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-116">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e3453-116">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-117">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="e3453-117">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateParameterUri <String> -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3453-118">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e3453-118">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3453-119">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e3453-119">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3453-120">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="e3453-120">ByTemplateSpecResourceId</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] [-QueryString <String>] -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3453-121">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3453-121">DESCRIPTION</span></span>
<span data-ttu-id="e3453-122">**Новый-AzResourceGroupDeployment** добавляет развертывание в существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3453-122">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="e3453-123">К ним относятся ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="e3453-123">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="e3453-124">Ресурс Azure — это объект Azure, управляемый пользователем, например сервер базы данных, база данных, веб-сайт, виртуальная машинка или учетная запись хранения.</span><span class="sxs-lookup"><span data-stu-id="e3453-124">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="e3453-125">Группа ресурсов Azure — это набор ресурсов Azure, развертываемых в качестве единицы, таких как веб-сайт, сервер баз данных и базы данных, необходимые для финансового веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="e3453-125">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="e3453-126">Развертывание группы ресурсов с помощью шаблона используется для добавления ресурсов в группу ресурсов и их публикации, чтобы они были доступны в Azure.</span><span class="sxs-lookup"><span data-stu-id="e3453-126">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="e3453-127">Чтобы добавить ресурсы в группу ресурсов, не используя шаблон, воспользуйтесь New-AzResource-New-AzResource ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3453-127">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="e3453-128">Чтобы добавить развертывание группы ресурсов, укажите имя существующей группы ресурсов и шаблон группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3453-128">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="e3453-129">Шаблон группы ресурсов — это строка JSON, представляюная группу ресурсов для сложной облачной службы, например веб-портала.</span><span class="sxs-lookup"><span data-stu-id="e3453-129">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="e3453-130">Шаблон содержит заметели параметров для необходимых ресурсов и настраиваемых значений свойств, таких как имена и размеры.</span><span class="sxs-lookup"><span data-stu-id="e3453-130">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="e3453-131">В коллекции шаблонов Azure можно найти множество шаблонов или создать собственные.</span><span class="sxs-lookup"><span data-stu-id="e3453-131">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="e3453-132">Чтобы использовать настраиваемый шаблон для создания группы ресурсов, укажите параметр *TemplateFile* или *TemplateUri.*</span><span class="sxs-lookup"><span data-stu-id="e3453-132">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="e3453-133">У каждого шаблона есть параметры настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="e3453-133">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="e3453-134">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="e3453-134">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="e3453-135">Кроме того, можно использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3453-135">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="e3453-136">Чтобы использовать динамические параметры, введите их в командной области или знак "минус" (-), чтобы указать параметр, и используйте клавишу TAB для циклиального перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="e3453-136">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="e3453-137">Значения параметров шаблона, которые вы вводите в командной области, имеют приоритет над значениями в объекте или файле с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3453-137">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="e3453-138">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e3453-138">EXAMPLES</span></span>

### <span data-ttu-id="e3453-139">Пример 1. Создание развертывания с помощью настраиваемой файла шаблона и параметра</span><span class="sxs-lookup"><span data-stu-id="e3453-139">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="e3453-140">Эта команда создает развертывание с использованием настраиваемого шаблона и файла шаблона на диске с определенным параметром тегов.</span><span class="sxs-lookup"><span data-stu-id="e3453-140">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="e3453-141">Команда использует параметр *TemplateFile* для указания шаблона, а параметр *TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="e3453-141">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="e3453-142">Пример 2. Создание развертывания с помощью настраиваемых объектов шаблонов и файлов параметров</span><span class="sxs-lookup"><span data-stu-id="e3453-142">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="e3453-143">Эта команда создает развертывание с использованием настраиваемого файла шаблона и файла шаблона на диске, преобразованного в формат в памяти.</span><span class="sxs-lookup"><span data-stu-id="e3453-143">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="e3453-144">Первые две команды читают текст файла шаблона на диске и преобразуют его в размер памяти.</span><span class="sxs-lookup"><span data-stu-id="e3453-144">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="e3453-145">Последняя команда использует параметр *TemplateObject* для указания параметров hashtable и *TemplateParameterFile* для указания файла, который содержит параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="e3453-145">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="e3453-146">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e3453-146">Example 3</span></span>

<span data-ttu-id="e3453-147">Добавляет развертывание Azure в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3453-147">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="e3453-148">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="e3453-148">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

### <span data-ttu-id="e3453-149">Пример 4. Развертывание шаблона, храняного в неугодной учетной записи хранения, с помощью маркера URI и SAS</span><span class="sxs-lookup"><span data-stu-id="e3453-149">Example 4: Deploy a template stored in a non public storage account using a uri and SAS token</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "RGName" -TemplateUri "https://example.com/example.json" -QueryString "foo"
```

<span data-ttu-id="e3453-150">Эта команда создает развертывание с использованием шаблона TemplateUri, который не является общедоступным и требует на доступ параметра token, который будет предоставляться с помощью параметра QueryString.</span><span class="sxs-lookup"><span data-stu-id="e3453-150">This command creates a new deployment using the template in TemplateUri which is not public and requires a token parameter to access which would be provided using the QueryString parameter.</span></span>
<span data-ttu-id="e3453-151">Эта команда будет эффективно работать с шаблоном по https://example.com/example.json?foo URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="e3453-151">Running this command effectively accesses the template using the url https://example.com/example.json?foo.</span></span>
<span data-ttu-id="e3453-152">Это может быть использовано, если вы хотите использовать шаблон в учетной записи хранения, предоставляя токен SAS в качестве QueryString.</span><span class="sxs-lookup"><span data-stu-id="e3453-152">This can be used if you want to use a template in a storage account by providing the SAS token as the QueryString</span></span>

## <span data-ttu-id="e3453-153">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3453-153">PARAMETERS</span></span>

### <span data-ttu-id="e3453-154">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3453-154">-AsJob</span></span>
<span data-ttu-id="e3453-155">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e3453-155">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3453-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3453-156">-DefaultProfile</span></span>
<span data-ttu-id="e3453-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e3453-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3453-158">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="e3453-158">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="e3453-159">Определяет уровень журнала отбивки.</span><span class="sxs-lookup"><span data-stu-id="e3453-159">Specifies a debug log level.</span></span>
<span data-ttu-id="e3453-160">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="e3453-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e3453-161">RequestContent</span><span class="sxs-lookup"><span data-stu-id="e3453-161">RequestContent</span></span>
- <span data-ttu-id="e3453-162">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="e3453-162">ResponseContent</span></span>
- <span data-ttu-id="e3453-163">Все</span><span class="sxs-lookup"><span data-stu-id="e3453-163">All</span></span>
- <span data-ttu-id="e3453-164">Нет</span><span class="sxs-lookup"><span data-stu-id="e3453-164">None</span></span>

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

### <span data-ttu-id="e3453-165">-Force</span><span class="sxs-lookup"><span data-stu-id="e3453-165">-Force</span></span>
<span data-ttu-id="e3453-166">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e3453-166">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3453-167">-Mode</span><span class="sxs-lookup"><span data-stu-id="e3453-167">-Mode</span></span>
<span data-ttu-id="e3453-168">Режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="e3453-168">Specifies the deployment mode.</span></span> <span data-ttu-id="e3453-169">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="e3453-169">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e3453-170">Завершено. В полном режиме диспетчер ресурсов удаляет ресурсы, которые существуют в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="e3453-170">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="e3453-171">Добавоч. Приращение в режиме приращения диспетчер ресурсов не изменяет ресурсы, которые существуют в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="e3453-171">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="e3453-172">-Name</span><span class="sxs-lookup"><span data-stu-id="e3453-172">-Name</span></span>
<span data-ttu-id="e3453-173">Имя развертывания, которое будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="e3453-173">The name of the deployment it's going to create.</span></span> <span data-ttu-id="e3453-174">Если он не задан, по умолчанию заданное имя файла шаблона при его предоставлении; по умолчанию на текущее время, когда предоставлен объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="e3453-174">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="e3453-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="e3453-175">-Pre</span></span>
<span data-ttu-id="e3453-176">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="e3453-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e3453-177">-QueryString</span><span class="sxs-lookup"><span data-stu-id="e3453-177">-QueryString</span></span>
<span data-ttu-id="e3453-178">Строка запроса (например, токен SAS), которая будет использоваться с параметром TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="e3453-178">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="e3453-179">Будет использоваться в случае связанных шаблонов</span><span class="sxs-lookup"><span data-stu-id="e3453-179">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="e3453-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3453-180">-ResourceGroupName</span></span>
<span data-ttu-id="e3453-181">Имя группы ресурсов, которая будет развернута.</span><span class="sxs-lookup"><span data-stu-id="e3453-181">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="e3453-182">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="e3453-182">-RollBackDeploymentName</span></span>
<span data-ttu-id="e3453-183">Откат до успешного развертывания с заданным именем в группе ресурсов не следует использовать, если используется -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="e3453-183">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="e3453-184">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="e3453-184">-RollbackToLastDeployment</span></span>
<span data-ttu-id="e3453-185">При этом не должно быть отката до последнего успешного развертывания в группе ресурсов, если используется имя -RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="e3453-185">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="e3453-186">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e3453-186">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e3453-187">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="e3453-187">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="e3453-188">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="e3453-188">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="e3453-189">Для неинтерационных сценариев можно использовать параметр SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="e3453-189">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e3453-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3453-190">-Tag</span></span>
<span data-ttu-id="e3453-191">Теги для развертывания.</span><span class="sxs-lookup"><span data-stu-id="e3453-191">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="e3453-192">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e3453-192">-TemplateFile</span></span>
<span data-ttu-id="e3453-193">Указывает полный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3453-193">Specifies the full path of a template file.</span></span> <span data-ttu-id="e3453-194">Поддерживаемый тип файла шаблона: json и bicep.</span><span class="sxs-lookup"><span data-stu-id="e3453-194">Supported template file type: json and bicep.</span></span>
<span data-ttu-id="e3453-195">Это может быть настраиваемый шаблон или шаблон коллекции, сохраненный в файле JSON, например с помощью cmdlet **Save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="e3453-195">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="e3453-196">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="e3453-196">-TemplateObject</span></span>
<span data-ttu-id="e3453-197">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="e3453-197">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="e3453-198">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3453-198">-TemplateParameterFile</span></span>
<span data-ttu-id="e3453-199">Указывает полный путь к JSON-файлу, который содержит имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3453-199">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="e3453-200">Если у шаблона есть параметры, необходимо указать их значения с помощью параметра *TemplateParameterFile* или *TemplateParameterObject.*</span><span class="sxs-lookup"><span data-stu-id="e3453-200">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="e3453-201">Параметры шаблона динамически добавляются в команду при его указании.</span><span class="sxs-lookup"><span data-stu-id="e3453-201">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="e3453-202">Чтобы использовать динамические параметры, введите знак "минус" (-), чтобы указать имя параметра, а затем используйте клавишу TAB для циклиального перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="e3453-202">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="e3453-203">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3453-203">-TemplateParameterObject</span></span>
<span data-ttu-id="e3453-204">Указывает таблицу с именами и значениями параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3453-204">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="e3453-205">Для справки по hash таблицам в Windows PowerShell введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="e3453-205">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="e3453-206">Если у шаблона есть параметры, необходимо указать их значения.</span><span class="sxs-lookup"><span data-stu-id="e3453-206">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="e3453-207">Параметры шаблона динамически добавляются в команду при его указании.</span><span class="sxs-lookup"><span data-stu-id="e3453-207">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="e3453-208">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e3453-208">-TemplateParameterUri</span></span>
<span data-ttu-id="e3453-209">Определяет URI файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3453-209">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="e3453-210">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="e3453-210">-TemplateSpecId</span></span>
<span data-ttu-id="e3453-211">ИД ресурса шаблонаSpec, который нужно развернуть.</span><span class="sxs-lookup"><span data-stu-id="e3453-211">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="e3453-212">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e3453-212">-TemplateUri</span></span>
<span data-ttu-id="e3453-213">Определяет URI файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3453-213">Specifies the URI of a template file.</span></span>
<span data-ttu-id="e3453-214">Этот файл может быть настраиваемый шаблон или шаблон коллекции, сохраненный как файл JSON, например с помощью **save-AzResourceGroupGalleryTemplate.**</span><span class="sxs-lookup"><span data-stu-id="e3453-214">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="e3453-215">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="e3453-215">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="e3453-216">Типы изменений ресурсов, разделенные запятой, которые следует исключить из What-If результатов.</span><span class="sxs-lookup"><span data-stu-id="e3453-216">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="e3453-217">Применимо, если за установлен переключатель -WhatIf или -Confirm.</span><span class="sxs-lookup"><span data-stu-id="e3453-217">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="e3453-218">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="e3453-218">-WhatIfResultFormat</span></span>
<span data-ttu-id="e3453-219">Результат What-If формате.</span><span class="sxs-lookup"><span data-stu-id="e3453-219">The What-If result format.</span></span>

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

### <span data-ttu-id="e3453-220">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3453-220">-Confirm</span></span>
<span data-ttu-id="e3453-221">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3453-221">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3453-222">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3453-222">-WhatIf</span></span>
<span data-ttu-id="e3453-223">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3453-223">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3453-224">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e3453-224">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3453-225">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3453-225">CommonParameters</span></span>
<span data-ttu-id="e3453-226">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3453-226">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3453-227">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3453-227">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3453-228">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3453-228">INPUTS</span></span>

### <span data-ttu-id="e3453-229">System.String</span><span class="sxs-lookup"><span data-stu-id="e3453-229">System.String</span></span>

### <span data-ttu-id="e3453-230">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="e3453-230">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="e3453-231">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3453-231">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e3453-232">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3453-232">OUTPUTS</span></span>

### <span data-ttu-id="e3453-233">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e3453-233">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="e3453-234">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e3453-234">NOTES</span></span>

## <span data-ttu-id="e3453-235">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3453-235">RELATED LINKS</span></span>

[<span data-ttu-id="e3453-236">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e3453-236">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="e3453-237">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="e3453-237">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="e3453-238">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e3453-238">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="e3453-239">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e3453-239">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="e3453-240">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e3453-240">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="e3453-241">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e3453-241">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)