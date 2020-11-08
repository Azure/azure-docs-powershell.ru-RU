---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzManagementGroupDeployment.md
ms.openlocfilehash: 81ee04b5248a95d686c2c135dfee0e73e6722bb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066174"
---
# <span data-ttu-id="c0082-101">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c0082-101">Test-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="c0082-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0082-102">SYNOPSIS</span></span>
<span data-ttu-id="c0082-103">Проверка развертывания в группе "Управление".</span><span class="sxs-lookup"><span data-stu-id="c0082-103">Validates a deployment at a management group.</span></span>

## <span data-ttu-id="c0082-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0082-104">SYNTAX</span></span>

### <span data-ttu-id="c0082-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0082-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0082-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c0082-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0082-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c0082-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0082-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="c0082-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String>
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-SkipTemplateParameterPrompt]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0082-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c0082-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0082-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c0082-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0082-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="c0082-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterFile <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0082-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c0082-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0082-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c0082-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateFile <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0082-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="c0082-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateParameterUri <String>
 -TemplateUri <String> [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0082-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c0082-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0082-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="c0082-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzManagementGroupDeployment -ManagementGroupId <String> -Location <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0082-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0082-117">DESCRIPTION</span></span>
<span data-ttu-id="c0082-118">Командлет **Test-AzManagementGroupDeployment** определяет, является ли шаблон развертывания и значения его параметров допустимыми в группе управления.</span><span class="sxs-lookup"><span data-stu-id="c0082-118">The **Test-AzManagementGroupDeployment** cmdlet determines whether a deployment template and its parameter values are valid at a management group.</span></span>

## <span data-ttu-id="c0082-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0082-119">EXAMPLES</span></span>

### <span data-ttu-id="c0082-120">Пример 1: Проверка развертывания с помощью настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="c0082-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="c0082-121">Эта команда проверяет развертывание в группе управления "myMG" с помощью заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="c0082-121">This command tests a deployment at the management group "myMG" using the given template file and parameters file.</span></span>

### <span data-ttu-id="c0082-122">Пример 2: Проверка развертывания с помощью настраиваемого объекта шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="c0082-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzManagementGroupDeployment -ManagementGroupId "myMG" -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="c0082-123">Эта команда проверяет развертывание в группе управления "myMG" с помощью хеш-таблицы в памяти, созданной из заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="c0082-123">This command tests a deployment at the management group "myMG" using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="c0082-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0082-124">PARAMETERS</span></span>

### <span data-ttu-id="c0082-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c0082-125">-ApiVersion</span></span>
<span data-ttu-id="c0082-126">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0082-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c0082-127">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="c0082-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c0082-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0082-128">-DefaultProfile</span></span>
<span data-ttu-id="c0082-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0082-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0082-130">-Location</span><span class="sxs-lookup"><span data-stu-id="c0082-130">-Location</span></span>
<span data-ttu-id="c0082-131">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="c0082-131">The location to store deployment data.</span></span>

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

### <span data-ttu-id="c0082-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c0082-132">-ManagementGroupId</span></span>
<span data-ttu-id="c0082-133">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="c0082-133">The management group id.</span></span>

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

### <span data-ttu-id="c0082-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="c0082-134">-Pre</span></span>
<span data-ttu-id="c0082-135">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="c0082-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c0082-136">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="c0082-136">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="c0082-137">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="c0082-137">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="c0082-138">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="c0082-138">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="c0082-139">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="c0082-139">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="c0082-140">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="c0082-140">-TemplateFile</span></span>
<span data-ttu-id="c0082-141">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="c0082-141">Local path to the template file.</span></span>

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

### <span data-ttu-id="c0082-142">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="c0082-142">-TemplateObject</span></span>
<span data-ttu-id="c0082-143">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="c0082-143">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="c0082-144">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="c0082-144">-TemplateParameterFile</span></span>
<span data-ttu-id="c0082-145">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="c0082-145">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="c0082-146">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="c0082-146">-TemplateParameterObject</span></span>
<span data-ttu-id="c0082-147">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="c0082-147">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="c0082-148">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="c0082-148">-TemplateParameterUri</span></span>
<span data-ttu-id="c0082-149">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="c0082-149">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="c0082-150">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="c0082-150">-TemplateUri</span></span>
<span data-ttu-id="c0082-151">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="c0082-151">Uri to the template file.</span></span>

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

### <span data-ttu-id="c0082-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0082-152">CommonParameters</span></span>
<span data-ttu-id="c0082-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0082-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0082-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0082-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0082-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0082-155">INPUTS</span></span>

### <span data-ttu-id="c0082-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0082-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c0082-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c0082-157">System.String</span></span>

## <span data-ttu-id="c0082-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0082-158">OUTPUTS</span></span>

### <span data-ttu-id="c0082-159">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="c0082-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="c0082-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0082-160">NOTES</span></span>

## <span data-ttu-id="c0082-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0082-161">RELATED LINKS</span></span>
