---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: bbcc33eee2932eed984f4cf06cfc09a79a1357af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721524"
---
# <span data-ttu-id="782fc-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="782fc-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="782fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="782fc-102">SYNOPSIS</span></span>
<span data-ttu-id="782fc-103">Получение сведений о конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="782fc-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="782fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="782fc-104">SYNTAX</span></span>

### <span data-ttu-id="782fc-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="782fc-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="782fc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="782fc-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="782fc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="782fc-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="782fc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="782fc-108">DESCRIPTION</span></span>
<span data-ttu-id="782fc-109">Командлет Get-AzDataFactoryV2Pipeline получает сведения о конвейерах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="782fc-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="782fc-110">Если вы задаете имя конвейера, этот командлет получает сведения об этом конвейере.</span><span class="sxs-lookup"><span data-stu-id="782fc-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="782fc-111">Если имя не задано, этот командлет получает сведения обо всех конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="782fc-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="782fc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="782fc-112">EXAMPLES</span></span>

### <span data-ttu-id="782fc-113">Пример 1: получение сведений обо всех каналах</span><span class="sxs-lookup"><span data-stu-id="782fc-113">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="782fc-114">Эта команда получает сведения обо всех конвейерах в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="782fc-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="782fc-115">Вы можете использовать один из приведенных ниже примеров команд.</span><span class="sxs-lookup"><span data-stu-id="782fc-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="782fc-116">Во втором используется объект фактов в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="782fc-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="782fc-117">Пример 2: получение сведений о конкретном конвейере</span><span class="sxs-lookup"><span data-stu-id="782fc-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="782fc-118">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="782fc-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="782fc-119">Команда передает эти данные командлету Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="782fc-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="782fc-120">Этот командлет Windows PowerShell форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="782fc-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="782fc-121">Чтобы получить дополнительные сведения, введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="782fc-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="782fc-122">Пример 3: получение свойств определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="782fc-122">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="782fc-123">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства Activitys, связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="782fc-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="782fc-124">Пример 6: получение сведений о входных данных для первого действия</span><span class="sxs-lookup"><span data-stu-id="782fc-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="782fc-125">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства Activitys, связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="782fc-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="782fc-126">Команда отображает свойство Inputs первого элемента массива "действия" с помощью командлета Format-List.</span><span class="sxs-lookup"><span data-stu-id="782fc-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="782fc-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="782fc-127">PARAMETERS</span></span>

### <span data-ttu-id="782fc-128">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="782fc-128">-DataFactory</span></span>
<span data-ttu-id="782fc-129">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="782fc-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="782fc-130">Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="782fc-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="782fc-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="782fc-131">-DataFactoryName</span></span>
<span data-ttu-id="782fc-132">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="782fc-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="782fc-133">Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="782fc-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="782fc-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782fc-134">-DefaultProfile</span></span>
<span data-ttu-id="782fc-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="782fc-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="782fc-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="782fc-136">-Name</span></span>
<span data-ttu-id="782fc-137">Указывает имя конвейера, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="782fc-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="782fc-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782fc-138">-ResourceGroupName</span></span>
<span data-ttu-id="782fc-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="782fc-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="782fc-140">Этот командлет получает конвейеры, принадлежащие к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="782fc-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="782fc-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="782fc-141">-ResourceId</span></span>
<span data-ttu-id="782fc-142">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="782fc-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="782fc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782fc-143">CommonParameters</span></span>
<span data-ttu-id="782fc-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="782fc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782fc-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="782fc-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782fc-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="782fc-146">INPUTS</span></span>

### <span data-ttu-id="782fc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="782fc-147">System.String</span></span>

### <span data-ttu-id="782fc-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="782fc-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="782fc-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="782fc-149">OUTPUTS</span></span>

### <span data-ttu-id="782fc-150">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="782fc-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="782fc-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="782fc-151">NOTES</span></span>
<span data-ttu-id="782fc-152">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="782fc-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="782fc-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="782fc-153">RELATED LINKS</span></span>

[<span data-ttu-id="782fc-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="782fc-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="782fc-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="782fc-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="782fc-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="782fc-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
