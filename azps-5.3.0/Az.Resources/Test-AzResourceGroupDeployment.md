---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505149"
---
# <span data-ttu-id="87cbd-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="87cbd-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="87cbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="87cbd-103">Проверка развертывания группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87cbd-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="87cbd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87cbd-104">SYNTAX</span></span>

### <span data-ttu-id="87cbd-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87cbd-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="87cbd-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="87cbd-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="87cbd-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="87cbd-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="87cbd-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="87cbd-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="87cbd-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="87cbd-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="87cbd-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="87cbd-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cbd-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="87cbd-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87cbd-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87cbd-117">DESCRIPTION</span></span>
<span data-ttu-id="87cbd-118">С **его** использованием можно определить, допустим ли шаблон развертывания группы ресурсов Azure и его значения параметров.</span><span class="sxs-lookup"><span data-stu-id="87cbd-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="87cbd-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87cbd-119">EXAMPLES</span></span>

### <span data-ttu-id="87cbd-120">Пример 1. Тестовая развертывание с объектом настраиваемого шаблона и файлом параметров</span><span class="sxs-lookup"><span data-stu-id="87cbd-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="87cbd-121">Эта команда проверяет развертывание в заданной группе ресурсов с использованием в памяти файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="87cbd-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="87cbd-122">Пример 2. Тестирование развертывания с помощью файла шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="87cbd-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="87cbd-123">Эта команда проверяет развертывание в заданной группе ресурсов и ресурса, используя предоставленный файл шаблона и файл параметров.</span><span class="sxs-lookup"><span data-stu-id="87cbd-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="87cbd-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87cbd-124">PARAMETERS</span></span>

### <span data-ttu-id="87cbd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87cbd-125">-DefaultProfile</span></span>
<span data-ttu-id="87cbd-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="87cbd-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87cbd-127">-Mode</span><span class="sxs-lookup"><span data-stu-id="87cbd-127">-Mode</span></span>
<span data-ttu-id="87cbd-128">Режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="87cbd-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="87cbd-129">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="87cbd-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="87cbd-130">Приращение</span><span class="sxs-lookup"><span data-stu-id="87cbd-130">Incremental</span></span>
- <span data-ttu-id="87cbd-131">Завершено</span><span class="sxs-lookup"><span data-stu-id="87cbd-131">Complete</span></span>

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

### <span data-ttu-id="87cbd-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="87cbd-132">-Pre</span></span>
<span data-ttu-id="87cbd-133">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="87cbd-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="87cbd-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87cbd-134">-ResourceGroupName</span></span>
<span data-ttu-id="87cbd-135">Указывает имя группы ресурсов, которая будет протестирована.</span><span class="sxs-lookup"><span data-stu-id="87cbd-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="87cbd-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="87cbd-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="87cbd-137">Откат до успешного развертывания с заданным именем в группе ресурсов не следует использовать, если используется -RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="87cbd-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="87cbd-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="87cbd-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="87cbd-139">При этом не должно быть отката до последнего успешного развертывания в группе ресурсов, если используется -RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="87cbd-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="87cbd-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="87cbd-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="87cbd-141">Пропускает динамическую обработку параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="87cbd-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="87cbd-142">При проверке пользователю будет предложено в качестве значения пропустить отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не был привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="87cbd-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="87cbd-143">Для неинтерационных сценариев можно предоставить функцию SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="87cbd-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="87cbd-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="87cbd-144">-TemplateFile</span></span>
<span data-ttu-id="87cbd-145">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="87cbd-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="87cbd-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="87cbd-146">-TemplateObject</span></span>
<span data-ttu-id="87cbd-147">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="87cbd-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="87cbd-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="87cbd-148">-TemplateParameterFile</span></span>
<span data-ttu-id="87cbd-149">Указывает полный путь к JSON-файлу, который содержит имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="87cbd-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="87cbd-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="87cbd-150">-TemplateParameterObject</span></span>
<span data-ttu-id="87cbd-151">Указывает таблицу с именами и значениями параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="87cbd-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="87cbd-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="87cbd-152">-TemplateParameterUri</span></span>
<span data-ttu-id="87cbd-153">Определяет URI файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="87cbd-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="87cbd-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="87cbd-154">-TemplateUri</span></span>
<span data-ttu-id="87cbd-155">Определяет URI файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="87cbd-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="87cbd-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87cbd-156">CommonParameters</span></span>
<span data-ttu-id="87cbd-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87cbd-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87cbd-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87cbd-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87cbd-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87cbd-159">INPUTS</span></span>

### <span data-ttu-id="87cbd-160">System.String</span><span class="sxs-lookup"><span data-stu-id="87cbd-160">System.String</span></span>

### <span data-ttu-id="87cbd-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="87cbd-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="87cbd-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="87cbd-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87cbd-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87cbd-163">OUTPUTS</span></span>

### <span data-ttu-id="87cbd-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="87cbd-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="87cbd-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87cbd-165">NOTES</span></span>

## <span data-ttu-id="87cbd-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87cbd-166">RELATED LINKS</span></span>

[<span data-ttu-id="87cbd-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="87cbd-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="87cbd-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="87cbd-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="87cbd-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="87cbd-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="87cbd-170">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="87cbd-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


