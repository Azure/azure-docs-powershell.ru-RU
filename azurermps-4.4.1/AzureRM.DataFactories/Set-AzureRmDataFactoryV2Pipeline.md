---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: 510f0f5b943a1a0abab1bc97ac5e70fa6f450898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560439"
---
# <span data-ttu-id="1fe5f-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1fe5f-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="1fe5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fe5f-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe5f-103">Создание конвейера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fe5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fe5f-104">SYNTAX</span></span>

### <span data-ttu-id="1fe5f-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fe5f-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fe5f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe5f-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe5f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fe5f-107">DESCRIPTION</span></span>
<span data-ttu-id="1fe5f-108">Командлет Set-AzureRmDataFactoryV2Pipeline создает конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="1fe5f-109">Если указать имя для конвейера, который уже существует, командлет запрашивает подтверждение перед заменой конвейера.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="1fe5f-110">Если указан параметр Force, командлет заменяет существующий конвейер без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>

<span data-ttu-id="1fe5f-111">Для выполнения этих операций выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="1fe5f-112">Если конвейер с таким именем уже существует в фабрике данных, этот командлет предложит вам подтвердить, нужно ли перезаписывать существующий конвейер с помощью нового конвейера.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-112">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="1fe5f-113">Если вы подтвердите перезапись существующего конвейера, определение конвейера также заменяется.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-113">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="1fe5f-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fe5f-114">EXAMPLES</span></span>

### <span data-ttu-id="1fe5f-115">Пример 1: создание конвейера</span><span class="sxs-lookup"><span data-stu-id="1fe5f-115">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="1fe5f-116">Эта команда создает конвейер с именем DPWikisample в фабрике данных с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-116">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="1fe5f-117">Команда основывается на сведениях в DPWikisample.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-117">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="1fe5f-118">Этот файл содержит сведения о действиях, таких как копирование и действия по HDInsight в конвейере.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-118">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="1fe5f-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fe5f-119">PARAMETERS</span></span>

### <span data-ttu-id="1fe5f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fe5f-120">-Confirm</span></span>
<span data-ttu-id="1fe5f-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe5f-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1fe5f-122">-DataFactoryName</span></span>
<span data-ttu-id="1fe5f-123">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1fe5f-124">Этот командлет создает конвейер для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-124">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1fe5f-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1fe5f-125">-DefinitionFile</span></span>
<span data-ttu-id="1fe5f-126">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-126">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe5f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="1fe5f-127">-Force</span></span>
<span data-ttu-id="1fe5f-128">Указывает на то, что этот командлет заменяет существующий конвейер без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-128">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1fe5f-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fe5f-129">-Name</span></span>
<span data-ttu-id="1fe5f-130">Указывает имя создаваемого конвейера.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-130">Specifies the name of the pipeline to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe5f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe5f-131">-ResourceGroupName</span></span>
<span data-ttu-id="1fe5f-132">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1fe5f-133">Этот командлет создает конвейер для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-133">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1fe5f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe5f-134">-ResourceId</span></span>
<span data-ttu-id="1fe5f-135">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-135">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe5f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe5f-136">-WhatIf</span></span>
<span data-ttu-id="1fe5f-137">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe5f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe5f-138">-DefaultProfile</span></span>
<span data-ttu-id="1fe5f-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe5f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe5f-140">CommonParameters</span></span>
<span data-ttu-id="1fe5f-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fe5f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe5f-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe5f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe5f-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fe5f-143">INPUTS</span></span>

### <span data-ttu-id="1fe5f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1fe5f-144">System.String</span></span>

## <span data-ttu-id="1fe5f-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fe5f-145">OUTPUTS</span></span>

### <span data-ttu-id="1fe5f-146">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1fe5f-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="1fe5f-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fe5f-147">NOTES</span></span>
<span data-ttu-id="1fe5f-148">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="1fe5f-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1fe5f-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fe5f-149">RELATED LINKS</span></span>

[<span data-ttu-id="1fe5f-150">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1fe5f-150">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="1fe5f-151">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1fe5f-151">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="1fe5f-152">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1fe5f-152">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
