---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: 6c64c9defb3905e9851e79da5303b68e98514f44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914713"
---
# <span data-ttu-id="e27e5-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e27e5-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="e27e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e27e5-102">SYNOPSIS</span></span>
<span data-ttu-id="e27e5-103">Добавляет развертывание Azure в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e27e5-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e27e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e27e5-104">SYNTAX</span></span>

### <span data-ttu-id="e27e5-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e27e5-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27e5-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e27e5-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27e5-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e27e5-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27e5-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e27e5-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27e5-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e27e5-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27e5-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e27e5-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27e5-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e27e5-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27e5-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e27e5-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] [-Force]
 [-AsJob] -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e27e5-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e27e5-113">DESCRIPTION</span></span>
<span data-ttu-id="e27e5-114">Командлет **New-AzureRmResourceGroupDeployment** добавляет развертывание в существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e27e5-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="e27e5-115">Сюда входят ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="e27e5-115">This includes the resources that the deployment requires.</span></span>
<span data-ttu-id="e27e5-116">Ресурс Azure — это управляемый пользователем сущность Azure, например сервер базы данных, базу данных, веб-сайт, виртуальную машину или учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="e27e5-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="e27e5-117">Группа ресурсов Azure — это коллекция ресурсов Azure, которые развертываются как единые, такие как веб-сайт, сервер баз данных и базы данных, необходимые для финансового веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="e27e5-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="e27e5-118">Развертывание группы ресурсов использует шаблон для добавления ресурсов в группу ресурсов и их публикации, чтобы они были доступны в Azure.</span><span class="sxs-lookup"><span data-stu-id="e27e5-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="e27e5-119">Чтобы добавить ресурсы в группу ресурсов без использования шаблона, используйте командлет New-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="e27e5-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>
<span data-ttu-id="e27e5-120">Чтобы добавить развертывание группы ресурсов, укажите имя существующей группы ресурсов и шаблона группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e27e5-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="e27e5-121">Шаблон группы ресурсов — это строка JSON, представляющая группу ресурсов для сложной облачной службы, например веб-портала.</span><span class="sxs-lookup"><span data-stu-id="e27e5-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="e27e5-122">Шаблон включает заполнители параметров для необходимых ресурсов и настраиваемых значений свойств, например имен и размеров.</span><span class="sxs-lookup"><span data-stu-id="e27e5-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="e27e5-123">Вы можете найти большое количество шаблонов в галерее шаблонов Azure или создать собственные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="e27e5-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="e27e5-124">Вы можете использовать командлет **Get-AzureRmResourceGroupGalleryTemplate** , чтобы найти шаблон в галерее.</span><span class="sxs-lookup"><span data-stu-id="e27e5-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>
<span data-ttu-id="e27e5-125">Чтобы создать группу ресурсов с помощью настраиваемого шаблона, укажите параметр *TemplateFile* или *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="e27e5-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="e27e5-126">Каждый шаблон имеет параметры для настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="e27e5-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="e27e5-127">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или параметр *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="e27e5-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="e27e5-128">Кроме того, вы можете использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="e27e5-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="e27e5-129">Чтобы использовать динамические параметры, введите их в командной строке или введите знак "минус" (-), чтобы обозначить параметр, и используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="e27e5-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="e27e5-130">Значения параметров шаблона, введенные в командной строке, имеют приоритет над значениями в объекте или файле параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="e27e5-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="e27e5-131">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e27e5-131">EXAMPLES</span></span>

### <span data-ttu-id="e27e5-132">Пример 1: использование настраиваемого шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="e27e5-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="e27e5-133">Эта команда создает новое развертывание с помощью настраиваемого шаблона и файла шаблона на диске.</span><span class="sxs-lookup"><span data-stu-id="e27e5-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="e27e5-134">В команде используется параметр *TemplateFile* , чтобы указать шаблон и параметр *TemplateParameterFile* , чтобы указать файл, содержащий параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="e27e5-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>

## <span data-ttu-id="e27e5-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e27e5-135">PARAMETERS</span></span>

### <span data-ttu-id="e27e5-136">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e27e5-136">-ApiVersion</span></span>
<span data-ttu-id="e27e5-137">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e27e5-137">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e27e5-138">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e27e5-138">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e27e5-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e27e5-139">-AsJob</span></span>
<span data-ttu-id="e27e5-140">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e27e5-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e27e5-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27e5-141">-DefaultProfile</span></span>
<span data-ttu-id="e27e5-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e27e5-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27e5-143">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="e27e5-143">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="e27e5-144">Задает уровень журнала отладки.</span><span class="sxs-lookup"><span data-stu-id="e27e5-144">Specifies a debug log level.</span></span>
<span data-ttu-id="e27e5-145">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e27e5-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e27e5-146">RequestContent</span><span class="sxs-lookup"><span data-stu-id="e27e5-146">RequestContent</span></span>
- <span data-ttu-id="e27e5-147">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="e27e5-147">ResponseContent</span></span>
- <span data-ttu-id="e27e5-148">Весь</span><span class="sxs-lookup"><span data-stu-id="e27e5-148">All</span></span>
- <span data-ttu-id="e27e5-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="e27e5-149">None</span></span>

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

