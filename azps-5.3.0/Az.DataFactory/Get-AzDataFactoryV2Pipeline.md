---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 6605fa005d8ca5c41c0ea60ee21a15c0196ae832
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518990"
---
# <span data-ttu-id="79534-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="79534-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="79534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79534-102">SYNOPSIS</span></span>
<span data-ttu-id="79534-103">Сведения о конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="79534-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="79534-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="79534-104">SYNTAX</span></span>

### <span data-ttu-id="79534-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79534-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79534-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="79534-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79534-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="79534-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79534-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79534-108">DESCRIPTION</span></span>
<span data-ttu-id="79534-109">Этот Get-AzDataFactoryV2Pipeline получает сведения о конвейерах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="79534-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="79534-110">Если указать имя конвейера, этот cmdlet получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="79534-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="79534-111">Если имя не указано, этот cmdlet получает сведения обо всех конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="79534-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="79534-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="79534-112">EXAMPLES</span></span>

### <span data-ttu-id="79534-113">Пример 1. Сведения обо всех конвейерах</span><span class="sxs-lookup"><span data-stu-id="79534-113">Example 1: Get information about all pipelines</span></span>
```powershell
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

<span data-ttu-id="79534-114">Эта команда получает сведения обо всех конвейерах в фабрике данных с именем ВикиADF.</span><span class="sxs-lookup"><span data-stu-id="79534-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="79534-115">Вы можете использовать одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="79534-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="79534-116">Во втором используется объект DataFactory в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="79534-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="79534-117">Пример 2. Просмотр сведений об определенном канале</span><span class="sxs-lookup"><span data-stu-id="79534-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="79534-118">Эта команда получает сведения о конвейере DPWikisample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="79534-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="79534-119">Эта команда передает эти сведения в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="79534-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="79534-120">Это Windows PowerShell форматирование результатов.</span><span class="sxs-lookup"><span data-stu-id="79534-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="79534-121">Для получения дополнительных сведений введите Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="79534-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="79534-122">Пример 3. Просмотр свойств для определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="79534-122">Example 3: Get the properties for a specific pipeline</span></span>
```powershell
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

<span data-ttu-id="79534-123">Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а затем использует стандартную точку для просмотра свойства "Действия", связанного с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="79534-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="79534-124">Пример 4. Просмотр сведений о вводе данных для первого действия</span><span class="sxs-lookup"><span data-stu-id="79534-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="79534-125">Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а затем использует стандартную точку для просмотра свойства "Действия", связанного с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="79534-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="79534-126">Команда отображает свойство Inputs первого элемента массива Activities с помощью Format-List командлета.</span><span class="sxs-lookup"><span data-stu-id="79534-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="79534-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79534-127">PARAMETERS</span></span>

### <span data-ttu-id="79534-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="79534-128">-DataFactory</span></span>
<span data-ttu-id="79534-129">Указывает объект PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="79534-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="79534-130">Этот cmdlet получает конвейеры, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="79534-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="79534-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="79534-131">-DataFactoryName</span></span>
<span data-ttu-id="79534-132">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="79534-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="79534-133">Этот cmdlet получает конвейеры, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="79534-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="79534-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79534-134">-DefaultProfile</span></span>
<span data-ttu-id="79534-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79534-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79534-136">-Name</span><span class="sxs-lookup"><span data-stu-id="79534-136">-Name</span></span>
<span data-ttu-id="79534-137">Название конвейера, сведения о котором нужно получить.</span><span class="sxs-lookup"><span data-stu-id="79534-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="79534-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79534-138">-ResourceGroupName</span></span>
<span data-ttu-id="79534-139">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="79534-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="79534-140">Этот cmdlet получает конвейеры, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="79534-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="79534-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79534-141">-ResourceId</span></span>
<span data-ttu-id="79534-142">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="79534-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="79534-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79534-143">CommonParameters</span></span>
<span data-ttu-id="79534-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79534-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79534-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79534-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79534-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79534-146">INPUTS</span></span>

### <span data-ttu-id="79534-147">System.String</span><span class="sxs-lookup"><span data-stu-id="79534-147">System.String</span></span>

### <span data-ttu-id="79534-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="79534-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="79534-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79534-149">OUTPUTS</span></span>

### <span data-ttu-id="79534-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="79534-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="79534-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="79534-151">NOTES</span></span>
<span data-ttu-id="79534-152">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="79534-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="79534-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79534-153">RELATED LINKS</span></span>

[<span data-ttu-id="79534-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="79534-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="79534-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="79534-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="79534-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="79534-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
