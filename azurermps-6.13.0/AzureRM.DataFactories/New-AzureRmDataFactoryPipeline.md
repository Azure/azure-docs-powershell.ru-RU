---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 30C1AF6C-A8DC-4CA0-9E5F-10641A29D0E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 7ad7eb0f87972c3a64b3fb966259d25d527c20c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560980"
---
# <span data-ttu-id="dd40e-101">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd40e-101">New-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="dd40e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd40e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd40e-103">Создание конвейера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="dd40e-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd40e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd40e-104">SYNTAX</span></span>

### <span data-ttu-id="dd40e-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd40e-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd40e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dd40e-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory> [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd40e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd40e-107">DESCRIPTION</span></span>
<span data-ttu-id="dd40e-108">Командлет **New-AzureRmDataFactoryPipeline** создает конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="dd40e-108">The **New-AzureRmDataFactoryPipeline** cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="dd40e-109">Если указать имя для конвейера, который уже существует, командлет запрашивает подтверждение перед заменой конвейера.</span><span class="sxs-lookup"><span data-stu-id="dd40e-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="dd40e-110">Если указан параметр *Force* , командлет заменяет существующий конвейер без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="dd40e-110">If you specify the *Force* parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="dd40e-111">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="dd40e-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="dd40e-112">Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="dd40e-112">Create a data factory.</span></span> 
- <span data-ttu-id="dd40e-113">Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="dd40e-113">Create linked services.</span></span> 
- <span data-ttu-id="dd40e-114">Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="dd40e-114">Create datasets.</span></span> 
- <span data-ttu-id="dd40e-115">Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="dd40e-115">Create a pipeline.</span></span>
<span data-ttu-id="dd40e-116">Если конвейер с таким именем уже существует в фабрике данных, этот командлет предложит вам подтвердить, нужно ли перезаписывать существующий конвейер с помощью нового конвейера.</span><span class="sxs-lookup"><span data-stu-id="dd40e-116">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="dd40e-117">Если вы подтвердите перезапись существующего конвейера, определение конвейера также заменяется.</span><span class="sxs-lookup"><span data-stu-id="dd40e-117">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="dd40e-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd40e-118">EXAMPLES</span></span>

### <span data-ttu-id="dd40e-119">Пример 1: создание конвейера</span><span class="sxs-lookup"><span data-stu-id="dd40e-119">Example 1: Create a pipeline</span></span>
```
PS C:\>New-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json" 
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF11
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="dd40e-120">Эта команда создает конвейер с именем DPWikisample в фабрике данных с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="dd40e-120">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="dd40e-121">Команда основывается на сведениях в DPWikisample.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="dd40e-121">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="dd40e-122">Этот файл содержит сведения о действиях, таких как копирование и действия по HDInsight в конвейере.</span><span class="sxs-lookup"><span data-stu-id="dd40e-122">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="dd40e-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd40e-123">PARAMETERS</span></span>

### <span data-ttu-id="dd40e-124">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="dd40e-124">-DataFactory</span></span>
<span data-ttu-id="dd40e-125">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="dd40e-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="dd40e-126">Этот командлет создает конвейер для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dd40e-126">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd40e-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="dd40e-127">-DataFactoryName</span></span>
<span data-ttu-id="dd40e-128">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="dd40e-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="dd40e-129">Этот командлет создает конвейер для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dd40e-129">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd40e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd40e-130">-DefaultProfile</span></span>
<span data-ttu-id="dd40e-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd40e-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd40e-132">-Файл</span><span class="sxs-lookup"><span data-stu-id="dd40e-132">-File</span></span>
<span data-ttu-id="dd40e-133">Указывает полный путь к файлу нотации объектов JavaScript (JSON), который содержит описание конвейера.</span><span class="sxs-lookup"><span data-stu-id="dd40e-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd40e-134">-Force</span><span class="sxs-lookup"><span data-stu-id="dd40e-134">-Force</span></span>
<span data-ttu-id="dd40e-135">Указывает на то, что этот командлет заменяет существующий конвейер без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="dd40e-135">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="dd40e-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd40e-136">-Name</span></span>
<span data-ttu-id="dd40e-137">Указывает имя создаваемого конвейера.</span><span class="sxs-lookup"><span data-stu-id="dd40e-137">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd40e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd40e-138">-ResourceGroupName</span></span>
<span data-ttu-id="dd40e-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="dd40e-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dd40e-140">Этот командлет создает конвейер для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dd40e-140">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd40e-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd40e-141">-Confirm</span></span>
<span data-ttu-id="dd40e-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd40e-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd40e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd40e-143">-WhatIf</span></span>
<span data-ttu-id="dd40e-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd40e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd40e-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd40e-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd40e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd40e-146">CommonParameters</span></span>
<span data-ttu-id="dd40e-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd40e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd40e-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd40e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd40e-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd40e-149">INPUTS</span></span>

### <span data-ttu-id="dd40e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="dd40e-150">System.String</span></span>

### <span data-ttu-id="dd40e-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="dd40e-151">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="dd40e-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd40e-152">OUTPUTS</span></span>

### <span data-ttu-id="dd40e-153">Microsoft. Azure. Commands. Factoring. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="dd40e-153">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="dd40e-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd40e-154">NOTES</span></span>
* <span data-ttu-id="dd40e-155">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="dd40e-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dd40e-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd40e-156">RELATED LINKS</span></span>

[<span data-ttu-id="dd40e-157">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd40e-157">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dd40e-158">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd40e-158">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dd40e-159">Возобновить — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd40e-159">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="dd40e-160">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="dd40e-160">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="dd40e-161">Приостановить — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="dd40e-161">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


