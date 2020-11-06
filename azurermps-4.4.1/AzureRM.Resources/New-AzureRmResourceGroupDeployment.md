---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6E2F0D5E-E683-46F3-B48B-55C4864F3308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 9512a8ae8e6bbd54704212539ad0650797cf4604
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567075"
---
# <span data-ttu-id="d368e-101">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d368e-101">New-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="d368e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d368e-102">SYNOPSIS</span></span>
<span data-ttu-id="d368e-103">Добавляет развертывание Azure в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d368e-103">Adds an Azure deployment to a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d368e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d368e-104">SYNTAX</span></span>

### <span data-ttu-id="d368e-105">Развертывание с помощью файла шаблона без параметров (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d368e-105">Deployment via template file without parameters (Default)</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d368e-106">Развертывание с помощью файла шаблона и объекта "Параметры шаблона"</span><span class="sxs-lookup"><span data-stu-id="d368e-106">Deployment via template file and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d368e-107">Развертывание с помощью URI шаблона и объекта "Параметры шаблона"</span><span class="sxs-lookup"><span data-stu-id="d368e-107">Deployment via template uri and template parameters object</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d368e-108">Развертывание с помощью файла шаблона и файла параметров шаблона</span><span class="sxs-lookup"><span data-stu-id="d368e-108">Deployment via template file and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d368e-109">Развертывание с помощью URI шаблона и файла параметров шаблона</span><span class="sxs-lookup"><span data-stu-id="d368e-109">Deployment via template uri and template parameters file</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d368e-110">Развертывание с помощью URI параметров шаблона файла шаблона</span><span class="sxs-lookup"><span data-stu-id="d368e-110">Deployment via template file template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d368e-111">Развертывание с помощью URI шаблона и URI параметров шаблона</span><span class="sxs-lookup"><span data-stu-id="d368e-111">Deployment via template uri and template parameters uri</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d368e-112">Развертывание с помощью URI шаблона без параметров</span><span class="sxs-lookup"><span data-stu-id="d368e-112">Deployment via template uri without parameters</span></span>
```
New-AzureRmResourceGroupDeployment [-Name <String>] -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-DeploymentDebugLogLevel <String>] [-Force] -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d368e-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d368e-113">DESCRIPTION</span></span>
<span data-ttu-id="d368e-114">Командлет **New-AzureRmResourceGroupDeployment** добавляет развертывание в существующую группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d368e-114">The **New-AzureRmResourceGroupDeployment** cmdlet adds a deployment to an existing resource group.</span></span>
<span data-ttu-id="d368e-115">Сюда входят ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="d368e-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="d368e-116">Ресурс Azure — это управляемый пользователем сущность Azure, например сервер базы данных, базу данных, веб-сайт, виртуальную машину или учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="d368e-116">An Azure resource is a user-managed Azure entity, such as a database server, database, website, virtual machine, or Storage account.</span></span>
<span data-ttu-id="d368e-117">Группа ресурсов Azure — это коллекция ресурсов Azure, которые развертываются как единые, такие как веб-сайт, сервер баз данных и базы данных, необходимые для финансового веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="d368e-117">An Azure resource group is a collection of Azure resources that are deployed as a unit, such as the website, database server, and databases that are required for a financial website.</span></span>
<span data-ttu-id="d368e-118">Развертывание группы ресурсов использует шаблон для добавления ресурсов в группу ресурсов и их публикации, чтобы они были доступны в Azure.</span><span class="sxs-lookup"><span data-stu-id="d368e-118">A resource group deployment uses a template to add resources to a resource group and publishes them so that they are available in Azure.</span></span>
<span data-ttu-id="d368e-119">Чтобы добавить ресурсы в группу ресурсов без использования шаблона, используйте командлет New-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="d368e-119">To add resources to a resource group without using a template, use the New-AzureRmResource cmdlet.</span></span>

<span data-ttu-id="d368e-120">Чтобы добавить развертывание группы ресурсов, укажите имя существующей группы ресурсов и шаблона группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d368e-120">To add a resource group deployment, specify the name of an existing resource group and a resource group template.</span></span>
<span data-ttu-id="d368e-121">Шаблон группы ресурсов — это строка JSON, представляющая группу ресурсов для сложной облачной службы, например веб-портала.</span><span class="sxs-lookup"><span data-stu-id="d368e-121">A resource group template is a JSON string that represents a resource group for a complex cloud-based service, such as a web portal.</span></span>
<span data-ttu-id="d368e-122">Шаблон включает заполнители параметров для необходимых ресурсов и настраиваемых значений свойств, например имен и размеров.</span><span class="sxs-lookup"><span data-stu-id="d368e-122">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>
<span data-ttu-id="d368e-123">Вы можете найти большое количество шаблонов в галерее шаблонов Azure или создать собственные шаблоны.</span><span class="sxs-lookup"><span data-stu-id="d368e-123">You can find many templates in the Azure template gallery or you can create your own templates.</span></span>
<span data-ttu-id="d368e-124">Вы можете использовать командлет **Get-AzureRmResourceGroupGalleryTemplate** , чтобы найти шаблон в галерее.</span><span class="sxs-lookup"><span data-stu-id="d368e-124">You can use the **Get-AzureRmResourceGroupGalleryTemplate** cmdlet to find a template in the gallery.</span></span>

<span data-ttu-id="d368e-125">Чтобы создать группу ресурсов с помощью настраиваемого шаблона, укажите параметр *TemplateFile* или *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="d368e-125">To use a custom template to create a resource group, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="d368e-126">Каждый шаблон имеет параметры для настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="d368e-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="d368e-127">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или параметр *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="d368e-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d368e-128">Кроме того, вы можете использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="d368e-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="d368e-129">Чтобы использовать динамические параметры, введите их в командной строке или введите знак "минус" (-), чтобы обозначить параметр, и используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="d368e-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="d368e-130">Значения параметров шаблона, введенные в командной строке, имеют приоритет над значениями в объекте или файле параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="d368e-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="d368e-131">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d368e-131">EXAMPLES</span></span>

### <span data-ttu-id="d368e-132">Пример 1: использование настраиваемого шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="d368e-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="d368e-133">Эта команда создает новое развертывание с помощью настраиваемого шаблона и файла шаблона на диске.</span><span class="sxs-lookup"><span data-stu-id="d368e-133">This command creates a new deployment by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="d368e-134">В команде используется параметр *TemplateFile* , чтобы указать шаблон и параметр *TemplateParameterFile* , чтобы указать файл, содержащий параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="d368e-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="d368e-135">Для указания версии шаблона используется параметр *TemplateVersion* .</span><span class="sxs-lookup"><span data-stu-id="d368e-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="d368e-136">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d368e-136">PARAMETERS</span></span>

### <span data-ttu-id="d368e-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d368e-137">-ApiVersion</span></span>
<span data-ttu-id="d368e-138">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d368e-138">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d368e-139">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d368e-139">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d368e-140">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="d368e-140">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="d368e-141">Задает уровень журнала отладки.</span><span class="sxs-lookup"><span data-stu-id="d368e-141">Specifies a debug log level.</span></span>
<span data-ttu-id="d368e-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d368e-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d368e-143">RequestContent</span><span class="sxs-lookup"><span data-stu-id="d368e-143">RequestContent</span></span> 
- <span data-ttu-id="d368e-144">ResponseContent</span><span class="sxs-lookup"><span data-stu-id="d368e-144">ResponseContent</span></span> 
- <span data-ttu-id="d368e-145">Весь</span><span class="sxs-lookup"><span data-stu-id="d368e-145">All</span></span> 
- <span data-ttu-id="d368e-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="d368e-146">None</span></span>

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

### <span data-ttu-id="d368e-147">-Force</span><span class="sxs-lookup"><span data-stu-id="d368e-147">-Force</span></span>
<span data-ttu-id="d368e-148">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d368e-148">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d368e-149">Режим</span><span class="sxs-lookup"><span data-stu-id="d368e-149">-Mode</span></span>
<span data-ttu-id="d368e-150">Задает режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="d368e-150">Specifies the deployment mode.</span></span> <span data-ttu-id="d368e-151">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d368e-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d368e-152">Полнот</span><span class="sxs-lookup"><span data-stu-id="d368e-152">Complete</span></span> 
- <span data-ttu-id="d368e-153">Разност</span><span class="sxs-lookup"><span data-stu-id="d368e-153">Incremental</span></span>

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

### <span data-ttu-id="d368e-154">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d368e-154">-Name</span></span>
<span data-ttu-id="d368e-155">Указывает имя создаваемого развертывания группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d368e-155">Specifies the name of the resource group deployment to create.</span></span>

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

### <span data-ttu-id="d368e-156">-Pre</span><span class="sxs-lookup"><span data-stu-id="d368e-156">-Pre</span></span>
<span data-ttu-id="d368e-157">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="d368e-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d368e-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d368e-158">-ResourceGroupName</span></span>
<span data-ttu-id="d368e-159">Указывает имя группы ресурсов для развертывания.</span><span class="sxs-lookup"><span data-stu-id="d368e-159">Specifies the name of the resource group to deploy.</span></span>

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

### <span data-ttu-id="d368e-160">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="d368e-160">-TemplateFile</span></span>
<span data-ttu-id="d368e-161">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="d368e-161">Specifies the full path of a JSON template file.</span></span>
<span data-ttu-id="d368e-162">Это может быть настраиваемый шаблон или шаблон коллекции, сохраненный в формате JSON, например созданный с помощью командлета **Save-AzureRmResourceGroupGalleryTemplate** .</span><span class="sxs-lookup"><span data-stu-id="d368e-162">This can be a custom template or a gallery template that is saved as a JSON file, such as one created by using the **Save-AzureRmResourceGroupGalleryTemplate** cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d368e-163">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="d368e-163">-TemplateParameterFile</span></span>
<span data-ttu-id="d368e-164">Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="d368e-164">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>
<span data-ttu-id="d368e-165">Если шаблон имеет параметры, необходимо указать значения параметров с помощью параметра *TemplateParameterFile* или параметра *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="d368e-165">If a template has parameters, you must specify the parameter values with the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="d368e-166">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="d368e-166">Template parameters are dynamically added to the command when you specify a template.</span></span>

<span data-ttu-id="d368e-167">Чтобы использовать динамические параметры, введите знак "минус" (-), чтобы обозначить имя параметра, а затем используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="d368e-167">To use the dynamic parameters, type a minus sign (-) to indicate a parameter name and then use the Tab key to cycle through the available parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d368e-168">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="d368e-168">-TemplateParameterObject</span></span>
<span data-ttu-id="d368e-169">Указывает хэш-таблицу имен и значений параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="d368e-169">Specifies a hash table of template parameter names and values.</span></span>
<span data-ttu-id="d368e-170">Чтобы получить справку по хэш-таблицам в Windows PowerShell, введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="d368e-170">For help with hash tables in Windows PowerShell, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="d368e-171">Если у шаблона есть параметры, необходимо указать значения параметров.</span><span class="sxs-lookup"><span data-stu-id="d368e-171">If a template has parameters, you must specify parameter values.</span></span>
<span data-ttu-id="d368e-172">Параметры шаблона динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="d368e-172">Template parameters are dynamically added to the command when you specify a template.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d368e-173">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="d368e-173">-TemplateParameterUri</span></span>
<span data-ttu-id="d368e-174">Задает универсальный код ресурса (URI) файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="d368e-174">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d368e-175">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="d368e-175">-TemplateUri</span></span>
<span data-ttu-id="d368e-176">Задает универсальный код ресурса (URI) для файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="d368e-176">Specifies the URI of a JSON template file.</span></span>
<span data-ttu-id="d368e-177">Этот файл может быть настраиваемым шаблоном или шаблоном коллекции, сохраненным в формате JSON, например с помощью команды **Save-AzureRmResourceGroupGalleryTemplate**.</span><span class="sxs-lookup"><span data-stu-id="d368e-177">This file can be a custom template or a gallery template that is saved as a JSON file, such as by using **Save-AzureRmResourceGroupGalleryTemplate**.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d368e-178">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d368e-178">-Confirm</span></span>
<span data-ttu-id="d368e-179">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d368e-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d368e-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d368e-180">-WhatIf</span></span>
<span data-ttu-id="d368e-181">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d368e-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d368e-182">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d368e-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d368e-183">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d368e-183">-DefaultProfile</span></span>
<span data-ttu-id="d368e-184">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d368e-184">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d368e-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d368e-185">CommonParameters</span></span>
<span data-ttu-id="d368e-186">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d368e-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d368e-187">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d368e-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d368e-188">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d368e-188">INPUTS</span></span>

### <span data-ttu-id="d368e-189">Ничего</span><span class="sxs-lookup"><span data-stu-id="d368e-189">None</span></span>

## <span data-ttu-id="d368e-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d368e-190">OUTPUTS</span></span>

### <span data-ttu-id="d368e-191">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d368e-191">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="d368e-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="d368e-192">NOTES</span></span>

## <span data-ttu-id="d368e-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d368e-193">RELATED LINKS</span></span>

[<span data-ttu-id="d368e-194">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d368e-194">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d368e-195">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d368e-195">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="d368e-196">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d368e-196">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="d368e-197">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d368e-197">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d368e-198">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d368e-198">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d368e-199">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d368e-199">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


