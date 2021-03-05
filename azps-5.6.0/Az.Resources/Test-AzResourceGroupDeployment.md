---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 0e0d4645901f60f9e290d197a47b133d6bf3db8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976456"
---
# <span data-ttu-id="937cc-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="937cc-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="937cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="937cc-102">SYNOPSIS</span></span>
<span data-ttu-id="937cc-103">Проверка развертывания группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="937cc-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="937cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="937cc-104">SYNTAX</span></span>

### <span data-ttu-id="937cc-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="937cc-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="937cc-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="937cc-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="937cc-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="937cc-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="937cc-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="937cc-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="937cc-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="937cc-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="937cc-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="937cc-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="937cc-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="937cc-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="937cc-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="937cc-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="937cc-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="937cc-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="937cc-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="937cc-119">ByTemplateSpecResourceId</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="937cc-120">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="937cc-120">DESCRIPTION</span></span>
<span data-ttu-id="937cc-121">С **его** использованием можно определить, допустим ли шаблон развертывания группы ресурсов Azure и его значения параметров.</span><span class="sxs-lookup"><span data-stu-id="937cc-121">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="937cc-122">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="937cc-122">EXAMPLES</span></span>

### <span data-ttu-id="937cc-123">Пример 1. Тестовая развертывание с объектом настраиваемого шаблона и файлом параметров</span><span class="sxs-lookup"><span data-stu-id="937cc-123">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="937cc-124">Эта команда проверяет развертывание в заданной группе ресурсов с использованием в памяти файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="937cc-124">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="937cc-125">Пример 2. Тестирование развертывания с помощью файла шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="937cc-125">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="937cc-126">Эта команда проверяет развертывание в заданной группе ресурсов и ресурса, используя предоставленный файл шаблона и файл параметров.</span><span class="sxs-lookup"><span data-stu-id="937cc-126">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="937cc-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="937cc-127">PARAMETERS</span></span>

### <span data-ttu-id="937cc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937cc-128">-DefaultProfile</span></span>
<span data-ttu-id="937cc-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="937cc-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="937cc-130">-Mode</span><span class="sxs-lookup"><span data-stu-id="937cc-130">-Mode</span></span>
<span data-ttu-id="937cc-131">Режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="937cc-131">Specifies the deployment mode.</span></span>
<span data-ttu-id="937cc-132">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="937cc-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="937cc-133">Приращение</span><span class="sxs-lookup"><span data-stu-id="937cc-133">Incremental</span></span>
- <span data-ttu-id="937cc-134">Завершено</span><span class="sxs-lookup"><span data-stu-id="937cc-134">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="937cc-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="937cc-135">-Pre</span></span>
<span data-ttu-id="937cc-136">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="937cc-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="937cc-137">-QueryString</span><span class="sxs-lookup"><span data-stu-id="937cc-137">-QueryString</span></span>
<span data-ttu-id="937cc-138">Строка запроса (например, токен SAS), которая будет использоваться с параметром TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="937cc-138">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="937cc-139">Будет использоваться в случае связанных шаблонов</span><span class="sxs-lookup"><span data-stu-id="937cc-139">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="937cc-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="937cc-140">-ResourceGroupName</span></span>
<span data-ttu-id="937cc-141">Указывает имя группы ресурсов, которая будет протестирована.</span><span class="sxs-lookup"><span data-stu-id="937cc-141">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="937cc-142">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="937cc-142">-RollBackDeploymentName</span></span>
<span data-ttu-id="937cc-143">Откат до успешного развертывания с заданным именем в группе ресурсов не следует использовать, если используется -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="937cc-143">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="937cc-144">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="937cc-144">-RollbackToLastDeployment</span></span>
<span data-ttu-id="937cc-145">При этом не должно быть отката до последнего успешного развертывания в группе ресурсов, если используется имя -RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="937cc-145">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="937cc-146">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="937cc-146">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="937cc-147">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="937cc-147">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="937cc-148">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="937cc-148">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="937cc-149">Для неинтерационных сценариев можно использовать параметр SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="937cc-149">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="937cc-150">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="937cc-150">-TemplateFile</span></span>
<span data-ttu-id="937cc-151">Указывает полный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="937cc-151">Specifies the full path of a template file.</span></span> <span data-ttu-id="937cc-152">Поддерживаемый тип файла шаблона: json и bicep.</span><span class="sxs-lookup"><span data-stu-id="937cc-152">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="937cc-153">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="937cc-153">-TemplateObject</span></span>
<span data-ttu-id="937cc-154">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="937cc-154">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="937cc-155">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="937cc-155">-TemplateParameterFile</span></span>
<span data-ttu-id="937cc-156">Указывает полный путь к JSON-файлу, который содержит имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="937cc-156">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="937cc-157">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="937cc-157">-TemplateParameterObject</span></span>
<span data-ttu-id="937cc-158">Указывает таблицу с именами и значениями параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="937cc-158">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="937cc-159">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="937cc-159">-TemplateParameterUri</span></span>
<span data-ttu-id="937cc-160">Определяет URI файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="937cc-160">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="937cc-161">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="937cc-161">-TemplateSpecId</span></span>
<span data-ttu-id="937cc-162">ИД ресурса шаблонаSpec, который нужно развернуть.</span><span class="sxs-lookup"><span data-stu-id="937cc-162">Resource ID of the templateSpec to be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateSpecResourceIdAndParams, ByTemplateSpecResourceIdAndParamsUri, ByTemplateSpecResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="937cc-163">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="937cc-163">-TemplateUri</span></span>
<span data-ttu-id="937cc-164">Определяет URI файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="937cc-164">Specifies the URI of a template file.</span></span>

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

### <span data-ttu-id="937cc-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937cc-165">CommonParameters</span></span>
<span data-ttu-id="937cc-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="937cc-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937cc-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="937cc-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937cc-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="937cc-168">INPUTS</span></span>

### <span data-ttu-id="937cc-169">System.String</span><span class="sxs-lookup"><span data-stu-id="937cc-169">System.String</span></span>

### <span data-ttu-id="937cc-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="937cc-170">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="937cc-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="937cc-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="937cc-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="937cc-172">OUTPUTS</span></span>

### <span data-ttu-id="937cc-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="937cc-173">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="937cc-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="937cc-174">NOTES</span></span>

## <span data-ttu-id="937cc-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="937cc-175">RELATED LINKS</span></span>

[<span data-ttu-id="937cc-176">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="937cc-176">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="937cc-177">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="937cc-177">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="937cc-178">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="937cc-178">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="937cc-179">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="937cc-179">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


