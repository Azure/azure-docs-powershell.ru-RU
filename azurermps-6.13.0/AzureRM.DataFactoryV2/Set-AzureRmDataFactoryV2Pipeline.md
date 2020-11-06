---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: dcdf7cdf9de6de23a3178fe8cbb4ac0f67f43d30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568923"
---
# <span data-ttu-id="0e760-101">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0e760-101">Set-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="0e760-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e760-102">SYNOPSIS</span></span>
<span data-ttu-id="0e760-103">Создание конвейера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="0e760-103">Creates a pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e760-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e760-104">SYNTAX</span></span>

### <span data-ttu-id="0e760-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e760-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e760-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e760-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e760-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e760-107">DESCRIPTION</span></span>
<span data-ttu-id="0e760-108">Командлет Set-AzureRmDataFactoryV2Pipeline создает конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="0e760-108">The Set-AzureRmDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="0e760-109">Если указать имя для конвейера, который уже существует, командлет запрашивает подтверждение перед заменой конвейера.</span><span class="sxs-lookup"><span data-stu-id="0e760-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="0e760-110">Если указан параметр Force, командлет заменяет существующий конвейер без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0e760-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="0e760-111">Эти операции выполняются в указанном ниже порядке:--Создание фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0e760-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="0e760-112">--Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="0e760-112">-- Create linked services.</span></span>
<span data-ttu-id="0e760-113">--Создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="0e760-113">-- Create datasets.</span></span>
<span data-ttu-id="0e760-114">--Создание конвейера.</span><span class="sxs-lookup"><span data-stu-id="0e760-114">-- Create a pipeline.</span></span>
<span data-ttu-id="0e760-115">Если конвейер с таким именем уже существует в фабрике данных, этот командлет предложит вам подтвердить, нужно ли перезаписывать существующий конвейер с помощью нового конвейера.</span><span class="sxs-lookup"><span data-stu-id="0e760-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="0e760-116">Если вы подтвердите перезапись существующего конвейера, определение конвейера также заменяется.</span><span class="sxs-lookup"><span data-stu-id="0e760-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="0e760-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e760-117">EXAMPLES</span></span>

### <span data-ttu-id="0e760-118">Пример 1: создание конвейера</span><span class="sxs-lookup"><span data-stu-id="0e760-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="0e760-119">Эта команда создает конвейер с именем DPWikisample в фабрике данных с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="0e760-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="0e760-120">Команда основывается на сведениях в DPWikisample.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="0e760-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="0e760-121">Этот файл содержит сведения о действиях, таких как копирование и действия по HDInsight в конвейере.</span><span class="sxs-lookup"><span data-stu-id="0e760-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="0e760-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e760-122">PARAMETERS</span></span>

### <span data-ttu-id="0e760-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0e760-123">-DataFactoryName</span></span>
<span data-ttu-id="0e760-124">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0e760-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0e760-125">Этот командлет создает конвейер для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0e760-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e760-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e760-126">-DefaultProfile</span></span>
<span data-ttu-id="0e760-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e760-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e760-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0e760-128">-DefinitionFile</span></span>
<span data-ttu-id="0e760-129">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="0e760-129">The JSON file path.</span></span>

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

### <span data-ttu-id="0e760-130">-Force</span><span class="sxs-lookup"><span data-stu-id="0e760-130">-Force</span></span>
<span data-ttu-id="0e760-131">Указывает на то, что этот командлет заменяет существующий конвейер без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0e760-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0e760-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e760-132">-Name</span></span>
<span data-ttu-id="0e760-133">Указывает имя создаваемого конвейера.</span><span class="sxs-lookup"><span data-stu-id="0e760-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="0e760-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e760-134">-ResourceGroupName</span></span>
<span data-ttu-id="0e760-135">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="0e760-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0e760-136">Этот командлет создает конвейер для группы, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0e760-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e760-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e760-137">-ResourceId</span></span>
<span data-ttu-id="0e760-138">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="0e760-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0e760-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e760-139">-Confirm</span></span>
<span data-ttu-id="0e760-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e760-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e760-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e760-141">-WhatIf</span></span>
<span data-ttu-id="0e760-142">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="0e760-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0e760-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e760-143">CommonParameters</span></span>
<span data-ttu-id="0e760-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e760-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e760-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e760-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e760-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e760-146">INPUTS</span></span>

### <span data-ttu-id="0e760-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0e760-147">System.String</span></span>

## <span data-ttu-id="0e760-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e760-148">OUTPUTS</span></span>

### <span data-ttu-id="0e760-149">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="0e760-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="0e760-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e760-150">NOTES</span></span>
<span data-ttu-id="0e760-151">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="0e760-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0e760-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e760-152">RELATED LINKS</span></span>

[<span data-ttu-id="0e760-153">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0e760-153">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0e760-154">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0e760-154">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0e760-155">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="0e760-155">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
