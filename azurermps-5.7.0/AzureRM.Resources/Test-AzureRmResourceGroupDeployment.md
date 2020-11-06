---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 0caf541aeadcbf2617ae5d31d0dfaf69e432e888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567929"
---
# <span data-ttu-id="f6473-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6473-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="f6473-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6473-102">SYNOPSIS</span></span>
<span data-ttu-id="f6473-103">Проверяет развертывание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6473-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6473-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6473-104">SYNTAX</span></span>

### <span data-ttu-id="f6473-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f6473-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6473-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f6473-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6473-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="f6473-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6473-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f6473-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6473-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="f6473-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6473-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f6473-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6473-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="f6473-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6473-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="f6473-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6473-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6473-113">DESCRIPTION</span></span>
<span data-ttu-id="f6473-114">Командлет **Test-AzureRmResourceGroupDeployment** определяет, являются ли шаблон развертывания группы ресурсов Azure и значения его параметров допустимыми.</span><span class="sxs-lookup"><span data-stu-id="f6473-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="f6473-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6473-115">EXAMPLES</span></span>

## <span data-ttu-id="f6473-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6473-116">PARAMETERS</span></span>

### <span data-ttu-id="f6473-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f6473-117">-ApiVersion</span></span>
<span data-ttu-id="f6473-118">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6473-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f6473-119">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f6473-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f6473-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6473-120">-DefaultProfile</span></span>
<span data-ttu-id="f6473-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6473-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6473-122">Режим</span><span class="sxs-lookup"><span data-stu-id="f6473-122">-Mode</span></span>
<span data-ttu-id="f6473-123">Задает режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="f6473-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="f6473-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f6473-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6473-125">Разност</span><span class="sxs-lookup"><span data-stu-id="f6473-125">Incremental</span></span>
- <span data-ttu-id="f6473-126">Полнот</span><span class="sxs-lookup"><span data-stu-id="f6473-126">Complete</span></span>

```yaml
Type: DeploymentMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6473-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="f6473-127">-Pre</span></span>
<span data-ttu-id="f6473-128">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f6473-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f6473-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6473-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6473-130">Указывает имя тестируемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6473-130">Specifies the name of the resource group to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6473-131">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f6473-131">-TemplateFile</span></span>
<span data-ttu-id="f6473-132">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="f6473-132">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="f6473-133">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="f6473-133">-TemplateParameterFile</span></span>
<span data-ttu-id="f6473-134">Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="f6473-134">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

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

### <span data-ttu-id="f6473-135">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="f6473-135">-TemplateParameterObject</span></span>
<span data-ttu-id="f6473-136">Указывает хэш-таблицу имен и значений параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="f6473-136">Specifies a hash table of template parameter names and values.</span></span>

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

### <span data-ttu-id="f6473-137">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="f6473-137">-TemplateParameterUri</span></span>
<span data-ttu-id="f6473-138">Задает универсальный код ресурса (URI) файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="f6473-138">Specifies the URI of a template parameters file.</span></span>

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

### <span data-ttu-id="f6473-139">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="f6473-139">-TemplateUri</span></span>
<span data-ttu-id="f6473-140">Задает универсальный код ресурса (URI) для файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="f6473-140">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="f6473-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6473-141">CommonParameters</span></span>
<span data-ttu-id="f6473-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6473-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6473-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6473-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6473-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6473-144">INPUTS</span></span>

### <span data-ttu-id="f6473-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="f6473-145">None</span></span>
<span data-ttu-id="f6473-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f6473-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6473-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6473-147">OUTPUTS</span></span>

### <span data-ttu-id="f6473-148">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="f6473-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="f6473-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6473-149">NOTES</span></span>

## <span data-ttu-id="f6473-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6473-150">RELATED LINKS</span></span>

[<span data-ttu-id="f6473-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6473-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f6473-152">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6473-152">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f6473-153">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6473-153">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f6473-154">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f6473-154">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


