---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroupDeployment.md
ms.openlocfilehash: 067faa4688f079d24f2fc79a4771c84f6c02d0c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729376"
---
# <span data-ttu-id="88670-101">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88670-101">New-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="88670-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88670-102">SYNOPSIS</span></span>
<span data-ttu-id="88670-103">Добавляет развертывание Azure в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88670-103">Adds an Azure deployment to a resource group.</span></span>

## <span data-ttu-id="88670-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88670-104">SYNTAX</span></span>

### <span data-ttu-id="88670-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88670-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88670-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="88670-106">ByTemplateObjectAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88670-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="88670-107">ByTemplateFileAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88670-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="88670-108">ByTemplateUriAndParameterObject</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88670-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="88670-109">ByTemplateObjectAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88670-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="88670-110">ByTemplateFileAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88670-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="88670-111">ByTemplateUriAndParameterFile</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88670-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="88670-112">ByTemplateObjectAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88670-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="88670-113">ByTemplateFileAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88670-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="88670-114">ByTemplateUriAndParameterUri</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88670-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="88670-115">ByTemplateObjectWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88670-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="88670-116">ByTemplateUriWithNoParameters</span></span>
```
New-AzResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88670-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88670-117">DESCRIPTION</span></span>
<span data-ttu-id="88670-118">Командлет **New-AzResourceGroupDeployment** добавляет развертывание в существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88670-118">The **New-AzResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="88670-119">Сюда входят ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="88670-119">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="88670-120">Ресурс Azure — это управляемый пользователем сущность Azure, например сервер базы данных, базу данных, веб-сайт, виртуальную машину или учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="88670-120">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="88670-121">Группа ресурсов Azure — это коллекция ресурсов Azure, которые развертываются как единые, такие как веб-сайт, сервер баз данных и базы данных, необходимые для финансового веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="88670-121">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="88670-122">Развертывание группы ресурсов использует шаблон для добавления ресурсов в группу ресурсов и их публикации, чтобы они были доступны в Azure.</span><span class="sxs-lookup"><span data-stu-id="88670-122">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="88670-123">Чтобы добавить ресурсы в группу ресурсов без использования шаблона, используйте командлет New-AzResource.</span><span class="sxs-lookup"><span data-stu-id="88670-123">To add resources to a resource group without using a template, use the New-AzResource cmdlet.</span></span>
<span data-ttu-id="88670-124">Чтобы добавить развертывание группы ресурсов, укажите имя существующей группы ресурсов и шаблона группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88670-124">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="88670-125">Шаблон группы ресурсов — это строка JSON, представляющая группу ресурсов для сложной облачной службы, например веб-портала.</span><span class="sxs-lookup"><span data-stu-id="88670-125">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="88670-126">Шаблон включает заполнители параметров для необходимых ресурсов и настраиваемых значений свойств, например имен и размеров.</span><span class="sxs-lookup"><span data-stu-id="88670-126">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="88670-127">Вы можете найти большое количество шаблонов в галерее шаблонов Azure или создать собственные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="88670-127">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="88670-128">Вы можете использовать командлет **Get-AzResourceGroupGalleryTemplate** , чтобы найти шаблон в галерее.</span><span class="sxs-lookup"><span data-stu-id="88670-128">You can use the **Get-AzResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="88670-129">Чтобы создать группу ресурсов с помощью настраиваемого шаблона, укажите параметр *TemplateFile* или *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="88670-129">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="88670-130">Каждый шаблон имеет параметры для настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="88670-130">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="88670-131">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или параметр *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="88670-131">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="88670-132">Кроме того, вы можете использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="88670-132">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="88670-133">Чтобы использовать динамические параметры, введите их в командной строке или введите знак "минус" (-), чтобы обозначить параметр, и используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="88670-133">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="88670-134">Значения параметров шаблона, введенные в командной строке, имеют приоритет над значениями в объекте или файле параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="88670-134">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="88670-135">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88670-135">EXAMPLES</span></span>

### <span data-ttu-id="88670-136">Пример 1: использование настраиваемого шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="88670-136">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="88670-137">Эта команда создает новое развертывание с помощью настраиваемого шаблона и файла шаблона на диске.</span><span class="sxs-lookup"><span data-stu-id="88670-137">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="88670-138">В команде используется параметр *TemplateFile* , чтобы указать шаблон и параметр *TemplateParameterFile* , чтобы указать файл, содержащий параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="88670-138">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

### <span data-ttu-id="88670-139">Пример 2: использование настраиваемого объекта шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="88670-139">Example 2: Use a custom template object and parameter file to create a deployment</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> New-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="88670-140">Эта команда создает новое развертывание с помощью настраиваемого и файла шаблона на диске, преобразованного в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="88670-140">This command creates a new deployment by using a custom and a template file on disk that has been converted to an in-memory hashtable.</span></span>
<span data-ttu-id="88670-141">Первые две команды считывают текст файла шаблона на диске и преобразуют его в хэш-таблицу в памяти.</span><span class="sxs-lookup"><span data-stu-id="88670-141">The first two commands read the text for the template file on disk and convert it to an in-memory hashtable.</span></span>
<span data-ttu-id="88670-142">Последняя команда использует параметр *TemplateObject* для указания Hashtable и параметра *TemplateParameterFile* для указания файла, содержащего параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="88670-142">The last command uses the *TemplateObject* parameter to specify the hashtable and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="88670-143">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88670-143">PARAMETERS</span></span>

### <span data-ttu-id="88670-144">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="88670-144">-ApiVersion</span></span>
<span data-ttu-id="88670-145">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88670-145">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="88670-146">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="88670-146">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="88670-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88670-147">-AsJob</span></span>
<span data-ttu-id="88670-148">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="88670-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88670-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88670-149">-DefaultProfile</span></span>
<span data-ttu-id="88670-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="88670-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88670-151">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="88670-151">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="88670-152">Задает уровень журнала отладки.</span><span class="sxs-lookup"><span data-stu-id="88670-152">Specifies a debug log level.</span></span>
<span data-ttu-id="88670-153">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="88670-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88670-154">RequestContent</span><span class="sxs-lookup"><span data-stu-id="88670-154">RequestContent</span></span>
- <span data-ttu-id="88670-155">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="88670-155">ResponseContent</span></span>
- <span data-ttu-id="88670-156">Весь</span><span class="sxs-lookup"><span data-stu-id="88670-156">All</span></span>
- <span data-ttu-id="88670-157">Ничего</span><span class="sxs-lookup"><span data-stu-id="88670-157">None</span></span>

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

### <span data-ttu-id="88670-158">-Force</span><span class="sxs-lookup"><span data-stu-id="88670-158">-Force</span></span>
<span data-ttu-id="88670-159">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="88670-159">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88670-160">Режим</span><span class="sxs-lookup"><span data-stu-id="88670-160">-Mode</span></span>
<span data-ttu-id="88670-161">Задает режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="88670-161">Specifies the deployment mode.</span></span> <span data-ttu-id="88670-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="88670-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="88670-163">Завершено: в режиме завершения диспетчер ресурсов удаляет ресурсы, которые существуют в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="88670-163">Complete: In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> 
- <span data-ttu-id="88670-164">Инкремент. в инкрементном режиме диспетчер ресурсов оставляет неизменные ресурсы, которые есть в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="88670-164">Incremental: In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

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

### <span data-ttu-id="88670-165">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88670-165">-Name</span></span>
<span data-ttu-id="88670-166">Указывает имя создаваемого развертывания группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88670-166">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="88670-167">-Pre</span><span class="sxs-lookup"><span data-stu-id="88670-167">-Pre</span></span>
<span data-ttu-id="88670-168">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="88670-168">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="88670-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88670-169">-ResourceGroupName</span></span>
<span data-ttu-id="88670-170">Указывает имя группы ресурсов для развертывания.</span><span class="sxs-lookup"><span data-stu-id="88670-170">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="88670-171">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="88670-171">-RollBackDeploymentName</span></span>
<span data-ttu-id="88670-172">Откат к успешному развертыванию с указанным именем в группе ресурсов не следует использовать, если используется параметр-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="88670-172">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="88670-173">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="88670-173">-RollbackToLastDeployment</span></span>
<span data-ttu-id="88670-174">Откат к последнему успешному развертыванию в группе ресурсов не отображается, если используется значение-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="88670-174">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="88670-175">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="88670-175">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="88670-176">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="88670-176">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="88670-177">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="88670-177">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="88670-178">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="88670-178">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="88670-179">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="88670-179">-TemplateFile</span></span>
<span data-ttu-id="88670-180">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="88670-180">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="88670-181">Это может быть настраиваемый шаблон или шаблон коллекции, сохраненный в формате JSON, например созданный с помощью командлета **Save-AzResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="88670-181">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="88670-182">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="88670-182">-TemplateObject</span></span>
<span data-ttu-id="88670-183">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="88670-183">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="88670-184">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="88670-184">-TemplateParameterFile</span></span>
<span data-ttu-id="88670-185">Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="88670-185">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="88670-186">Если шаблон имеет параметры, необходимо указать значения параметров с помощью параметра *TemplateParameterFile* или параметра *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="88670-186">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="88670-187">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="88670-187">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="88670-188">Чтобы использовать динамические параметры, введите знак "минус" (-), чтобы обозначить имя параметра, а затем используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="88670-188">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

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

### <span data-ttu-id="88670-189">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="88670-189">-TemplateParameterObject</span></span>
<span data-ttu-id="88670-190">Указывает хэш-таблицу имен и значений параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="88670-190">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="88670-191">Чтобы получить справку по хэш-таблицам в Windows PowerShell, введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="88670-191">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="88670-192">Если у шаблона есть параметры, необходимо указать значения параметров.</span><span class="sxs-lookup"><span data-stu-id="88670-192">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="88670-193">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="88670-193">Template parameters are dynamically added to the command when you specify a template.</span></span>

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

### <span data-ttu-id="88670-194">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="88670-194">-TemplateParameterUri</span></span>
<span data-ttu-id="88670-195">Задает универсальный код ресурса (URI) файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="88670-195">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="88670-196">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="88670-196">-TemplateUri</span></span>
<span data-ttu-id="88670-197">Задает универсальный код ресурса (URI) для файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="88670-197">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="88670-198">Этот файл может быть настраиваемым шаблоном или шаблоном коллекции, сохраненным в формате JSON, например с помощью команды **Save-AzResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="88670-198">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="88670-199">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88670-199">-Confirm</span></span>
<span data-ttu-id="88670-200">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88670-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88670-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88670-201">-WhatIf</span></span>
<span data-ttu-id="88670-202">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88670-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88670-203">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88670-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88670-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88670-204">CommonParameters</span></span>
<span data-ttu-id="88670-205">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88670-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88670-206">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88670-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88670-207">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88670-207">INPUTS</span></span>

### <span data-ttu-id="88670-208">System. String</span><span class="sxs-lookup"><span data-stu-id="88670-208">System.String</span></span>

### <span data-ttu-id="88670-209">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="88670-209">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="88670-210">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="88670-210">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88670-211">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88670-211">OUTPUTS</span></span>

### <span data-ttu-id="88670-212">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88670-212">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="88670-213">Пуск</span><span class="sxs-lookup"><span data-stu-id="88670-213">NOTES</span></span>

## <span data-ttu-id="88670-214">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88670-214">RELATED LINKS</span></span>

[<span data-ttu-id="88670-215">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88670-215">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="88670-216">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="88670-216">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="88670-217">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88670-217">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="88670-218">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88670-218">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="88670-219">Остановить-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88670-219">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="88670-220">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="88670-220">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


