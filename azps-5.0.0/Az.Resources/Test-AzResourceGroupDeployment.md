---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzResourceGroupDeployment.md
ms.openlocfilehash: 5ee86c91b1dc1354b078b727e3bc9ebfe5a43bfe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245879"
---
# <span data-ttu-id="f7ce6-101">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7ce6-101">Test-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="f7ce6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ce6-103">Проверяет развертывание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-103">Validates a resource group deployment.</span></span>

## <span data-ttu-id="f7ce6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7ce6-104">SYNTAX</span></span>

### <span data-ttu-id="f7ce6-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7ce6-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f7ce6-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f7ce6-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f7ce6-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f7ce6-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f7ce6-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f7ce6-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f7ce6-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f7ce6-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f7ce6-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f7ce6-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7ce6-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f7ce6-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] [-RollbackToLastDeployment]
 [-RollBackDeploymentName <String>] -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7ce6-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7ce6-117">DESCRIPTION</span></span>
<span data-ttu-id="f7ce6-118">Командлет **Test-AzResourceGroupDeployment** определяет, являются ли шаблон развертывания группы ресурсов Azure и значения его параметров допустимыми.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-118">The **Test-AzResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f7ce6-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7ce6-119">EXAMPLES</span></span>

### <span data-ttu-id="f7ce6-120">Пример 1: Проверка развертывания с помощью настраиваемого объекта шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="f7ce6-120">Example 1: Test deployment with a custom template object and parameter file</span></span>

```powershell
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName "ContosoEngineering" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="f7ce6-121">Эта команда проверяет развертывание в заданной группе ресурсов с помощью хэш-таблицы в памяти, созданной из заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-121">This command tests a deployment in the given resource group using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

### <span data-ttu-id="f7ce6-122">Пример 2: Проверка развертывания с помощью файла шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="f7ce6-122">Example 2: Test deployment via template file and parameter file</span></span>

```powershell
PS C:\> Test-AzResourceGroupDeployment -ResourceGroupName testRG01 -TemplateFile "D:\Azure\Templates\sampleDeploymentTemplate.json" -TemplateParameterFile "D:\Azure\Templates\sampleDeploymentTemplateParams.json"
```

<span data-ttu-id="f7ce6-123">Эта команда проверяет развертывание в заданной группе ресурсов и ресурс с помощью предоставленного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-123">This command tests a deployment in the given resource group and resource using the provided template file and a parameter file.</span></span>

## <span data-ttu-id="f7ce6-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7ce6-124">PARAMETERS</span></span>

### <span data-ttu-id="f7ce6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ce6-125">-DefaultProfile</span></span>
<span data-ttu-id="f7ce6-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7ce6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7ce6-127">Режим</span><span class="sxs-lookup"><span data-stu-id="f7ce6-127">-Mode</span></span>
<span data-ttu-id="f7ce6-128">Задает режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-128">Specifies the deployment mode.</span></span>
<span data-ttu-id="f7ce6-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f7ce6-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7ce6-130">Разност</span><span class="sxs-lookup"><span data-stu-id="f7ce6-130">Incremental</span></span>
- <span data-ttu-id="f7ce6-131">Полнот</span><span class="sxs-lookup"><span data-stu-id="f7ce6-131">Complete</span></span>

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

### <span data-ttu-id="f7ce6-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="f7ce6-132">-Pre</span></span>
<span data-ttu-id="f7ce6-133">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f7ce6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ce6-134">-ResourceGroupName</span></span>
<span data-ttu-id="f7ce6-135">Указывает имя тестируемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-135">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="f7ce6-136">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="f7ce6-136">-RollBackDeploymentName</span></span>
<span data-ttu-id="f7ce6-137">Откат к успешному развертыванию с указанным именем в группе ресурсов не следует использовать, если используется параметр-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-137">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

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

### <span data-ttu-id="f7ce6-138">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="f7ce6-138">-RollbackToLastDeployment</span></span>
<span data-ttu-id="f7ce6-139">Откат к последнему успешному развертыванию в группе ресурсов не отображается, если используется значение-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-139">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="f7ce6-140">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="f7ce6-140">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="f7ce6-141">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-141">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="f7ce6-142">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-142">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="f7ce6-143">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-143">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="f7ce6-144">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f7ce6-144">-TemplateFile</span></span>
<span data-ttu-id="f7ce6-145">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-145">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="f7ce6-146">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="f7ce6-146">-TemplateObject</span></span>
<span data-ttu-id="f7ce6-147">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-147">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="f7ce6-148">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f7ce6-148">-TemplateParameterFile</span></span>
<span data-ttu-id="f7ce6-149">Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-149">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="f7ce6-150">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f7ce6-150">-TemplateParameterObject</span></span>
<span data-ttu-id="f7ce6-151">Указывает хэш-таблицу имен и значений параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-151">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="f7ce6-152">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f7ce6-152">-TemplateParameterUri</span></span>
<span data-ttu-id="f7ce6-153">Задает универсальный код ресурса (URI) файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-153">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="f7ce6-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f7ce6-154">-TemplateUri</span></span>
<span data-ttu-id="f7ce6-155">Задает универсальный код ресурса (URI) для файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-155">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="f7ce6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ce6-156">CommonParameters</span></span>
<span data-ttu-id="f7ce6-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7ce6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ce6-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7ce6-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ce6-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7ce6-159">INPUTS</span></span>

### <span data-ttu-id="f7ce6-160">System. String</span><span class="sxs-lookup"><span data-stu-id="f7ce6-160">System.String</span></span>

### <span data-ttu-id="f7ce6-161">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="f7ce6-161">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode</span></span>

### <span data-ttu-id="f7ce6-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f7ce6-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f7ce6-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7ce6-163">OUTPUTS</span></span>

### <span data-ttu-id="f7ce6-164">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="f7ce6-164">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="f7ce6-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7ce6-165">NOTES</span></span>

## <span data-ttu-id="f7ce6-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7ce6-166">RELATED LINKS</span></span>

[<span data-ttu-id="f7ce6-167">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7ce6-167">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="f7ce6-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7ce6-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="f7ce6-169">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7ce6-169">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="f7ce6-170">Остановить-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f7ce6-170">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)


