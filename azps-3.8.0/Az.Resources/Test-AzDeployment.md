---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: d6222c0e1ecd6eee39b65ac65e74707d1d64ef17
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066176"
---
# <span data-ttu-id="83103-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="83103-101">Test-AzDeployment</span></span>

## <span data-ttu-id="83103-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83103-102">SYNOPSIS</span></span>
<span data-ttu-id="83103-103">Проверка развертывания.</span><span class="sxs-lookup"><span data-stu-id="83103-103">Validates a deployment.</span></span>

## <span data-ttu-id="83103-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83103-104">SYNTAX</span></span>

### <span data-ttu-id="83103-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83103-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83103-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="83103-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83103-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="83103-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83103-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="83103-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83103-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="83103-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83103-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="83103-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83103-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="83103-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83103-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="83103-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83103-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="83103-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83103-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="83103-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83103-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="83103-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83103-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="83103-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83103-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83103-117">DESCRIPTION</span></span>
<span data-ttu-id="83103-118">Командлет **Test-AzDeployment** определяет, являются ли шаблон развертывания и значения его параметров допустимыми.</span><span class="sxs-lookup"><span data-stu-id="83103-118">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="83103-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83103-119">EXAMPLES</span></span>

### <span data-ttu-id="83103-120">Пример 1: Проверка развертывания с помощью настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="83103-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="83103-121">Эта команда проверяет развертывание в текущей области подписки с помощью заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="83103-121">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="83103-122">Пример 2: Проверка развертывания с помощью настраиваемого объекта шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="83103-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\EngineeringSite.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="83103-123">Эта команда проверяет развертывание в текущей области подписки с помощью хэш-таблицы в памяти, созданной из заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="83103-123">This command tests a deployment at the current subscription scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="83103-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83103-124">PARAMETERS</span></span>

### <span data-ttu-id="83103-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="83103-125">-ApiVersion</span></span>
<span data-ttu-id="83103-126">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83103-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="83103-127">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="83103-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="83103-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83103-128">-DefaultProfile</span></span>
<span data-ttu-id="83103-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83103-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83103-130">-Location</span><span class="sxs-lookup"><span data-stu-id="83103-130">-Location</span></span>
<span data-ttu-id="83103-131">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="83103-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="83103-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="83103-132">-Pre</span></span>
<span data-ttu-id="83103-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="83103-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="83103-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="83103-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="83103-135">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="83103-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span> <span data-ttu-id="83103-136">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="83103-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span> <span data-ttu-id="83103-137">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="83103-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="83103-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="83103-138">-TemplateFile</span></span>
<span data-ttu-id="83103-139">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="83103-139">Local path to the template file.</span></span>

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

### <span data-ttu-id="83103-140">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="83103-140">-TemplateObject</span></span>
<span data-ttu-id="83103-141">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="83103-141">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="83103-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="83103-142">-TemplateParameterFile</span></span>
<span data-ttu-id="83103-143">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="83103-143">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="83103-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="83103-144">-TemplateParameterObject</span></span>
<span data-ttu-id="83103-145">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="83103-145">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="83103-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="83103-146">-TemplateParameterUri</span></span>
<span data-ttu-id="83103-147">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="83103-147">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="83103-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="83103-148">-TemplateUri</span></span>
<span data-ttu-id="83103-149">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="83103-149">Uri to the template file.</span></span>

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

### <span data-ttu-id="83103-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83103-150">CommonParameters</span></span>
<span data-ttu-id="83103-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83103-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83103-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83103-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83103-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83103-153">INPUTS</span></span>

### <span data-ttu-id="83103-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="83103-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="83103-155">System. String</span><span class="sxs-lookup"><span data-stu-id="83103-155">System.String</span></span>

## <span data-ttu-id="83103-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83103-156">OUTPUTS</span></span>

### <span data-ttu-id="83103-157">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="83103-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="83103-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="83103-158">NOTES</span></span>

## <span data-ttu-id="83103-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83103-159">RELATED LINKS</span></span>
