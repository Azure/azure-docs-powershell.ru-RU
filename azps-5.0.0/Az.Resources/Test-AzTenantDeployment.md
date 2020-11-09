---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Test-AzTenantDeployment.md
ms.openlocfilehash: 5144dacb044523c2ad72d0a9c24aa43427f14f99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318866"
---
# <span data-ttu-id="fb224-101">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="fb224-101">Test-AzTenantDeployment</span></span>

## <span data-ttu-id="fb224-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb224-102">SYNOPSIS</span></span>
<span data-ttu-id="fb224-103">Проверяет развертывание в области клиента.</span><span class="sxs-lookup"><span data-stu-id="fb224-103">Validates a deployment at tenant scope.</span></span>

## <span data-ttu-id="fb224-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb224-104">SYNTAX</span></span>

### <span data-ttu-id="fb224-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb224-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateFile <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-106">ByTemplateObjectAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="fb224-106">ByTemplateObjectAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-107">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="fb224-107">ByTemplateFileAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-108">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="fb224-108">ByTemplateUriAndParameterObject</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-109">ByTemplateObjectAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="fb224-109">ByTemplateObjectAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-110">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="fb224-110">ByTemplateFileAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-111">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="fb224-111">ByTemplateUriAndParameterFile</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-112">ByTemplateObjectAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="fb224-112">ByTemplateObjectAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateObject <Hashtable>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-113">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="fb224-113">ByTemplateFileAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-114">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="fb224-114">ByTemplateUriAndParameterUri</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-SkipTemplateParameterPrompt] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-115">ByTemplateObjectWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="fb224-115">ByTemplateObjectWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateObject <Hashtable> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb224-116">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="fb224-116">ByTemplateUriWithNoParameters</span></span>
```
Test-AzTenantDeployment -Location <String> -TemplateUri <String> [-SkipTemplateParameterPrompt] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb224-117">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb224-117">DESCRIPTION</span></span>
<span data-ttu-id="fb224-118">Командлет **Test-AzTenantDeployment** определяет, является ли шаблон развертывания и значения его параметров допустимыми в текущей области клиента.</span><span class="sxs-lookup"><span data-stu-id="fb224-118">The **Test-AzTenantDeployment** cmdlet determines whether a deployment template and its parameter values are valid at the current tenant scope.</span></span>

## <span data-ttu-id="fb224-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb224-119">EXAMPLES</span></span>

### <span data-ttu-id="fb224-120">Пример 1: Проверка развертывания с помощью настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="fb224-120">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\OrgSetup.json" -TemplateParameterFile "D:\Azure\Templates\OrgParms.json"
```

<span data-ttu-id="fb224-121">Эта команда проверяет развертывание в текущей области клиента с помощью заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="fb224-121">This command tests a deployment at the current tenant scope using the given template file and parameters file.</span></span>

### <span data-ttu-id="fb224-122">Пример 2: Проверка развертывания с помощью настраиваемого объекта шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="fb224-122">Example 2: Test deployment with a custom template object and parameter file</span></span>
```
PS C:\> $TemplateFileText = [System.IO.File]::ReadAllText("D:\Azure\Templates\OrgSetup.json")
PS C:\> $TemplateObject = ConvertFrom-Json $TemplateFileText -AsHashtable
PS C:\> Test-AzTenantDeployment -Location "West US" -TemplateObject $TemplateObject -TemplateParameterFile "D:\Azure\Templates\EngSiteParams.json"
```

<span data-ttu-id="fb224-123">Эта команда проверяет развертывание в текущей области клиента с помощью хэш-таблицы в памяти, созданной из заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="fb224-123">This command tests a deployment at the current tenant scope using the an in-memory hashtable created from the given template file and a parameter file.</span></span>

## <span data-ttu-id="fb224-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb224-124">PARAMETERS</span></span>

