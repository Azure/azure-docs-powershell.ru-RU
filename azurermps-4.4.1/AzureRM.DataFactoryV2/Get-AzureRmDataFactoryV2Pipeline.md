---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: b8065c3b4aa958c9138316488b7ca8a9b982d97c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569560"
---
# <span data-ttu-id="16440-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="16440-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="16440-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16440-102">SYNOPSIS</span></span>
<span data-ttu-id="16440-103">Получение сведений о конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="16440-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16440-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16440-104">SYNTAX</span></span>

### <span data-ttu-id="16440-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16440-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="16440-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="16440-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="16440-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16440-107">DESCRIPTION</span></span>
<span data-ttu-id="16440-108">Командлет Get-AzureRmDataFactoryV2Pipeline получает сведения о конвейерах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="16440-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="16440-109">Если вы задаете имя конвейера, этот командлет получает сведения об этом конвейере.</span><span class="sxs-lookup"><span data-stu-id="16440-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="16440-110">Если имя не задано, этот командлет получает сведения обо всех конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="16440-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="16440-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16440-111">EXAMPLES</span></span>

### <span data-ttu-id="16440-112">Пример 1: получение сведений обо всех каналах</span><span class="sxs-lookup"><span data-stu-id="16440-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="16440-113">Эта команда получает сведения обо всех конвейерах в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="16440-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="16440-114">Вы можете использовать один из приведенных ниже примеров команд.</span><span class="sxs-lookup"><span data-stu-id="16440-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="16440-115">Во втором используется объект фактов в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="16440-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="16440-116">Пример 2: получение сведений о конкретном конвейере</span><span class="sxs-lookup"><span data-stu-id="16440-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="16440-117">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="16440-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="16440-118">Команда передает эти данные командлету Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="16440-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="16440-119">Этот командлет Windows PowerShell форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="16440-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="16440-120">Чтобы получить дополнительные сведения, введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="16440-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="16440-121">Пример 3: получение свойств определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="16440-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}

```

<span data-ttu-id="16440-122">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства Activitys, связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="16440-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="16440-123">Пример 6: получение сведений о входных данных для первого действия</span><span class="sxs-lookup"><span data-stu-id="16440-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :

```

<span data-ttu-id="16440-124">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства Activitys, связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="16440-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="16440-125">Команда отображает свойство Inputs первого элемента массива "действия" с помощью командлета Format-List.</span><span class="sxs-lookup"><span data-stu-id="16440-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="16440-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16440-126">PARAMETERS</span></span>

### <span data-ttu-id="16440-127">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="16440-127">-DataFactory</span></span>
<span data-ttu-id="16440-128">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="16440-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="16440-129">Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16440-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16440-130">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="16440-130">-DataFactoryName</span></span>
<span data-ttu-id="16440-131">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="16440-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="16440-132">Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16440-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16440-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16440-133">-Name</span></span>
<span data-ttu-id="16440-134">Указывает имя конвейера, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="16440-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16440-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16440-135">-ResourceGroupName</span></span>
<span data-ttu-id="16440-136">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="16440-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="16440-137">Этот командлет получает конвейеры, принадлежащие к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="16440-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="16440-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16440-138">INPUTS</span></span>

### <span data-ttu-id="16440-139">System. String</span><span class="sxs-lookup"><span data-stu-id="16440-139">System.String</span></span>
<span data-ttu-id="16440-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="16440-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="16440-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16440-141">OUTPUTS</span></span>

### <span data-ttu-id="16440-142">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="16440-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="16440-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="16440-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="16440-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="16440-144">NOTES</span></span>
<span data-ttu-id="16440-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="16440-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="16440-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16440-146">RELATED LINKS</span></span>
[<span data-ttu-id="16440-147">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="16440-147">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="16440-148">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="16440-148">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="16440-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="16440-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
