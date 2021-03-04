---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 5a7bb411c5b2881361c1f9dfe7e675450f76e318
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962643"
---
# <span data-ttu-id="e3656-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="e3656-101">Test-AzDeployment</span></span>

## <span data-ttu-id="e3656-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3656-102">SYNOPSIS</span></span>
<span data-ttu-id="e3656-103">Проверяет развертывание.</span><span class="sxs-lookup"><span data-stu-id="e3656-103">Validates a deployment.</span></span>

## <span data-ttu-id="e3656-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e3656-104">SYNTAX</span></span>

### <span data-ttu-id="e3656-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3656-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3656-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3656-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3656-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3656-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3656-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3656-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3656-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="e3656-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e3656-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e3656-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="e3656-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="e3656-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3656-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e3656-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3656-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="e3656-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3656-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="e3656-119">ByTemplateSpecResourceId</span></span>
```
Test-AzDeployment -Location <String> [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3656-120">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3656-120">DESCRIPTION</span></span>
<span data-ttu-id="e3656-121">С **его использованием** можно определить, допустим ли шаблон развертывания и его значения параметров.</span><span class="sxs-lookup"><span data-stu-id="e3656-121">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="e3656-122">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e3656-122">EXAMPLES</span></span>

### <span data-ttu-id="e3656-123">Пример 1. Тестирование развертывания с использованием настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="e3656-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="e3656-124">Эта команда проверяет развертывание в текущей области подписки, используя файл шаблона и файл параметров.</span><span class="sxs-lookup"><span data-stu-id="e3656-124">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="e3656-125">Пример 2. Тестовая развертывание с объектом настраиваемого шаблона и файлом параметров</span><span class="sxs-lookup"><span data-stu-id="e3656-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="e3656-126">Эта команда проверяет развертывание в текущей области подписки с использованием в памяти файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="e3656-126">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="e3656-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3656-127">PARAMETERS</span></span>

### <span data-ttu-id="e3656-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3656-128">-DefaultProfile</span></span>
<span data-ttu-id="e3656-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3656-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3656-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e3656-130">-Location</span></span>
<span data-ttu-id="e3656-131">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="e3656-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="e3656-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="e3656-132">-Pre</span></span>
<span data-ttu-id="e3656-133">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="e3656-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e3656-134">-QueryString</span><span class="sxs-lookup"><span data-stu-id="e3656-134">-QueryString</span></span>
<span data-ttu-id="e3656-135">Строка запроса (например, токен SAS), которая будет использоваться с параметром TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="e3656-135">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="e3656-136">Будет использоваться в случае связанных шаблонов</span><span class="sxs-lookup"><span data-stu-id="e3656-136">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="e3656-137">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="e3656-137">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="e3656-138">Пропускает динамическую обработку параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="e3656-138">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="e3656-139">При этой проверке пользователю будет предложено укастереть отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не будет привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="e3656-139">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="e3656-140">Для неинтерационных сценариев можно предоставить функцию SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="e3656-140">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="e3656-141">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e3656-141">-TemplateFile</span></span>
<span data-ttu-id="e3656-142">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3656-142">Local path to the template file.</span></span> <span data-ttu-id="e3656-143">Поддерживаемый тип файла шаблона: json и bicep.</span><span class="sxs-lookup"><span data-stu-id="e3656-143">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="e3656-144">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="e3656-144">-TemplateObject</span></span>
<span data-ttu-id="e3656-145">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="e3656-145">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="e3656-146">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="e3656-146">-TemplateParameterFile</span></span>
<span data-ttu-id="e3656-147">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3656-147">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="e3656-148">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="e3656-148">-TemplateParameterObject</span></span>
<span data-ttu-id="e3656-149">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="e3656-149">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="e3656-150">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="e3656-150">-TemplateParameterUri</span></span>
<span data-ttu-id="e3656-151">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3656-151">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="e3656-152">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="e3656-152">-TemplateSpecId</span></span>
<span data-ttu-id="e3656-153">ИД ресурса шаблонаSpec, который нужно развернуть.</span><span class="sxs-lookup"><span data-stu-id="e3656-153">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="e3656-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="e3656-154">-TemplateUri</span></span>
<span data-ttu-id="e3656-155">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="e3656-155">Uri to the template file.</span></span>

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

### <span data-ttu-id="e3656-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3656-156">CommonParameters</span></span>
<span data-ttu-id="e3656-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3656-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3656-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3656-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3656-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3656-159">INPUTS</span></span>

### <span data-ttu-id="e3656-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3656-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e3656-161">System.String</span><span class="sxs-lookup"><span data-stu-id="e3656-161">System.String</span></span>

## <span data-ttu-id="e3656-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3656-162">OUTPUTS</span></span>

### <span data-ttu-id="e3656-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="e3656-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="e3656-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e3656-164">NOTES</span></span>

## <span data-ttu-id="e3656-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3656-165">RELATED LINKS</span></span>
