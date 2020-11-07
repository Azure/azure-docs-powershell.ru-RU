---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/test-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Test-AzDeployment.md
ms.openlocfilehash: 77c2a712a3d44d963fd08642d1a1c88b5d8c81e1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910813"
---
# <span data-ttu-id="6d7a7-101">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="6d7a7-101">Test-AzDeployment</span></span>

## <span data-ttu-id="6d7a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d7a7-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7a7-103">Проверка развертывания.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-103">Validates a deployment.</span></span>

## <span data-ttu-id="6d7a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d7a7-104">SYNTAX</span></span>

### <span data-ttu-id="6d7a7-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d7a7-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzDeployment -Location <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d7a7-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6d7a7-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d7a7-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="6d7a7-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterObject <Hashtable> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d7a7-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6d7a7-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d7a7-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="6d7a7-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterFile <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d7a7-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6d7a7-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d7a7-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="6d7a7-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzDeployment -Location <String> -TemplateParameterUri <String> -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d7a7-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="6d7a7-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzDeployment -Location <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d7a7-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d7a7-113">DESCRIPTION</span></span>
<span data-ttu-id="6d7a7-114">Командлет **Test-AzDeployment** определяет, являются ли шаблон развертывания и значения его параметров допустимыми.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-114">The **Test-AzDeployment** cmdlet determines whether a deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="6d7a7-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d7a7-115">EXAMPLES</span></span>

### <span data-ttu-id="6d7a7-116">Пример 1: Проверка развертывания с помощью настраиваемого шаблона и файла параметров</span><span class="sxs-lookup"><span data-stu-id="6d7a7-116">Example 1: Test deployment with a custom template and parameter file</span></span>
```
PS C:\>Test-AzDeployment -Location "West US" -TemplateFile "D:\Azure\Templates\EngineeringSite.json" -TemplateParameterFile "D:\Azure\Templates\EngSiteParms.json"
```

<span data-ttu-id="6d7a7-117">Эта команда проверяет развертывание в текущей области подписки с помощью заданного файла шаблона и файла параметров.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-117">This command tests a deployment at the current subscription scope using the given template file and parameters file.</span></span>

## <span data-ttu-id="6d7a7-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d7a7-118">PARAMETERS</span></span>

### <span data-ttu-id="6d7a7-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6d7a7-119">-ApiVersion</span></span>
<span data-ttu-id="6d7a7-120">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6d7a7-121">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6d7a7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7a7-122">-DefaultProfile</span></span>
<span data-ttu-id="6d7a7-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7a7-124">-Location</span><span class="sxs-lookup"><span data-stu-id="6d7a7-124">-Location</span></span>
<span data-ttu-id="6d7a7-125">Расположение для хранения данных развертывания.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-125">The location to store deployment data.</span></span>

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

### <span data-ttu-id="6d7a7-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="6d7a7-126">-Pre</span></span>
<span data-ttu-id="6d7a7-127">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="6d7a7-128">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="6d7a7-128">-TemplateFile</span></span>
<span data-ttu-id="6d7a7-129">Локальный путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-129">Local path to the template file.</span></span>

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

### <span data-ttu-id="6d7a7-130">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="6d7a7-130">-TemplateParameterFile</span></span>
<span data-ttu-id="6d7a7-131">Файл с параметрами шаблона.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-131">A file that has the template parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7a7-132">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="6d7a7-132">-TemplateParameterObject</span></span>
<span data-ttu-id="6d7a7-133">Хэш-таблица, представляющая параметры.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-133">A hash table which represents the parameters.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7a7-134">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="6d7a7-134">-TemplateParameterUri</span></span>
<span data-ttu-id="6d7a7-135">Универсальный код ресурса (URI) в файл параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-135">Uri to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7a7-136">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="6d7a7-136">-TemplateUri</span></span>
<span data-ttu-id="6d7a7-137">Универсальный код ресурса (URI) в файл шаблона.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-137">Uri to the template file.</span></span>

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

### <span data-ttu-id="6d7a7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7a7-138">CommonParameters</span></span>
<span data-ttu-id="6d7a7-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d7a7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7a7-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d7a7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7a7-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d7a7-141">INPUTS</span></span>

### <span data-ttu-id="6d7a7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6d7a7-142">System.String</span></span>
<span data-ttu-id="6d7a7-143">Microsoft. Azure. Management. ResourceManager. Models. DeploymentMode System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6d7a7-143">Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode System.Collections.Hashtable</span></span>

## <span data-ttu-id="6d7a7-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d7a7-144">OUTPUTS</span></span>

### <span data-ttu-id="6d7a7-145">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="6d7a7-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError</span></span>

## <span data-ttu-id="6d7a7-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d7a7-146">NOTES</span></span>

## <span data-ttu-id="6d7a7-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d7a7-147">RELATED LINKS</span></span>
