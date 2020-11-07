---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/test-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f1109e61c2ea1f8c4d2f20aec7927cc550f95249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734293"
---
# <span data-ttu-id="8f212-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8f212-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="8f212-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f212-102">SYNOPSIS</span></span>
<span data-ttu-id="8f212-103">Проверяет развертывание группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f212-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f212-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f212-104">SYNTAX</span></span>

### <span data-ttu-id="8f212-105">ByTemplateFileWithNoParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f212-105">ByTemplateFileWithNoParameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateFile <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f212-106">ByTemplateFileAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8f212-106">ByTemplateFileAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f212-107">ByTemplateUriAndParameterObject</span><span class="sxs-lookup"><span data-stu-id="8f212-107">ByTemplateUriAndParameterObject</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterObject <Hashtable>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f212-108">ByTemplateFileAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8f212-108">ByTemplateFileAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f212-109">ByTemplateUriAndParameterFile</span><span class="sxs-lookup"><span data-stu-id="8f212-109">ByTemplateUriAndParameterFile</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterFile <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f212-110">ByTemplateFileAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8f212-110">ByTemplateFileAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateFile <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f212-111">ByTemplateUriAndParameterUri</span><span class="sxs-lookup"><span data-stu-id="8f212-111">ByTemplateUriAndParameterUri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateParameterUri <String>
 -TemplateUri <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f212-112">ByTemplateUriWithNoParameters</span><span class="sxs-lookup"><span data-stu-id="8f212-112">ByTemplateUriWithNoParameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 [-RollbackToLastDeployment] [-RollBackDeploymentName <String>] -TemplateUri <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f212-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f212-113">DESCRIPTION</span></span>
<span data-ttu-id="8f212-114">Командлет **Test-AzureRmResourceGroupDeployment** определяет, являются ли шаблон развертывания группы ресурсов Azure и значения его параметров допустимыми.</span><span class="sxs-lookup"><span data-stu-id="8f212-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="8f212-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f212-115">EXAMPLES</span></span>

## <span data-ttu-id="8f212-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f212-116">PARAMETERS</span></span>

### <span data-ttu-id="8f212-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8f212-117">-ApiVersion</span></span>
<span data-ttu-id="8f212-118">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f212-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8f212-119">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f212-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8f212-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f212-120">-DefaultProfile</span></span>
<span data-ttu-id="8f212-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8f212-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f212-122">Режим</span><span class="sxs-lookup"><span data-stu-id="8f212-122">-Mode</span></span>
<span data-ttu-id="8f212-123">Задает режим развертывания.</span><span class="sxs-lookup"><span data-stu-id="8f212-123">Specifies the deployment mode.</span></span>
<span data-ttu-id="8f212-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8f212-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8f212-125">Разност</span><span class="sxs-lookup"><span data-stu-id="8f212-125">Incremental</span></span>
- <span data-ttu-id="8f212-126">Полнот</span><span class="sxs-lookup"><span data-stu-id="8f212-126">Complete</span></span>

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

### <span data-ttu-id="8f212-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="8f212-127">-Pre</span></span>
<span data-ttu-id="8f212-128">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="8f212-128">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8f212-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f212-129">-ResourceGroupName</span></span>
<span data-ttu-id="8f212-130">Указывает имя тестируемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f212-130">Specifies the name of the resource group to test.</span></span>

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

### <span data-ttu-id="8f212-131">-RollBackDeploymentName</span><span class="sxs-lookup"><span data-stu-id="8f212-131">-RollBackDeploymentName</span></span>
<span data-ttu-id="8f212-132">Откат к успешному развертыванию с указанным именем в группе ресурсов не следует использовать, если используется параметр-RollbackToLastDeployment.</span><span class="sxs-lookup"><span data-stu-id="8f212-132">Rollback to the successful deployment with the given name in the resource group, should not be used if -RollbackToLastDeployment is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f212-133">-RollbackToLastDeployment</span><span class="sxs-lookup"><span data-stu-id="8f212-133">-RollbackToLastDeployment</span></span>
<span data-ttu-id="8f212-134">Откат к последнему успешному развертыванию в группе ресурсов не отображается, если используется значение-RollBackDeploymentName.</span><span class="sxs-lookup"><span data-stu-id="8f212-134">Rollback to the last successful deployment in the resource group, should not be present if -RollBackDeploymentName is used.</span></span>

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

### <span data-ttu-id="8f212-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="8f212-135">-TemplateFile</span></span>
<span data-ttu-id="8f212-136">Указывает полный путь к файлу шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="8f212-136">Specifies the full path of a JSON template file.</span></span>

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

### <span data-ttu-id="8f212-137">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8f212-137">-TemplateParameterFile</span></span>
<span data-ttu-id="8f212-138">Задает полный путь к файлу JSON, содержащему имена и значения параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="8f212-138">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterFile, ByTemplateUriAndParameterFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f212-139">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8f212-139">-TemplateParameterObject</span></span>
<span data-ttu-id="8f212-140">Указывает хэш-таблицу имен и значений параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="8f212-140">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTemplateFileAndParameterObject, ByTemplateUriAndParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f212-141">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8f212-141">-TemplateParameterUri</span></span>
<span data-ttu-id="8f212-142">Задает универсальный код ресурса (URI) файла параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="8f212-142">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTemplateFileAndParameterUri, ByTemplateUriAndParameterUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f212-143">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8f212-143">-TemplateUri</span></span>
<span data-ttu-id="8f212-144">Задает универсальный код ресурса (URI) для файла шаблона JSON.</span><span class="sxs-lookup"><span data-stu-id="8f212-144">Specifies the URI of a JSON template file.</span></span>

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

### <span data-ttu-id="8f212-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f212-145">CommonParameters</span></span>
<span data-ttu-id="8f212-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f212-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f212-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f212-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f212-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f212-148">INPUTS</span></span>

### <span data-ttu-id="8f212-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="8f212-149">None</span></span>

## <span data-ttu-id="8f212-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f212-150">OUTPUTS</span></span>

### <span data-ttu-id="8f212-151">Microsoft. Azure. Commands. ResourceManager. Models. PSResourceManagerError</span><span class="sxs-lookup"><span data-stu-id="8f212-151">Microsoft.Azure.Commands.ResourceManager.Models.PSResourceManagerError</span></span>

## <span data-ttu-id="8f212-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f212-152">NOTES</span></span>

## <span data-ttu-id="8f212-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f212-153">RELATED LINKS</span></span>

[<span data-ttu-id="8f212-154">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8f212-154">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8f212-155">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8f212-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8f212-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8f212-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8f212-157">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8f212-157">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


