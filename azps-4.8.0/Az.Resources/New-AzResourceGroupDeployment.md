---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: fd7aa7e892c4874ad0087956156e0ef28ab9f995
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235438"
---
# <span data-ttu-id="2d8b9-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8b9-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="2d8b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2d8b9-103">Добавляет развертывание Azure в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="2d8b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d8b9-104">SYNTAX</span></span>

### <span data-ttu-id="2d8b9-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d8b9-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d8b9-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d8b9-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d8b9-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d8b9-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d8b9-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d8b9-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d8b9-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d8b9-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d8b9-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2d8b9-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d8b9-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="2d8b9-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>]
 [-Tag <Hashtable>] [-WhatIfResultFormat <WhatIfResultFormat>] [-WhatIfExcludeChangeType <String[]>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d8b9-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d8b9-117">DESCRIPTION</span></span>
<span data-ttu-id="2d8b9-118">Командлет **New-AzResourceGroupDeployment** добавляет развертывание в существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="2d8b9-119">Сюда входят ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="2d8b9-120">Ресурс Azure — это управляемый пользователем сущность Azure, например сервер базы данных, базу данных, веб-сайт, виртуальную машину или учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="2d8b9-121">Группа ресурсов Azure — это коллекция ресурсов Azure, которые развертываются как единые, такие как веб-сайт, сервер баз данных и базы данных, необходимые для финансового веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="2d8b9-122">Развертывание группы ресурсов использует шаблон для добавления ресурсов в группу ресурсов и их публикации, чтобы они были доступны в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="2d8b9-123">Чтобы добавить ресурсы в группу ресурсов без использования шаблона, используйте командлет New-AzResource.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="2d8b9-124">Чтобы добавить развертывание группы ресурсов, укажите имя существующей группы ресурсов и шаблона группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="2d8b9-125">Шаблон группы ресурсов — это строка JSON, представляющая группу ресурсов для сложной облачной службы, например веб-портала.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="2d8b9-126">Шаблон включает заполнители параметров для необходимых ресурсов и настраиваемых значений свойств, например имен и размеров.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="2d8b9-127">Вы можете найти большое количество шаблонов в галерее шаблонов Azure или создать собственные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="2d8b9-128">Чтобы создать группу ресурсов с помощью настраиваемого шаблона, укажите параметр *TemplateFile* или *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="2d8b9-128">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="2d8b9-129">Каждый шаблон имеет параметры для настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-129">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="2d8b9-130">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или параметр *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="2d8b9-130">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2d8b9-131">Кроме того, вы можете использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-131">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="2d8b9-132">Чтобы использовать динамические параметры, введите их в командной строке или введите знак "минус" (-), чтобы обозначить параметр, и используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-132">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="2d8b9-133">Значения параметров шаблона, введенные в командной строке, имеют приоритет над значениями в объекте или файле параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-133">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="2d8b9-134">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d8b9-134">EXAMPLES</span></span>

### <span data-ttu-id="2d8b9-135">Пример 1: использование настраиваемого шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="2d8b9-135">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```powershell
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -Tag @{"key1"="value1"; "key2"="value2";}
```

<span data-ttu-id="2d8b9-136">Эта команда создает новое развертывание с помощью настраиваемого шаблона и файла шаблона на диске с параметром "Теги".</span><span class="sxs-lookup"><span data-stu-id="2d8b9-136">This command creates a new deployment by using a custom template and a template file on disk, with defined tags parameter.</span></span>
<span data-ttu-id="2d8b9-137">В команде используется параметр *TemplateFile* , чтобы указать шаблон и параметр *TemplateParameterFile* , чтобы указать файл, содержащий параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-137">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="2d8b9-138">Пример 2: использование настраиваемого объекта шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="2d8b9-138">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="2d8b9-139">Эта команда создает новое развертывание с помощью настраиваемого и файла шаблона на диске, преобразованного в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-139">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="2d8b9-140">Первые две команды считывают текст файла шаблона на диске и преобразуют его в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-140">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="2d8b9-141">Последняя команда использует параметр *TemplateObject* для указания Hashtable и параметра *TemplateParameterFile* для указания файла, содержащего параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-141">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="2d8b9-142">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2d8b9-142">Example 3</span></span>

<span data-ttu-id="2d8b9-143">Добавляет развертывание Azure в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-143">Adds an Azure deployment to a resource group.</span></span> <span data-ttu-id="2d8b9-144">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="2d8b9-144">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzResourceGroupDeployment -DeploymentDebugLogLevel RequestContent -Name mynewstorageaccount -ResourceGroupName 'ContosoEngineering' -TemplateFile 'D:\Azure\Templates\EngineeringSite.json' -TemplateParameterObject <Hashtable>
```

## <span data-ttu-id="2d8b9-145">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d8b9-145">PARAMETERS</span></span>

### <span data-ttu-id="2d8b9-146">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2d8b9-146">-ApiVersion</span></span>
<span data-ttu-id="2d8b9-147">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-147">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2d8b9-148">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-148">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="2d8b9-149">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d8b9-149">-AsJob</span></span>
<span data-ttu-id="2d8b9-150">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2d8b9-150">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d8b9-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d8b9-151">-DefaultProfile</span></span>
<span data-ttu-id="2d8b9-152">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2d8b9-152">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d8b9-153">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="2d8b9-153">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="2d8b9-154">Задает уровень журнала отладки.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-154">Specifies a debug log level.</span></span>
<span data-ttu-id="2d8b9-155">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2d8b9-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d8b9-156">RequestContent</span><span class="sxs-lookup"><span data-stu-id="2d8b9-156">RequestContent</span></span>
- <span data-ttu-id="2d8b9-157">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="2d8b9-157">ResponseContent</span></span>
- <span data-ttu-id="2d8b9-158">Весь</span><span class="sxs-lookup"><span data-stu-id="2d8b9-158">All</span></span>
- <span data-ttu-id="2d8b9-159">Ничего</span><span class="sxs-lookup"><span data-stu-id="2d8b9-159">None</span></span>

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

### <span data-ttu-id="2d8b9-160">-Force</span><span class="sxs-lookup"><span data-stu-id="2d8b9-160">-Force</span></span>
<span data-ttu-id="2d8b9-161">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-161">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d8b9-162">Режим</span><span class="sxs-lookup"><span data-stu-id="2d8b9-162">-Mode</span></span>
<span data-ttu-id="2d8b9-163">Задает режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-163">Specifies the deployment mode.</span></span> <span data-ttu-id="2d8b9-164">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2d8b9-164">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d8b9-165">Завершено: в режиме завершения диспетчер ресурсов удаляет ресурсы, которые существуют в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-165">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="2d8b9-166">Инкремент. в инкрементном режиме диспетчер ресурсов оставляет неизменные ресурсы, которые есть в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-166">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="2d8b9-167">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d8b9-167">-Name</span></span>
<span data-ttu-id="2d8b9-168">Имя развертывания, которое будет создано.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-168">The name of the deployment it's going to create.</span></span> <span data-ttu-id="2d8b9-169">Если не указано, по умолчанию используется имя файла шаблона, когда указан файл шаблона; по умолчанию — текущее время, когда указан объект шаблона, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="2d8b9-169">If not specified, defaults to the template file name when a template file is provided; defaults to the current time when a template object is provided, e.g. "20131223140835".</span></span>

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

### <span data-ttu-id="2d8b9-170">-Pre</span><span class="sxs-lookup"><span data-stu-id="2d8b9-170">-Pre</span></span>
<span data-ttu-id="2d8b9-171">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-171">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2d8b9-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d8b9-172">-ResourceGroupName</span></span>
<span data-ttu-id="2d8b9-173">Указывает имя группы ресурсов для развертывания.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-173">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="2d8b9-174">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="2d8b9-174">-RollBackDeploymentName</span></span>
<span data-ttu-id="2d8b9-175">Откат к успешному развертыванию с указанным именем в группе ресурсов не следует использовать, если используется параметр-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-175">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="2d8b9-176">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8b9-176">-RollbackToLastDeployment</span></span>
<span data-ttu-id="2d8b9-177">Откат к последнему успешному развертыванию в группе ресурсов не отображается, если используется значение-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-177">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="2d8b9-178">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="2d8b9-178">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="2d8b9-179">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-179">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="2d8b9-180">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-180">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="2d8b9-181">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-181">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="2d8b9-182">-Тег</span><span class="sxs-lookup"><span data-stu-id="2d8b9-182">-Tag</span></span>
<span data-ttu-id="2d8b9-183">Теги, помещаемые в развертывание.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-183">The tags to put on the deployment.</span></span>

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

### <span data-ttu-id="2d8b9-184">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="2d8b9-184">-TemplateFile</span></span>
<span data-ttu-id="2d8b9-185">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-185">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="2d8b9-186">Это может быть настраиваемый шаблон или шаблон коллекции, сохраненный в формате JSON, например созданный с помощью командлета **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="2d8b9-186">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="2d8b9-187">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="2d8b9-187">-TemplateObject</span></span>
<span data-ttu-id="2d8b9-188">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-188">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="2d8b9-189">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="2d8b9-189">-TemplateParameterFile</span></span>
<span data-ttu-id="2d8b9-190">Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-190">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="2d8b9-191">Если шаблон имеет параметры, необходимо указать значения параметров с помощью параметра *TemplateParameterFile* или параметра *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="2d8b9-191">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="2d8b9-192">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-192">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="2d8b9-193">Чтобы использовать динамические параметры, введите знак "минус" (-), чтобы обозначить имя параметра, а затем используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-193">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="2d8b9-194">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="2d8b9-194">-TemplateParameterObject</span></span>
<span data-ttu-id="2d8b9-195">Указывает хэш-таблицу имен и значений параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-195">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="2d8b9-196">Чтобы получить справку по хэш-таблицам в Windows PowerShell, введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="2d8b9-196">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="2d8b9-197">Если у шаблона есть параметры, необходимо указать значения параметров.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-197">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="2d8b9-198">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-198">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="2d8b9-199">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="2d8b9-199">-TemplateParameterUri</span></span>
<span data-ttu-id="2d8b9-200">Задает универсальный код ресурса (URI) файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-200">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="2d8b9-201">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="2d8b9-201">-TemplateUri</span></span>
<span data-ttu-id="2d8b9-202">Задает универсальный код ресурса (URI) для файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-202">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="2d8b9-203">Этот файл может быть настраиваемым шаблоном или шаблоном коллекции, сохраненным в формате JSON, например с помощью команды **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-203">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="2d8b9-204">-WhatIfExcludeChangeType</span><span class="sxs-lookup"><span data-stu-id="2d8b9-204">-WhatIfExcludeChangeType</span></span>
<span data-ttu-id="2d8b9-205">Типы изменения ресурсов, разделенные запятыми, которые будут исключены из результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-205">Comma-separated resource change types to be excluded from What-If results.</span></span> <span data-ttu-id="2d8b9-206">Применимо, если установлен параметр-WhatIf или-Confirm.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-206">Applicable when the -WhatIf or -Confirm switch is set.</span></span>

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

### <span data-ttu-id="2d8b9-207">-WhatIfResultFormat</span><span class="sxs-lookup"><span data-stu-id="2d8b9-207">-WhatIfResultFormat</span></span>
<span data-ttu-id="2d8b9-208">Формат результатов What-If.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-208">The What-If result format.</span></span>

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

### <span data-ttu-id="2d8b9-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d8b9-209">-Confirm</span></span>
<span data-ttu-id="2d8b9-210">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d8b9-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d8b9-211">-WhatIf</span></span>
<span data-ttu-id="2d8b9-212">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d8b9-213">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d8b9-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d8b9-214">CommonParameters</span></span>
<span data-ttu-id="2d8b9-215">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d8b9-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d8b9-216">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d8b9-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d8b9-217">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d8b9-217">INPUTS</span></span>

### <span data-ttu-id="2d8b9-218">System. String</span><span class="sxs-lookup"><span data-stu-id="2d8b9-218">System.String</span></span>

### <span data-ttu-id="2d8b9-219">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="2d8b9-219">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="2d8b9-220">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d8b9-220">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d8b9-221">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d8b9-221">OUTPUTS</span></span>

### <span data-ttu-id="2d8b9-222">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8b9-222">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="2d8b9-223">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d8b9-223">NOTES</span></span>

## <span data-ttu-id="2d8b9-224">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d8b9-224">RELATED LINKS</span></span>

[<span data-ttu-id="2d8b9-225">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8b9-225">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="2d8b9-226">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="2d8b9-226">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="2d8b9-227">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2d8b9-227">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="2d8b9-228">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8b9-228">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="2d8b9-229">Остановить-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8b9-229">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="2d8b9-230">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d8b9-230">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)