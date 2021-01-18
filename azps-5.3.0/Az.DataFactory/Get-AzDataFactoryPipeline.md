---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508549"
---
# <span data-ttu-id="6526d-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6526d-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="6526d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6526d-102">SYNOPSIS</span></span>
<span data-ttu-id="6526d-103">Сведения о конвейерах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="6526d-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="6526d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6526d-104">SYNTAX</span></span>

### <span data-ttu-id="6526d-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6526d-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6526d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6526d-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6526d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6526d-107">DESCRIPTION</span></span>
<span data-ttu-id="6526d-108">**Cmdlet Get-AzDataFactoryPipeline** получает сведения о конвейерах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="6526d-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="6526d-109">Если указать имя конвейера, этот cmdlet получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="6526d-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="6526d-110">Если имя не указано, этот cmdlet получает сведения обо всех конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="6526d-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="6526d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6526d-111">EXAMPLES</span></span>

### <span data-ttu-id="6526d-112">Пример 1. Сведения обо всех конвейерах</span><span class="sxs-lookup"><span data-stu-id="6526d-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="6526d-113">Эта команда получает сведения обо всех конвейерах в фабрике данных с именем ВикиADF.</span><span class="sxs-lookup"><span data-stu-id="6526d-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="6526d-114">Вы можете использовать одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="6526d-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="6526d-115">Во втором используется объект **DataFactory** в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="6526d-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="6526d-116">Пример 2. Просмотр сведений об определенном канале</span><span class="sxs-lookup"><span data-stu-id="6526d-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="6526d-117">Эта команда получает сведения о конвейере DPWikisample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="6526d-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="6526d-118">Эта команда передает эти сведения в командлет Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="6526d-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6526d-119">Этот cmdlet formats the results (Форматирование результатов).</span><span class="sxs-lookup"><span data-stu-id="6526d-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="6526d-120">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="6526d-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="6526d-121">Пример 3. Просмотр свойств для определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="6526d-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="6526d-122">Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а затем использует стандартную точку для просмотра свойства **Properties,** связанного с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="6526d-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="6526d-123">Пример 4. Просмотр действий для определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="6526d-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="6526d-124">Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а  затем использует стандартную точку для просмотра свойства "Действия", связанного с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="6526d-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="6526d-125">Пример 5. Просмотр сведений о времени запуска для определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="6526d-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="6526d-126">Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а затем использует стандартную точку для просмотра свойства **RuntimeInfo,** связанного с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="6526d-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="6526d-127">Пример 6. Просмотр сведений о вводе данных для первого действия</span><span class="sxs-lookup"><span data-stu-id="6526d-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="6526d-128">Эта команда получает сведения о конвейере DPWikisample в фабрике данных WikiADF, а  затем использует стандартную точку для просмотра свойства "Действия", связанного с этим каналом.</span><span class="sxs-lookup"><span data-stu-id="6526d-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="6526d-129">Команда отображает свойство **Inputs** первого элемента массива **Activities** с помощью **Format-List.**</span><span class="sxs-lookup"><span data-stu-id="6526d-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="6526d-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6526d-130">PARAMETERS</span></span>

### <span data-ttu-id="6526d-131">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6526d-131">-DataFactory</span></span>
<span data-ttu-id="6526d-132">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="6526d-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6526d-133">Этот cmdlet получает конвейеры, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6526d-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6526d-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6526d-134">-DataFactoryName</span></span>
<span data-ttu-id="6526d-135">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="6526d-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6526d-136">Этот cmdlet получает конвейеры, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6526d-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6526d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6526d-137">-DefaultProfile</span></span>
<span data-ttu-id="6526d-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6526d-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6526d-139">-Name</span><span class="sxs-lookup"><span data-stu-id="6526d-139">-Name</span></span>
<span data-ttu-id="6526d-140">Название конвейера, сведения о котором нужно получить.</span><span class="sxs-lookup"><span data-stu-id="6526d-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="6526d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6526d-141">-ResourceGroupName</span></span>
<span data-ttu-id="6526d-142">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6526d-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6526d-143">Этот cmdlet получает конвейеры, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="6526d-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6526d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6526d-144">CommonParameters</span></span>
<span data-ttu-id="6526d-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6526d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6526d-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6526d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6526d-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6526d-147">INPUTS</span></span>

### <span data-ttu-id="6526d-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6526d-148">System.String</span></span>

### <span data-ttu-id="6526d-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6526d-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="6526d-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6526d-150">OUTPUTS</span></span>

### <span data-ttu-id="6526d-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="6526d-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="6526d-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6526d-152">NOTES</span></span>
* <span data-ttu-id="6526d-153">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="6526d-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6526d-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6526d-154">RELATED LINKS</span></span>

[<span data-ttu-id="6526d-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6526d-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="6526d-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6526d-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="6526d-157">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6526d-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="6526d-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="6526d-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="6526d-159">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6526d-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


