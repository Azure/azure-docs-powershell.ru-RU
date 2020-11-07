---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzDeployment.md
ms.openlocfilehash: 97d6b11a4993ced62b84de24c501a2c438173141
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910902"
---
# <span data-ttu-id="1ef05-101">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="1ef05-101">New-AzDeployment</span></span>

## <span data-ttu-id="1ef05-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ef05-102">SYNOPSIS</span></span>
<span data-ttu-id="1ef05-103">Создать развертывание</span><span class="sxs-lookup"><span data-stu-id="1ef05-103">Creat a deployment</span></span>

## <span data-ttu-id="1ef05-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ef05-104">SYNTAX</span></span>

### <span data-ttu-id="1ef05-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1ef05-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef05-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1ef05-106">ByTemplateFileAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef05-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="1ef05-107">ByTemplateUriAndParameterObject</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef05-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1ef05-108">ByTemplateFileAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef05-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="1ef05-109">ByTemplateUriAndParameterFile</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef05-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1ef05-110">ByTemplateFileAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef05-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="1ef05-111">ByTemplateUriAndParameterUri</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ef05-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="1ef05-112">ByTemplateUriWithNoParameters</span></span>
```
New-AzDeployment [-Name <String>] -Location <String> [-DeploymentDebugLogLevel <String>] [-AsJob]
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ef05-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ef05-113">DESCRIPTION</span></span>
<span data-ttu-id="1ef05-114">Командлет **New-AzDeployment** добавляет развертывание в текущую область подписки.</span><span class="sxs-lookup"><span data-stu-id="1ef05-114">The **New-AzDeployment** cmdlet adds a deployment at the current subscription scope.</span></span>
<span data-ttu-id="1ef05-115">Сюда входят ресурсы, необходимые для развертывания.</span><span class="sxs-lookup"><span data-stu-id="1ef05-115">This includes the resources that the deployment requires.</span></span>

<span data-ttu-id="1ef05-116">Ресурс Azure — это управляемая пользователем сущность Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef05-116">An Azure resource is a user-managed Azure entity.</span></span> <span data-ttu-id="1ef05-117">Ресурс может находиться в группе ресурсов, например на сервере базы данных, базе данных, веб-сайте, виртуальной машине или учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1ef05-117">A resource can live in a resource group, like database server, database, website, virtual machine, or Storage account.</span></span> <span data-ttu-id="1ef05-118">Или это может быть ресурс уровня подписки, например определение роли, определение политики и т. д.</span><span class="sxs-lookup"><span data-stu-id="1ef05-118">Or, it can be a subscription level resource, like role definition, policy definition, etc.</span></span>

<span data-ttu-id="1ef05-119">Чтобы добавить ресурсы в группу ресурсов, используйте **New-AzDeployment** , который создает развертывание в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ef05-119">To add resources to a resource group, use the **New-AzDeployment** which creates a deployment at a resource group.</span></span>
<span data-ttu-id="1ef05-120">Командлет **New-AzDeployment** создает развертывание в текущей области подписки, которое развертывает ресурсы уровня подписки.</span><span class="sxs-lookup"><span data-stu-id="1ef05-120">The **New-AzDeployment** cmdlet creates a deployment at the current subscription scope, which deploys subscription level resources.</span></span> 

<span data-ttu-id="1ef05-121">Чтобы добавить развертывание на подписку, укажите расположение и шаблон.</span><span class="sxs-lookup"><span data-stu-id="1ef05-121">To add a deployment at subscription, specify the location and a template.</span></span>
<span data-ttu-id="1ef05-122">Расположение указывает диспетчеру ресурсов Azure, где хранятся данные развертывания.</span><span class="sxs-lookup"><span data-stu-id="1ef05-122">The location tells Azure Resource Manager where to store the deployment data.</span></span> <span data-ttu-id="1ef05-123">Шаблон — это строка JSON, содержащая отдельные ресурсы для развертывания.</span><span class="sxs-lookup"><span data-stu-id="1ef05-123">The template is a JSON string that contains individual resources to be deployed.</span></span>
<span data-ttu-id="1ef05-124">Шаблон включает заполнители параметров для необходимых ресурсов и настраиваемых значений свойств, например имен и размеров.</span><span class="sxs-lookup"><span data-stu-id="1ef05-124">The template includes parameter placeholders for required resources and configurable property values, such as names and sizes.</span></span>

<span data-ttu-id="1ef05-125">Чтобы использовать настраиваемый шаблон для развертывания, укажите параметр *TemplateFile* или *TemplateUri* .</span><span class="sxs-lookup"><span data-stu-id="1ef05-125">To use a custom template for the deployment, specify the *TemplateFile* parameter or *TemplateUri* parameter.</span></span>
<span data-ttu-id="1ef05-126">Каждый шаблон имеет параметры для настраиваемых свойств.</span><span class="sxs-lookup"><span data-stu-id="1ef05-126">Each template has parameters for configurable properties.</span></span>
<span data-ttu-id="1ef05-127">Чтобы задать значения для параметров шаблона, укажите параметр *TemplateParameterFile* или параметр *TemplateParameterObject* .</span><span class="sxs-lookup"><span data-stu-id="1ef05-127">To specify values for the template parameters, specify the *TemplateParameterFile* parameter or the *TemplateParameterObject* parameter.</span></span>
<span data-ttu-id="1ef05-128">Кроме того, вы можете использовать параметры шаблона, которые динамически добавляются в команду при указании шаблона.</span><span class="sxs-lookup"><span data-stu-id="1ef05-128">Alternatively, you can use the template parameters that are dynamically added to the command when you specify a template.</span></span>
<span data-ttu-id="1ef05-129">Чтобы использовать динамические параметры, введите их в командной строке или введите знак "минус" (-), чтобы обозначить параметр, и используйте клавишу TAB для переключения между доступными параметрами.</span><span class="sxs-lookup"><span data-stu-id="1ef05-129">To use dynamic parameters, type them at the command prompt, or type a minus sign (-) to indicate a parameter and use the Tab key to cycle through available parameters.</span></span>
<span data-ttu-id="1ef05-130">Значения параметров шаблона, введенные в командной строке, имеют приоритет над значениями в объекте или файле параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="1ef05-130">Template parameter values that you enter at the command prompt take precedence over values in a template parameter object or file.</span></span>

## <span data-ttu-id="1ef05-131">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ef05-131">EXAMPLES</span></span>

### <span data-ttu-id="1ef05-132">Пример 1: использование настраиваемого шаблона и файла параметров для создания развертывания</span><span class="sxs-lookup"><span data-stu-id="1ef05-132">Example 1: Use a custom template and parameter file to create a deployment</span></span>
```
PS C:\>New-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json" -TemplateVersion "2.1"
```

<span data-ttu-id="1ef05-133">Эта команда создает новое развертывание в текущей области подписки с помощью настраиваемого шаблона и файла шаблона на диске.</span><span class="sxs-lookup"><span data-stu-id="1ef05-133">This command creates a new deployment at the current subscription scope by using a custom template and a template file on disk.</span></span>
<span data-ttu-id="1ef05-134">В команде используется параметр *TemplateFile* , чтобы указать шаблон и параметр *TemplateParameterFile* , чтобы указать файл, содержащий параметры и значения параметров.</span><span class="sxs-lookup"><span data-stu-id="1ef05-134">The command uses the *TemplateFile* parameter to specify the template and the *TemplateParameterFile* parameter to specify a file that contains parameters and parameter values.</span></span>
<span data-ttu-id="1ef05-135">Для указания версии шаблона используется параметр *TemplateVersion* .</span><span class="sxs-lookup"><span data-stu-id="1ef05-135">It uses the *TemplateVersion* parameter to specify the version of the template.</span></span>

## <span data-ttu-id="1ef05-136">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ef05-136">PARAMETERS</span></span>

### <span data-ttu-id="1ef05-137">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1ef05-137">-ApiVersion</span></span>
<span data-ttu-id="1ef05-138">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ef05-138">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1ef05-139">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="1ef05-139">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1ef05-140">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ef05-140">-AsJob</span></span>
<span data-ttu-id="1ef05-141">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1ef05-141">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ef05-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ef05-142">-DefaultProfile</span></span>
<span data-ttu-id="1ef05-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ef05-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ef05-144">-DeploymentDebugLogLevel</span><span class="sxs-lookup"><span data-stu-id="1ef05-144">-DeploymentDebugLogLevel</span></span>
<span data-ttu-id="1ef05-145">Уровень журнала отладки развертывания.</span><span class="sxs-lookup"><span data-stu-id="1ef05-145">The deployment debug log level.</span></span>

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

### <span data-ttu-id="1ef05-146">-Location</span><span class="sxs-lookup"><span data-stu-id="1ef05-146">-Location</span></span>
<span data-ttu-id="1ef05-147">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="1ef05-147">The location to store deployment data.</span></span>

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

### <span data-ttu-id="1ef05-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ef05-148">-Name</span></span>
<span data-ttu-id="1ef05-149">Имя развертывания, которое будет создано.</span><span class="sxs-lookup"><span data-stu-id="1ef05-149">The name of the deployment it's going to create.</span></span>
<span data-ttu-id="1ef05-150">Действительно только при использовании шаблона.</span><span class="sxs-lookup"><span data-stu-id="1ef05-150">Only valid when a template is used.</span></span>
<span data-ttu-id="1ef05-151">При использовании шаблона, если пользователь не указывает имя развертывания, используйте текущее время, например "20131223140835".</span><span class="sxs-lookup"><span data-stu-id="1ef05-151">When a template is used, if the user doesn't specify a deployment name, use the current time, like "20131223140835".</span></span>

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

### <span data-ttu-id="1ef05-152">-Pre</span><span class="sxs-lookup"><span data-stu-id="1ef05-152">-Pre</span></span>
<span data-ttu-id="1ef05-153">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="1ef05-153">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1ef05-154">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="1ef05-154">-TemplateFile</span></span>
<span data-ttu-id="1ef05-155">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="1ef05-155">Local path to the template file.</span></span>

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

### <span data-ttu-id="1ef05-156">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="1ef05-156">-TemplateParameterFile</span></span>
<span data-ttu-id="1ef05-157">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="1ef05-157">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef05-158">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="1ef05-158">-TemplateParameterObject</span></span>
<span data-ttu-id="1ef05-159">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="1ef05-159">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef05-160">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="1ef05-160">-TemplateParameterUri</span></span>
<span data-ttu-id="1ef05-161">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="1ef05-161">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ef05-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="1ef05-162">-TemplateUri</span></span>
<span data-ttu-id="1ef05-163">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="1ef05-163">Uri to the template file.</span></span>

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

### <span data-ttu-id="1ef05-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ef05-164">-Confirm</span></span>
<span data-ttu-id="1ef05-165">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1ef05-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ef05-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ef05-166">-WhatIf</span></span>
<span data-ttu-id="1ef05-167">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1ef05-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ef05-168">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1ef05-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ef05-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ef05-169">CommonParameters</span></span>
<span data-ttu-id="1ef05-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ef05-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ef05-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ef05-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ef05-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ef05-172">INPUTS</span></span>

### <span data-ttu-id="1ef05-173">System. String</span><span class="sxs-lookup"><span data-stu-id="1ef05-173">System.String</span></span>
<span data-ttu-id="1ef05-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ef05-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1ef05-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ef05-175">OUTPUTS</span></span>

### <span data-ttu-id="1ef05-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1ef05-176">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1ef05-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ef05-177">NOTES</span></span>

## <span data-ttu-id="1ef05-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ef05-178">RELATED LINKS</span></span>