### <span data-ttu-id="fb224-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb224-125">-DefaultProfile</span></span>
<span data-ttu-id="fb224-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb224-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb224-127">-Location</span><span class="sxs-lookup"><span data-stu-id="fb224-127">-Location</span></span>
<span data-ttu-id="fb224-128">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="fb224-128">The location to store deployment data.</span></span>

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

### <span data-ttu-id="fb224-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="fb224-129">-Pre</span></span>
<span data-ttu-id="fb224-130">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="fb224-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fb224-131">-SkipTemplateParameterPrompt</span><span class="sxs-lookup"><span data-stu-id="fb224-131">-SkipTemplateParameterPrompt</span></span>
<span data-ttu-id="fb224-132">Пропускает обработку динамических параметров PowerShell, которая проверяет, есть ли в указанном параметре шаблона все необходимые параметры, используемые шаблоном.</span><span class="sxs-lookup"><span data-stu-id="fb224-132">Skips the PowerShell dynamic parameter processing that checks if the provided template parameter contains all necessary parameters used by the template.</span></span>
<span data-ttu-id="fb224-133">Эта проверка предложит пользователю предоставить значение для отсутствующих параметров, но при этом параметр-SkipTemplateParameterPrompt будет игнорировать этот запрос и сразу же выдать сообщение об ошибке, если в шаблоне не была выполнена привязка параметра.</span><span class="sxs-lookup"><span data-stu-id="fb224-133">This check would prompt the user to provide a value for the missing parameters, but providing the -SkipTemplateParameterPrompt will ignore this prompt and error out immediately if a parameter was found not to be bound in the template.</span></span>
<span data-ttu-id="fb224-134">Для неинтерактивных скриптов параметр-SkipTemplateParameterPrompt можно использовать для предоставления более качественного сообщения об ошибке в случае, если не все необходимые параметры выполнены.</span><span class="sxs-lookup"><span data-stu-id="fb224-134">For non-interactive scripts, -SkipTemplateParameterPrompt can be provided to provide a better error message in the case where not all required parameters are satisfied.</span></span>

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

### <span data-ttu-id="fb224-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="fb224-135">-TemplateFile</span></span>
<span data-ttu-id="fb224-136">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="fb224-136">Local path to the template file.</span></span>

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

### <span data-ttu-id="fb224-137">-TemplateObject</span><span class="sxs-lookup"><span data-stu-id="fb224-137">-TemplateObject</span></span>
<span data-ttu-id="fb224-138">Хэш-таблица, представляющая шаблон.</span><span class="sxs-lookup"><span data-stu-id="fb224-138">A hash table which represents the template.</span></span>

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

### <span data-ttu-id="fb224-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="fb224-139">-TemplateParameterFile</span></span>
<span data-ttu-id="fb224-140">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="fb224-140">A file that has the template parameters.</span></span>

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

### <span data-ttu-id="fb224-141">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="fb224-141">-TemplateParameterObject</span></span>
<span data-ttu-id="fb224-142">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="fb224-142">A hash table which represents the parameters.</span></span>

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

### <span data-ttu-id="fb224-143">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="fb224-143">-TemplateParameterUri</span></span>
<span data-ttu-id="fb224-144">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="fb224-144">Uri to the template parameter file.</span></span>

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

### <span data-ttu-id="fb224-145">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="fb224-145">-TemplateUri</span></span>
<span data-ttu-id="fb224-146">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="fb224-146">Uri to the template file.</span></span>

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

### <span data-ttu-id="fb224-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb224-147">CommonParameters</span></span>
<span data-ttu-id="fb224-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb224-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb224-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb224-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb224-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb224-150">INPUTS</span></span>

### <span data-ttu-id="fb224-151">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fb224-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fb224-152">System. String</span><span class="sxs-lookup"><span data-stu-id="fb224-152">System.String</span></span>

## <span data-ttu-id="fb224-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb224-153">OUTPUTS</span></span>

### <span data-ttu-id="fb224-154">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="fb224-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="fb224-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb224-155">NOTES</span></span>

## <span data-ttu-id="fb224-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb224-156">RELATED LINKS</span></span>
