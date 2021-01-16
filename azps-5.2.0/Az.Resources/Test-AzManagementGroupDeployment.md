---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 4f4aa6972c8152e3340a9cc938df9cfa8b585dbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414972"
---
# <span data-ttu-id="f57bf-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f57bf-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="f57bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f57bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f57bf-103">Проверка развертывания в группе управления.</span><span class="sxs-lookup"><span data-stu-id="f57bf-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="f57bf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f57bf-104">SYNTAX</span></span>

### <span data-ttu-id="f57bf-105">ByTemplateFileWithNoParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="f57bf-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f57bf-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f57bf-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f57bf-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f57bf-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f57bf-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f57bf-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f57bf-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f57bf-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f57bf-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f57bf-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f57bf-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f57bf-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f57bf-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f57bf-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f57bf-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f57bf-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f57bf-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f57bf-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f57bf-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f57bf-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f57bf-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f57bf-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f57bf-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f57bf-117">DESCRIPTION</span></span>
<span data-ttu-id="f57bf-118">Для **группировки управления test-AzManagementGroupDeployment** определяется, допустим ли шаблон развертывания и его значения параметров.</span><span class="sxs-lookup"><span data-stu-id="f57bf-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="f57bf-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f57bf-119">EXAMPLES</span></span>

### <span data-ttu-id="f57bf-120">Пример 1. Тестирование развертывания с использованием настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="f57bf-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="f57bf-121">Эта команда проверяет развертывание в группе управления MyMG, используя файл шаблона и файл параметров.</span><span class="sxs-lookup"><span data-stu-id="f57bf-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="f57bf-122">Пример 2. Тестовая развертывание с объектом настраиваемого шаблона и файлом параметров</span><span class="sxs-lookup"><span data-stu-id="f57bf-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="f57bf-123">Эта команда проверяет развертывание в группе управления MyMG с использованием в памяти файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="f57bf-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="f57bf-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f57bf-124">PARAMETERS</span></span>

### <span data-ttu-id="f57bf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f57bf-125">-DefaultProfile</span></span>
<span data-ttu-id="f57bf-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f57bf-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f57bf-127">-Location</span><span class="sxs-lookup"><span data-stu-id="f57bf-127">-Location</span></span>
<span data-ttu-id="f57bf-128">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="f57bf-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="f57bf-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f57bf-129">-ManagementGroupId</span></span>
<span data-ttu-id="f57bf-130">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="f57bf-130">The management group id.</span></span>

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

### <span data-ttu-id="f57bf-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="f57bf-131">-Pre</span></span>
<span data-ttu-id="f57bf-132">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="f57bf-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f57bf-133">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="f57bf-133">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="f57bf-134">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="f57bf-134">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="f57bf-135">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="f57bf-135">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="f57bf-136">Для неинтерационных сценариев можно предоставить функцию SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="f57bf-136">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="f57bf-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f57bf-137">-TemplateFile</span></span>
<span data-ttu-id="f57bf-138">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="f57bf-138">Local path to the template file.</span></span>

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

### <span data-ttu-id="f57bf-139">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="f57bf-139">-TemplateObject</span></span>
<span data-ttu-id="f57bf-140">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="f57bf-140">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="f57bf-141">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f57bf-141">-TemplateParameterFile</span></span>
<span data-ttu-id="f57bf-142">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="f57bf-142">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="f57bf-143">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f57bf-143">-TemplateParameterObject</span></span>
<span data-ttu-id="f57bf-144">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="f57bf-144">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="f57bf-145">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f57bf-145">-TemplateParameterUri</span></span>
<span data-ttu-id="f57bf-146">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="f57bf-146">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="f57bf-147">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f57bf-147">-TemplateUri</span></span>
<span data-ttu-id="f57bf-148">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="f57bf-148">Uri to the template file.</span></span>

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

### <span data-ttu-id="f57bf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57bf-149">CommonParameters</span></span>
<span data-ttu-id="f57bf-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f57bf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57bf-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f57bf-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57bf-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f57bf-152">INPUTS</span></span>

### <span data-ttu-id="f57bf-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f57bf-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f57bf-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f57bf-154">System.String</span></span>

## <span data-ttu-id="f57bf-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f57bf-155">OUTPUTS</span></span>

### <span data-ttu-id="f57bf-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="f57bf-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="f57bf-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f57bf-157">NOTES</span></span>

## <span data-ttu-id="f57bf-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f57bf-158">RELATED LINKS</span></span>