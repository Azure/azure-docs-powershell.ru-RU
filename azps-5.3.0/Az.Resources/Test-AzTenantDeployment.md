---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5144dacb044523c2ad72d0a9c24aa43427f14f99
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507646"
---
# <span data-ttu-id="51b77-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="51b77-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="51b77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51b77-102">SYNOPSIS</span></span>
<span data-ttu-id="51b77-103">Проверяет развертывание в области клиента.</span><span class="sxs-lookup"><span data-stu-id="51b77-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="51b77-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="51b77-104">SYNTAX</span></span>

### <span data-ttu-id="51b77-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51b77-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="51b77-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="51b77-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="51b77-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="51b77-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="51b77-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="51b77-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="51b77-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="51b77-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="51b77-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="51b77-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51b77-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="51b77-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51b77-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51b77-117">DESCRIPTION</span></span>
<span data-ttu-id="51b77-118">Для определения текущей области клиента шаблон развертывания и его значения параметров определяется **cmdlet Test-AzTenantDeployment.**</span><span class="sxs-lookup"><span data-stu-id="51b77-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="51b77-119">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="51b77-119">EXAMPLES</span></span>

### <span data-ttu-id="51b77-120">Пример 1. Тестирование развертывания с использованием настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="51b77-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="51b77-121">Эта команда проверяет развертывание в текущей области клиента, используя файл шаблона и файл параметров.</span><span class="sxs-lookup"><span data-stu-id="51b77-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="51b77-122">Пример 2. Тестовая развертывание с объектом настраиваемого шаблона и файлом параметров</span><span class="sxs-lookup"><span data-stu-id="51b77-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="51b77-123">Эта команда проверяет развертывание в текущей области клиента с использованием в памяти файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="51b77-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="51b77-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51b77-124">PARAMETERS</span></span>

### <span data-ttu-id="51b77-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b77-125">-DefaultProfile</span></span>
<span data-ttu-id="51b77-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51b77-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51b77-127">-Location</span><span class="sxs-lookup"><span data-stu-id="51b77-127">-Location</span></span>
<span data-ttu-id="51b77-128">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="51b77-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="51b77-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="51b77-129">-Pre</span></span>
<span data-ttu-id="51b77-130">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="51b77-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="51b77-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="51b77-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="51b77-132">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="51b77-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="51b77-133">При проверке пользователю будет предложено в качестве значения пропустить отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не был привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="51b77-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="51b77-134">Для неинтерационных сценариев можно использовать параметр SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="51b77-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="51b77-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="51b77-135">-TemplateFile</span></span>
<span data-ttu-id="51b77-136">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="51b77-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="51b77-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="51b77-137">-TemplateObject</span></span>
<span data-ttu-id="51b77-138">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="51b77-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="51b77-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="51b77-139">-TemplateParameterFile</span></span>
<span data-ttu-id="51b77-140">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="51b77-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="51b77-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="51b77-141">-TemplateParameterObject</span></span>
<span data-ttu-id="51b77-142">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="51b77-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="51b77-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="51b77-143">-TemplateParameterUri</span></span>
<span data-ttu-id="51b77-144">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="51b77-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="51b77-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="51b77-145">-TemplateUri</span></span>
<span data-ttu-id="51b77-146">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="51b77-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="51b77-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b77-147">CommonParameters</span></span>
<span data-ttu-id="51b77-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51b77-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b77-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51b77-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b77-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51b77-150">INPUTS</span></span>

### <span data-ttu-id="51b77-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="51b77-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="51b77-152">System.String</span><span class="sxs-lookup"><span data-stu-id="51b77-152">System.String</span></span>

## <span data-ttu-id="51b77-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="51b77-153">OUTPUTS</span></span>

### <span data-ttu-id="51b77-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="51b77-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="51b77-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="51b77-155">NOTES</span></span>

## <span data-ttu-id="51b77-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51b77-156">RELATED LINKS</span></span>
