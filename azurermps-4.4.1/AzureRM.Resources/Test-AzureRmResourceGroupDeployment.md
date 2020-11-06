---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565166"
---
# <span data-ttu-id="3435b-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3435b-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="3435b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3435b-102">SYNOPSIS</span></span>
<span data-ttu-id="3435b-103">Проверяет развертывание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3435b-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3435b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3435b-104">SYNTAX</span></span>

### <span data-ttu-id="3435b-105">Развертывание с помощью файла шаблона без параметров (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3435b-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3435b-106">Развертывание с помощью файла шаблона и объекта "Параметры шаблона"</span><span class="sxs-lookup"><span data-stu-id="3435b-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3435b-107">Развертывание с помощью URI шаблона и объекта "Параметры шаблона"</span><span class="sxs-lookup"><span data-stu-id="3435b-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3435b-108">Развертывание с помощью файла шаблона и файла параметров шаблона</span><span class="sxs-lookup"><span data-stu-id="3435b-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3435b-109">Развертывание с помощью URI шаблона и файла параметров шаблона</span><span class="sxs-lookup"><span data-stu-id="3435b-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3435b-110">Развертывание с помощью URI параметров шаблона файла шаблона</span><span class="sxs-lookup"><span data-stu-id="3435b-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3435b-111">Развертывание с помощью URI шаблона и URI параметров шаблона</span><span class="sxs-lookup"><span data-stu-id="3435b-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3435b-112">Развертывание с помощью URI шаблона без параметров</span><span class="sxs-lookup"><span data-stu-id="3435b-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3435b-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3435b-113">DESCRIPTION</span></span>
<span data-ttu-id="3435b-114">Командлет **Test-AzureRmResourceGroupDeployment** определяет, являются ли шаблон развертывания группы ресурсов Azure и значения его параметров допустимыми.</span><span class="sxs-lookup"><span data-stu-id="3435b-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="3435b-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3435b-115">EXAMPLES</span></span>

## <span data-ttu-id="3435b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3435b-116">PARAMETERS</span></span>

### <span data-ttu-id="3435b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3435b-117">-ApiVersion</span></span>
<span data-ttu-id="3435b-118">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3435b-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="3435b-119">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3435b-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="3435b-120">Режим</span><span class="sxs-lookup"><span data-stu-id="3435b-120">-Mode</span></span>
<span data-ttu-id="3435b-121">Задает режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="3435b-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="3435b-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3435b-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3435b-123">Разност</span><span class="sxs-lookup"><span data-stu-id="3435b-123">Incremental</span></span>
- <span data-ttu-id="3435b-124">Полнот</span><span class="sxs-lookup"><span data-stu-id="3435b-124">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3435b-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="3435b-125">-Pre</span></span>
<span data-ttu-id="3435b-126">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="3435b-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3435b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3435b-127">-ResourceGroupName</span></span>
<span data-ttu-id="3435b-128">Указывает имя тестируемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3435b-128">Specifies the name of the resource group to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3435b-129">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="3435b-129">-TemplateFile</span></span>
<span data-ttu-id="3435b-130">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="3435b-130">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3435b-131">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="3435b-131">-TemplateParameterFile</span></span>
<span data-ttu-id="3435b-132">Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="3435b-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3435b-133">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="3435b-133">-TemplateParameterObject</span></span>
<span data-ttu-id="3435b-134">Указывает хэш-таблицу имен и значений параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="3435b-134">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3435b-135">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="3435b-135">-TemplateParameterUri</span></span>
<span data-ttu-id="3435b-136">Задает универсальный код ресурса (URI) файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="3435b-136">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3435b-137">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3435b-137">-TemplateUri</span></span>
<span data-ttu-id="3435b-138">Задает универсальный код ресурса (URI) для файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="3435b-138">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3435b-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3435b-139">-DefaultProfile</span></span>
<span data-ttu-id="3435b-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3435b-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3435b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3435b-141">CommonParameters</span></span>
<span data-ttu-id="3435b-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3435b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3435b-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3435b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3435b-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3435b-144">INPUTS</span></span>

## <span data-ttu-id="3435b-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3435b-145">OUTPUTS</span></span>

### <span data-ttu-id="3435b-146">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="3435b-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="3435b-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="3435b-147">NOTES</span></span>

## <span data-ttu-id="3435b-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3435b-148">RELATED LINKS</span></span>

[<span data-ttu-id="3435b-149">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3435b-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="3435b-150">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3435b-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="3435b-151">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3435b-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="3435b-152">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3435b-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


