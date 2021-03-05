---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5c440c6f150993b947a0db2162ef0fd664e73220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960104"
---
# <span data-ttu-id="3d7fc-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="3d7fc-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="3d7fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="3d7fc-103">Проверяет развертывание в области клиента.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="3d7fc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3d7fc-104">SYNTAX</span></span>

### <span data-ttu-id="3d7fc-105">ByTemplateFileWithNoParameters (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d7fc-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d7fc-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d7fc-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d7fc-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3d7fc-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3d7fc-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="3d7fc-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-112">ByTemplateSpecResourceIdAndParams</span><span class="sxs-lookup"><span data-stu-id="3d7fc-112">ByTemplateSpecResourceIdAndParams</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterFile <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-113">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3d7fc-113">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-114">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3d7fc-114">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-115">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="3d7fc-115">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-116">ByTemplateSpecResourceIdAndParamsUri</span><span class="sxs-lookup"><span data-stu-id="3d7fc-116">ByTemplateSpecResourceIdAndParamsUri</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateParameterUri <String>
 -TemplateSpecId <String> [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-117">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3d7fc-117">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-118">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="3d7fc-118">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d7fc-119">ByTemplateSpecResourceId</span><span class="sxs-lookup"><span data-stu-id="3d7fc-119">ByTemplateSpecResourceId</span></span>
```
Test-AzTenantDeployment -Location <String> [-QueryString <String>] -TemplateSpecId <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d7fc-120">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d7fc-120">DESCRIPTION</span></span>
<span data-ttu-id="3d7fc-121">Для определения текущей области клиента шаблон развертывания и его значения параметров определяется **cmdlet Test-AzTenantDeployment.**</span><span class="sxs-lookup"><span data-stu-id="3d7fc-121">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="3d7fc-122">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3d7fc-122">EXAMPLES</span></span>

### <span data-ttu-id="3d7fc-123">Пример 1. Тестирование развертывания с использованием настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="3d7fc-123">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="3d7fc-124">Эта команда проверяет развертывание в текущей области клиента, используя файл шаблона и файл параметров.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-124">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="3d7fc-125">Пример 2. Тестирование развертывания с использованием настраиваемого объекта шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="3d7fc-125">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="3d7fc-126">Эта команда проверяет развертывание в текущей области клиента с использованием в памяти файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-126">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="3d7fc-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d7fc-127">PARAMETERS</span></span>

### <span data-ttu-id="3d7fc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d7fc-128">-DefaultProfile</span></span>
<span data-ttu-id="3d7fc-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d7fc-130">-Location</span><span class="sxs-lookup"><span data-stu-id="3d7fc-130">-Location</span></span>
<span data-ttu-id="3d7fc-131">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="3d7fc-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="3d7fc-132">-Pre</span></span>
<span data-ttu-id="3d7fc-133">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3d7fc-134">-QueryString</span><span class="sxs-lookup"><span data-stu-id="3d7fc-134">-QueryString</span></span>
<span data-ttu-id="3d7fc-135">Строка запроса (например, токен SAS), которая будет использоваться с параметром TemplateUri.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-135">The query string (for example, a SAS token) to be used with the TemplateUri parameter.</span></span> <span data-ttu-id="3d7fc-136">Будет использоваться в случае связанных шаблонов</span><span class="sxs-lookup"><span data-stu-id="3d7fc-136">Would be used in case of linked templates</span></span>

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

### <span data-ttu-id="3d7fc-137">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="3d7fc-137">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="3d7fc-138">Пропускает обработку динамических параметров PowerShell, которая проверяет, содержит ли предоставленный параметр шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-138">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="3d7fc-139">При проверке пользователю будет предложено в качестве значения пропустить отсутствующие параметры, но при этом параметр -SkipTemplateParameterPrompt сразу же проигнорирует этот запрос и выпустит ошибку, если параметр не был привязан к шаблону.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-139">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="3d7fc-140">Для неинтерационных сценариев можно предоставить функцию SkipTemplateParameterPrompt, чтобы улучшить сообщение об ошибке в случае, если удовлетворены не все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-140">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="3d7fc-141">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3d7fc-141">-TemplateFile</span></span>
<span data-ttu-id="3d7fc-142">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-142">Local path to the template file.</span></span> <span data-ttu-id="3d7fc-143">Поддерживаемый тип файла шаблона: json и bicep.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-143">Supported template file type: json and bicep.</span></span>

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

### <span data-ttu-id="3d7fc-144">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="3d7fc-144">-TemplateObject</span></span>
<span data-ttu-id="3d7fc-145">Hash table which represents the template.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-145">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="3d7fc-146">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3d7fc-146">-TemplateParameterFile</span></span>
<span data-ttu-id="3d7fc-147">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-147">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="3d7fc-148">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="3d7fc-148">-TemplateParameterObject</span></span>
<span data-ttu-id="3d7fc-149">Hash table which represents the parameters.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-149">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="3d7fc-150">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="3d7fc-150">-TemplateParameterUri</span></span>
<span data-ttu-id="3d7fc-151">Uri файла параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-151">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="3d7fc-152">-TemplateSpecId</span><span class="sxs-lookup"><span data-stu-id="3d7fc-152">-TemplateSpecId</span></span>
<span data-ttu-id="3d7fc-153">ИД ресурса шаблонаSpec, который нужно развернуть.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-153">Resource ID of the templateSpec to be deployed.</span></span>

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

### <span data-ttu-id="3d7fc-154">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3d7fc-154">-TemplateUri</span></span>
<span data-ttu-id="3d7fc-155">Uri файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-155">Uri to the template file.</span></span>

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

### <span data-ttu-id="3d7fc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d7fc-156">CommonParameters</span></span>
<span data-ttu-id="3d7fc-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d7fc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d7fc-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d7fc-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d7fc-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d7fc-159">INPUTS</span></span>

### <span data-ttu-id="3d7fc-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d7fc-160">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3d7fc-161">System.String</span><span class="sxs-lookup"><span data-stu-id="3d7fc-161">System.String</span></span>

## <span data-ttu-id="3d7fc-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d7fc-162">OUTPUTS</span></span>

### <span data-ttu-id="3d7fc-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="3d7fc-163">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="3d7fc-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3d7fc-164">NOTES</span></span>

## <span data-ttu-id="3d7fc-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d7fc-165">RELATED LINKS</span></span>
