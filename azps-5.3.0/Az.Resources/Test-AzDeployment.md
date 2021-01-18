---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 9a1a183ac6a0fb896f6b3d901e8f429fdf225e26
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505150"
---
# <span data-ttu-id="744d4-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="744d4-101">Test-AzDeployment</span></span>

## <span data-ttu-id="744d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="744d4-102">SYNOPSIS</span></span>
<span data-ttu-id="744d4-103">Проверяет развертывание.</span><span class="sxs-lookup"><span data-stu-id="744d4-103">Validates a deployment.</span></span>

## <span data-ttu-id="744d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="744d4-104">SYNTAX</span></span>

### <span data-ttu-id="744d4-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="744d4-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="744d4-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="744d4-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="744d4-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="744d4-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="744d4-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="744d4-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="744d4-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="744d4-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="744d4-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="744d4-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="744d4-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="744d4-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="744d4-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="744d4-117">DESCRIPTION</span></span>
<span data-ttu-id="744d4-118">Параметр **Test-AzDeployment** определяет, допустим ли шаблон развертывания и его значения параметров.</span><span class="sxs-lookup"><span data-stu-id="744d4-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="744d4-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="744d4-119">EXAMPLES</span></span>

### <span data-ttu-id="744d4-120">Пример 1. Тестирование развертывания с использованием настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="744d4-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="744d4-121">Эта команда проверяет развертывание в текущей области подписки, используя файл шаблона и файл параметров.</span><span class="sxs-lookup"><span data-stu-id="744d4-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="744d4-122">Пример 2. Тестирование развертывания с использованием настраиваемого объекта шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="744d4-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="744d4-123">Эта команда проверяет развертывание в текущей области подписки, используя в памяти файл, созданный из данного файла шаблона, и файл с параметрами.</span><span class="sxs-lookup"><span data-stu-id="744d4-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="744d4-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="744d4-124">PARAMETERS</span></span>

### <span data-ttu-id="744d4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744d4-125">-DefaultProfile</span></span>
<span data-ttu-id="744d4-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="744d4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="744d4-127">-Location</span><span class="sxs-lookup"><span data-stu-id="744d4-127">-Location</span></span>
<span data-ttu-id="744d4-128">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="744d4-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="744d4-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="744d4-129">-Pre</span></span>
<span data-ttu-id="744d4-130">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="744d4-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="744d4-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="744d4-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="744d4-132">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="744d4-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="744d4-133">При проверке пользователю будет предложено в качестве значения пропустить отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не был привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="744d4-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="744d4-134">Для неинтерационных сценариев можно предоставить функцию SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="744d4-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="744d4-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="744d4-135">-TemplateFile</span></span>
<span data-ttu-id="744d4-136">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="744d4-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="744d4-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="744d4-137">-TemplateObject</span></span>
<span data-ttu-id="744d4-138">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="744d4-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="744d4-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="744d4-139">-TemplateParameterFile</span></span>
<span data-ttu-id="744d4-140">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="744d4-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="744d4-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="744d4-141">-TemplateParameterObject</span></span>
<span data-ttu-id="744d4-142">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="744d4-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="744d4-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="744d4-143">-TemplateParameterUri</span></span>
<span data-ttu-id="744d4-144">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="744d4-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="744d4-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="744d4-145">-TemplateUri</span></span>
<span data-ttu-id="744d4-146">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="744d4-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="744d4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744d4-147">CommonParameters</span></span>
<span data-ttu-id="744d4-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="744d4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744d4-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="744d4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744d4-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="744d4-150">INPUTS</span></span>

### <span data-ttu-id="744d4-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="744d4-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="744d4-152">System.String</span><span class="sxs-lookup"><span data-stu-id="744d4-152">System.String</span></span>

## <span data-ttu-id="744d4-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="744d4-153">OUTPUTS</span></span>

### <span data-ttu-id="744d4-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="744d4-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="744d4-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="744d4-155">NOTES</span></span>

## <span data-ttu-id="744d4-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="744d4-156">RELATED LINKS</span></span>
