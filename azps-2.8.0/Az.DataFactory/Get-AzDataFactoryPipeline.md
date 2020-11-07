---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 2f08d81820ab28688b645ef3ec6a8f519985585c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721546"
---
# <span data-ttu-id="778eb-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="778eb-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="778eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="778eb-102">SYNOPSIS</span></span>
<span data-ttu-id="778eb-103">Получение сведений о конвейерах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="778eb-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="778eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="778eb-104">SYNTAX</span></span>

### <span data-ttu-id="778eb-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="778eb-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="778eb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="778eb-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="778eb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="778eb-107">DESCRIPTION</span></span>
<span data-ttu-id="778eb-108">Командлет **Get-AzDataFactoryPipeline** получает сведения о конвейерах в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="778eb-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="778eb-109">Если вы задаете имя конвейера, этот командлет получает сведения об этом конвейере.</span><span class="sxs-lookup"><span data-stu-id="778eb-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="778eb-110">Если имя не задано, этот командлет получает сведения обо всех конвейерах в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="778eb-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="778eb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="778eb-111">EXAMPLES</span></span>

### <span data-ttu-id="778eb-112">Пример 1: получение сведений обо всех каналах</span><span class="sxs-lookup"><span data-stu-id="778eb-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="778eb-113">Эта команда получает сведения обо всех конвейерах в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="778eb-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="778eb-114">Вы можете выполнить одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="778eb-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="778eb-115">Во втором используется объект **фактов** в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="778eb-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="778eb-116">Пример 2: получение сведений о конкретном конвейере</span><span class="sxs-lookup"><span data-stu-id="778eb-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="778eb-117">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="778eb-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="778eb-118">Команда передает эти данные командлету Format-List с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="778eb-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="778eb-119">Этот командлет форматирует результаты.</span><span class="sxs-lookup"><span data-stu-id="778eb-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="778eb-120">Для получения дополнительных сведений введите `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="778eb-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="778eb-121">Пример 3: получение свойств определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="778eb-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="778eb-122">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF и использует стандартную нотацию для просмотра свойства **Properties** , связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="778eb-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="778eb-123">Пример 4: получение действий для определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="778eb-123">Example 4: Get the activities for a specific pipeline</span></span>
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

<span data-ttu-id="778eb-124">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства **activitys** , связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="778eb-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="778eb-125">Пример 5: получение сведений о среде выполнения для определенного конвейера</span><span class="sxs-lookup"><span data-stu-id="778eb-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="778eb-126">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF и использует стандартную нотацию для просмотра свойства **RuntimeInfo** , связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="778eb-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="778eb-127">Пример 6: получение сведений о входных данных для первого действия</span><span class="sxs-lookup"><span data-stu-id="778eb-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="778eb-128">Эта команда получает сведения о конвейере с именем DPWikisample в фабрике данных с именем WikiADF, а затем использует стандартную нотацию для просмотра свойства **activitys** , связанного с этим конвейером.</span><span class="sxs-lookup"><span data-stu-id="778eb-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="778eb-129">Команда отображает свойство **Inputs** первого элемента массива " **действия** " с помощью **Format-List**.</span><span class="sxs-lookup"><span data-stu-id="778eb-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="778eb-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="778eb-130">PARAMETERS</span></span>

### <span data-ttu-id="778eb-131">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="778eb-131">-DataFactory</span></span>
<span data-ttu-id="778eb-132">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="778eb-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="778eb-133">Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="778eb-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="778eb-134">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="778eb-134">-DataFactoryName</span></span>
<span data-ttu-id="778eb-135">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="778eb-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="778eb-136">Этот командлет получает конвейеры, которые принадлежат к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="778eb-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="778eb-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778eb-137">-DefaultProfile</span></span>
<span data-ttu-id="778eb-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="778eb-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="778eb-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="778eb-139">-Name</span></span>
<span data-ttu-id="778eb-140">Указывает имя конвейера, сведения о котором требуется получить.</span><span class="sxs-lookup"><span data-stu-id="778eb-140">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="778eb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778eb-141">-ResourceGroupName</span></span>
<span data-ttu-id="778eb-142">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="778eb-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="778eb-143">Этот командлет получает конвейеры, принадлежащие к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="778eb-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="778eb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778eb-144">CommonParameters</span></span>
<span data-ttu-id="778eb-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="778eb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778eb-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="778eb-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778eb-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="778eb-147">INPUTS</span></span>

### <span data-ttu-id="778eb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="778eb-148">System.String</span></span>

### <span data-ttu-id="778eb-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="778eb-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="778eb-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="778eb-150">OUTPUTS</span></span>

### <span data-ttu-id="778eb-151">Microsoft. Azure. Commands. Factoring. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="778eb-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="778eb-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="778eb-152">NOTES</span></span>
* <span data-ttu-id="778eb-153">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="778eb-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="778eb-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="778eb-154">RELATED LINKS</span></span>

[<span data-ttu-id="778eb-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="778eb-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="778eb-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="778eb-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="778eb-157">Возобновить — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="778eb-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="778eb-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="778eb-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="778eb-159">Приостановить — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="778eb-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


