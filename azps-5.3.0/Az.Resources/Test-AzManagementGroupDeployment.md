---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506695"
---
# <span data-ttu-id="db11d-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="db11d-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="db11d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db11d-102">SYNOPSIS</span></span>
<span data-ttu-id="db11d-103">Проверка развертывания в группе управления.</span><span class="sxs-lookup"><span data-stu-id="db11d-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="db11d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db11d-104">SYNTAX</span></span>

### <span data-ttu-id="db11d-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db11d-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db11d-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="db11d-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db11d-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="db11d-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db11d-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="db11d-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db11d-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="db11d-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db11d-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="db11d-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db11d-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="db11d-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db11d-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="db11d-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db11d-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="db11d-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db11d-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="db11d-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db11d-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="db11d-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db11d-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="db11d-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db11d-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db11d-117">DESCRIPTION</span></span>
<span data-ttu-id="db11d-118">Для **группировки управления тест-azManagementGroupDeployment** определяет, допустим ли шаблон развертывания и его значения параметров.</span><span class="sxs-lookup"><span data-stu-id="db11d-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="db11d-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db11d-119">EXAMPLES</span></span>

### <span data-ttu-id="db11d-120">Пример 1. Тестирование развертывания с использованием настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="db11d-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="db11d-121">Эта команда проверяет развертывание в группе управления MyMG, используя файл шаблона и файл параметров.</span><span class="sxs-lookup"><span data-stu-id="db11d-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="db11d-122">Пример 2. Тестирование развертывания с использованием настраиваемого объекта шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="db11d-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="db11d-123">Эта команда проверяет развертывание в группе управления MyMG с использованием в памяти файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="db11d-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="db11d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db11d-124">PARAMETERS</span></span>

### <span data-ttu-id="db11d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db11d-125">-DefaultProfile</span></span>
<span data-ttu-id="db11d-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db11d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db11d-127">-Location</span><span class="sxs-lookup"><span data-stu-id="db11d-127">-Location</span></span>
<span data-ttu-id="db11d-128">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="db11d-128">The location to store deployment data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db11d-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="db11d-129">-ManagementGroupId</span></span>
<span data-ttu-id="db11d-130">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="db11d-130">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db11d-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="db11d-131">-Pre</span></span>
<span data-ttu-id="db11d-132">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="db11d-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="db11d-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="db11d-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="db11d-134">Пропускает динамическую обработку параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="db11d-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="db11d-135">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="db11d-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="db11d-136">Для неинтерационных сценариев можно предоставить функцию SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="db11d-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="db11d-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="db11d-137">-TemplateFile</span></span>
<span data-ttu-id="db11d-138">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="db11d-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="db11d-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="db11d-139">-TemplateObject</span></span>
<span data-ttu-id="db11d-140">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="db11d-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="db11d-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="db11d-141">-TemplateParameterFile</span></span>
<span data-ttu-id="db11d-142">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="db11d-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="db11d-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="db11d-143">-TemplateParameterObject</span></span>
<span data-ttu-id="db11d-144">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="db11d-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="db11d-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="db11d-145">-TemplateParameterUri</span></span>
<span data-ttu-id="db11d-146">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="db11d-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="db11d-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="db11d-147">-TemplateUri</span></span>
<span data-ttu-id="db11d-148">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="db11d-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="db11d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db11d-149">CommonParameters</span></span>
<span data-ttu-id="db11d-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db11d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db11d-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db11d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db11d-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db11d-152">INPUTS</span></span>

### <span data-ttu-id="db11d-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="db11d-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="db11d-154">System.String</span><span class="sxs-lookup"><span data-stu-id="db11d-154">System.String</span></span>

## <span data-ttu-id="db11d-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db11d-155">OUTPUTS</span></span>

### <span data-ttu-id="db11d-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="db11d-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="db11d-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db11d-157">NOTES</span></span>

## <span data-ttu-id="db11d-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db11d-158">RELATED LINKS</span></span>
