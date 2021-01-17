---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 34db93baa063961958bdd4422143fdbe82b5f6a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407983"
---
# <span data-ttu-id="1960b-101">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1960b-101">Set-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="1960b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1960b-102">SYNOPSIS</span></span>
<span data-ttu-id="1960b-103">Создает конвейер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="1960b-103">Creates a pipeline in Data Factory.</span></span>

## <span data-ttu-id="1960b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1960b-104">SYNTAX</span></span>

### <span data-ttu-id="1960b-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1960b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Pipeline [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1960b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1960b-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Pipeline [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1960b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1960b-107">DESCRIPTION</span></span>
<span data-ttu-id="1960b-108">С Set-AzDataFactoryV2Pipeline создается конвейер в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="1960b-108">The Set-AzDataFactoryV2Pipeline cmdlet creates a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="1960b-109">Если указать имя для конвейера, который уже существует, то перед заменой конвейера будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1960b-109">If you specify a name for a pipeline that already exists, the cmdlet prompts you for confirmation before it replaces the pipeline.</span></span>
<span data-ttu-id="1960b-110">При указании параметра Force вместо существующего конвейера не будет подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1960b-110">If you specify the Force parameter, the cmdlet replaces the existing pipeline without confirmation.</span></span>
<span data-ttu-id="1960b-111">Выполните эти действия в следующем порядке: создайте фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="1960b-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="1960b-112">-- Создание связанных служб.</span><span class="sxs-lookup"><span data-stu-id="1960b-112">-- Create linked services.</span></span>
<span data-ttu-id="1960b-113">— создание наборов данных.</span><span class="sxs-lookup"><span data-stu-id="1960b-113">-- Create datasets.</span></span>
<span data-ttu-id="1960b-114">— создать канал.</span><span class="sxs-lookup"><span data-stu-id="1960b-114">-- Create a pipeline.</span></span>
<span data-ttu-id="1960b-115">Если в фабрике данных уже существует канал с таким же именем, этот cmdlet запросит подтверждение перезаписи существующего конвейера с помощью нового.</span><span class="sxs-lookup"><span data-stu-id="1960b-115">If a pipeline with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing pipeline with the new pipeline.</span></span>
<span data-ttu-id="1960b-116">При подтверждении переописи существующего конвейера определение конвейера также заменяется.</span><span class="sxs-lookup"><span data-stu-id="1960b-116">If you confirm to overwrite the existing pipeline, the pipeline definition is also replaced.</span></span>

## <span data-ttu-id="1960b-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1960b-117">EXAMPLES</span></span>

### <span data-ttu-id="1960b-118">Пример 1. Создание конвейера</span><span class="sxs-lookup"><span data-stu-id="1960b-118">Example 1: Create a pipeline</span></span>
```
PS C:\> Set-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" -File "C:\DPWikisample.json"

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF11
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="1960b-119">Эта команда создает конвейер под названием DPWikisample в фабрике данных ADF.</span><span class="sxs-lookup"><span data-stu-id="1960b-119">This command creates a pipeline named DPWikisample in the data factory named ADF.</span></span>
<span data-ttu-id="1960b-120">Эта команда будет базой данных в канале, DPWikisample.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="1960b-120">The command bases the pipeline on information in the DPWikisample.json file.</span></span>
<span data-ttu-id="1960b-121">Этот файл содержит сведения о действиях, таких как копирование и HDInsight в конвейере.</span><span class="sxs-lookup"><span data-stu-id="1960b-121">This file includes information about activities such as Copy Activity and HDInsight Activity in the pipeline.</span></span>

## <span data-ttu-id="1960b-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1960b-122">PARAMETERS</span></span>

### <span data-ttu-id="1960b-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1960b-123">-DataFactoryName</span></span>
<span data-ttu-id="1960b-124">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="1960b-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1960b-125">Этот cmdlet создает канал для фабрики данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1960b-125">This cmdlet creates a pipeline for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1960b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1960b-126">-DefaultProfile</span></span>
<span data-ttu-id="1960b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1960b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1960b-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="1960b-128">-DefinitionFile</span></span>
<span data-ttu-id="1960b-129">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="1960b-129">The JSON file path.</span></span>

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

### <span data-ttu-id="1960b-130">-Force</span><span class="sxs-lookup"><span data-stu-id="1960b-130">-Force</span></span>
<span data-ttu-id="1960b-131">Указывает на то, что этот cmdlet заменяет существующий канал без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1960b-131">Indicates that this cmdlet replaces an existing pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1960b-132">-Name</span><span class="sxs-lookup"><span data-stu-id="1960b-132">-Name</span></span>
<span data-ttu-id="1960b-133">Указывает имя созда создаемого конвейера.</span><span class="sxs-lookup"><span data-stu-id="1960b-133">Specifies the name of the pipeline to create.</span></span>

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

### <span data-ttu-id="1960b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1960b-134">-ResourceGroupName</span></span>
<span data-ttu-id="1960b-135">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1960b-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1960b-136">Этот cmdlet создает канал для группы, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="1960b-136">This cmdlet creates a pipeline for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1960b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1960b-137">-ResourceId</span></span>
<span data-ttu-id="1960b-138">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="1960b-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1960b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1960b-139">-Confirm</span></span>
<span data-ttu-id="1960b-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1960b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1960b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1960b-141">-WhatIf</span></span>
<span data-ttu-id="1960b-142">Показывает, что происходит, если выполняется только запуск, но не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1960b-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1960b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1960b-143">CommonParameters</span></span>
<span data-ttu-id="1960b-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1960b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1960b-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1960b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1960b-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1960b-146">INPUTS</span></span>

### <span data-ttu-id="1960b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="1960b-147">System.String</span></span>

## <span data-ttu-id="1960b-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1960b-148">OUTPUTS</span></span>

### <span data-ttu-id="1960b-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="1960b-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="1960b-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1960b-150">NOTES</span></span>
<span data-ttu-id="1960b-151">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="1960b-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1960b-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1960b-152">RELATED LINKS</span></span>

[<span data-ttu-id="1960b-153">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1960b-153">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="1960b-154">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1960b-154">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="1960b-155">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="1960b-155">Invoke-AzDataFactoryV2Pipeline</span></span>]()
