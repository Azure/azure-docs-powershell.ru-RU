---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 60db8b7b544b63e29b4834676da946ebbf6c39c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236638"
---
# <span data-ttu-id="9be69-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="9be69-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="9be69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9be69-102">SYNOPSIS</span></span>
<span data-ttu-id="9be69-103">Проверяет развертывание в области клиента.</span><span class="sxs-lookup"><span data-stu-id="9be69-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="9be69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9be69-104">SYNTAX</span></span>

### <span data-ttu-id="9be69-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9be69-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be69-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9be69-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be69-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9be69-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be69-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="9be69-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be69-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9be69-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be69-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9be69-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be69-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="9be69-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be69-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9be69-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be69-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9be69-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be69-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="9be69-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9be69-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9be69-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9be69-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="9be69-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9be69-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9be69-117">DESCRIPTION</span></span>
<span data-ttu-id="9be69-118">Командлет **Test-AzTenantDeployment** определяет, является ли шаблон развертывания и значения его параметров допустимыми в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="9be69-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="9be69-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9be69-119">EXAMPLES</span></span>

### <span data-ttu-id="9be69-120">Пример 1: Проверка развертывания с помощью настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="9be69-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="9be69-121">Эта команда проверяет развертывание в текущей области клиента с помощью заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="9be69-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="9be69-122">Пример 2: Проверка развертывания с помощью настраиваемого объекта шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="9be69-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="9be69-123">Эта команда проверяет развертывание в текущей области клиента с помощью хэш-таблицы в памяти, созданной из заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="9be69-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="9be69-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9be69-124">PARAMETERS</span></span>

### <span data-ttu-id="9be69-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9be69-125">-ApiVersion</span></span>
<span data-ttu-id="9be69-126">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9be69-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9be69-127">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="9be69-127">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9be69-128">-DefaultProfile</span></span>
<span data-ttu-id="9be69-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9be69-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-130">-Location</span><span class="sxs-lookup"><span data-stu-id="9be69-130">-Location</span></span>
<span data-ttu-id="9be69-131">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="9be69-131">The location to store deployment data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="9be69-132">-Pre</span></span>
<span data-ttu-id="9be69-133">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="9be69-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-134">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="9be69-134">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="9be69-135">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="9be69-135">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="9be69-136">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="9be69-136">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="9be69-137">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="9be69-137">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-138">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="9be69-138">-TemplateFile</span></span>
<span data-ttu-id="9be69-139">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="9be69-139">Local path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileWithNoParameters, ByTemplateFileAndParameterObject, ByTemplateFileAndParameterFile, ByTemplateFileAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-140">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="9be69-140">-TemplateObject</span></span>
<span data-ttu-id="9be69-141">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="9be69-141">A hash table which represents the template.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateObjectAndParameterFile, ByTemplateObjectAndParameterUri, ByTemplateObjectWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-142">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="9be69-142">-TemplateParameterFile</span></span>
<span data-ttu-id="9be69-143">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="9be69-143">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterFile, ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-144">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="9be69-144">-TemplateParameterObject</span></span>
<span data-ttu-id="9be69-145">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="9be69-145">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateObjectAndParameterObject, ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-146">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="9be69-146">-TemplateParameterUri</span></span>
<span data-ttu-id="9be69-147">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="9be69-147">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateObjectAndParameterUri, ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-148">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="9be69-148">-TemplateUri</span></span>
<span data-ttu-id="9be69-149">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="9be69-149">Uri to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateUriAndParameterObject, ByTemplateUriAndParameterFile, ByTemplateUriAndParameterUri, ByTemplateUriWithNoParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9be69-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be69-150">CommonParameters</span></span>
<span data-ttu-id="9be69-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9be69-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be69-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9be69-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be69-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9be69-153">INPUTS</span></span>

### <span data-ttu-id="9be69-154">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9be69-154">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9be69-155">System. String</span><span class="sxs-lookup"><span data-stu-id="9be69-155">System.String</span></span>

## <span data-ttu-id="9be69-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9be69-156">OUTPUTS</span></span>

### <span data-ttu-id="9be69-157">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="9be69-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="9be69-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="9be69-158">NOTES</span></span>

## <span data-ttu-id="9be69-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9be69-159">RELATED LINKS</span></span>