### <span data-ttu-id="e27e5-150">-Force</span><span class="sxs-lookup"><span data-stu-id="e27e5-150">-Force</span></span>
<span data-ttu-id="e27e5-151">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e27e5-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e27e5-152">Режим</span><span class="sxs-lookup"><span data-stu-id="e27e5-152">-Mode</span></span>
<span data-ttu-id="e27e5-153">Задает режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="e27e5-153">Specifies the deployment mode.</span></span> <span data-ttu-id="e27e5-154">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e27e5-154">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e27e5-155">Полнот</span><span class="sxs-lookup"><span data-stu-id="e27e5-155">Complete</span></span>
- <span data-ttu-id="e27e5-156">Инкрементный режим. в этом режиме диспетчер ресурсов удаляет ресурсы, которые существуют в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="e27e5-156">Incremental In complete mode, Resource Manager deletes resources that exist in the resource group but are not specified in the template.</span></span> <span data-ttu-id="e27e5-157">В инкрементном режиме диспетчер ресурсов оставляет неизменные ресурсы, которые есть в группе ресурсов, но не указаны в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="e27e5-157">In incremental mode, Resource Manager leaves unchanged resources that exist in the resource group but are not specified in the template.</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Incremental
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27e5-158">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e27e5-158">-Name</span></span>
<span data-ttu-id="e27e5-159">Указывает имя создаваемого развертывания группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e27e5-159">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="e27e5-160">-Pre</span><span class="sxs-lookup"><span data-stu-id="e27e5-160">-Pre</span></span>
<span data-ttu-id="e27e5-161">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="e27e5-161">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e27e5-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27e5-162">-ResourceGroupName</span></span>
<span data-ttu-id="e27e5-163">Указывает имя группы ресурсов для развертывания.</span><span class="sxs-lookup"><span data-stu-id="e27e5-163">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="e27e5-164">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="e27e5-164">-RollBackDeploymentName</span></span>
<span data-ttu-id="e27e5-165">Откат к успешному развертыванию с указанным именем в группе ресурсов не следует использовать, если используется параметр-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="e27e5-165">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="e27e5-166">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="e27e5-166">-RollbackToLastDeployment</span></span>
<span data-ttu-id="e27e5-167">Откат к последнему успешному развертыванию в группе ресурсов не отображается, если используется значение-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="e27e5-167">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="e27e5-168">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e27e5-168">-TemplateFile</span></span>
<span data-ttu-id="e27e5-169">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="e27e5-169">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="e27e5-170">Это может быть настраиваемый шаблон или шаблон коллекции, сохраненный в формате JSON, например созданный с помощью командлета **Save-AzureRmResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="e27e5-170">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

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

### <span data-ttu-id="e27e5-171">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e27e5-171">-TemplateParameterFile</span></span>
<span data-ttu-id="e27e5-172">Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="e27e5-172">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="e27e5-173">Если шаблон имеет параметры, необходимо указать значения параметров с помощью параметра *TemplateParameterFile* или параметра *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="e27e5-173">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="e27e5-174">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="e27e5-174">Template parameters are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="e27e5-175">Чтобы использовать динамические параметры, введите знак "минус" (-), чтобы обозначить имя параметра, а затем используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="e27e5-175">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27e5-176">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e27e5-176">-TemplateParameterObject</span></span>
<span data-ttu-id="e27e5-177">Указывает хэш-таблицу имен и значений параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="e27e5-177">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="e27e5-178">Чтобы получить справку по хэш-таблицам в Windows PowerShell, введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="e27e5-178">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="e27e5-179">Если у шаблона есть параметры, необходимо указать значения параметров.</span><span class="sxs-lookup"><span data-stu-id="e27e5-179">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="e27e5-180">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="e27e5-180">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27e5-181">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e27e5-181">-TemplateParameterUri</span></span>
<span data-ttu-id="e27e5-182">Задает универсальный код ресурса (URI) файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="e27e5-182">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e27e5-183">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e27e5-183">-TemplateUri</span></span>
<span data-ttu-id="e27e5-184">Задает универсальный код ресурса (URI) для файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="e27e5-184">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="e27e5-185">Этот файл может быть настраиваемым шаблоном или шаблоном коллекции, сохраненным в формате JSON, например с помощью команды **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="e27e5-185">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

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

### <span data-ttu-id="e27e5-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e27e5-186">-Confirm</span></span>
<span data-ttu-id="e27e5-187">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e27e5-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e27e5-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e27e5-188">-WhatIf</span></span>
<span data-ttu-id="e27e5-189">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e27e5-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e27e5-190">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e27e5-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e27e5-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27e5-191">CommonParameters</span></span>
<span data-ttu-id="e27e5-192">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e27e5-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27e5-193">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e27e5-193">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27e5-194">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e27e5-194">INPUTS</span></span>

### <span data-ttu-id="e27e5-195">Ничего</span><span class="sxs-lookup"><span data-stu-id="e27e5-195">None</span></span>

## <span data-ttu-id="e27e5-196">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e27e5-196">OUTPUTS</span></span>

### <span data-ttu-id="e27e5-197">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e27e5-197">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="e27e5-198">Пуск</span><span class="sxs-lookup"><span data-stu-id="e27e5-198">NOTES</span></span>

## <span data-ttu-id="e27e5-199">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e27e5-199">RELATED LINKS</span></span>

[<span data-ttu-id="e27e5-200">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e27e5-200">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e27e5-201">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e27e5-201">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e27e5-202">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e27e5-202">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="e27e5-203">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e27e5-203">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e27e5-204">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e27e5-204">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="e27e5-205">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e27e5-205">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


