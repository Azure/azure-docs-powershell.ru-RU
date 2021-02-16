---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242824"
---
# <span data-ttu-id="23a85-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="23a85-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="23a85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23a85-102">SYNOPSIS</span></span>
<span data-ttu-id="23a85-103">Получает срезы данных для наборов данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="23a85-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="23a85-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23a85-104">SYNTAX</span></span>

### <span data-ttu-id="23a85-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23a85-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23a85-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="23a85-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23a85-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23a85-107">DESCRIPTION</span></span>
<span data-ttu-id="23a85-108">Для наборов данных в фабрике данных Azure срезы получаются срезами для **get-AzDataFactorySlice.**</span><span class="sxs-lookup"><span data-stu-id="23a85-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="23a85-109">Укажите время начала и время окончания для определения диапазона срезов данных, которые нужно просмотреть.</span><span class="sxs-lookup"><span data-stu-id="23a85-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="23a85-110">Состояние среза данных — одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="23a85-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="23a85-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="23a85-111">PendingExecution.</span></span>
<span data-ttu-id="23a85-112">Обработка данных не начата.</span><span class="sxs-lookup"><span data-stu-id="23a85-112">Data processing has not started.</span></span> 
- <span data-ttu-id="23a85-113">InProgress.</span><span class="sxs-lookup"><span data-stu-id="23a85-113">InProgress.</span></span>
<span data-ttu-id="23a85-114">Идет обработка данных.</span><span class="sxs-lookup"><span data-stu-id="23a85-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="23a85-115">"Готово".</span><span class="sxs-lookup"><span data-stu-id="23a85-115">Ready.</span></span>
<span data-ttu-id="23a85-116">Обработка данных завершена.</span><span class="sxs-lookup"><span data-stu-id="23a85-116">Data processing is completed.</span></span>
<span data-ttu-id="23a85-117">Срез данных готов к обработке зависимых срезов.</span><span class="sxs-lookup"><span data-stu-id="23a85-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="23a85-118">Не удалось.</span><span class="sxs-lookup"><span data-stu-id="23a85-118">Failed.</span></span>
<span data-ttu-id="23a85-119">Сбой запуска среза.</span><span class="sxs-lookup"><span data-stu-id="23a85-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="23a85-120">Пропустить.</span><span class="sxs-lookup"><span data-stu-id="23a85-120">Skip.</span></span>
<span data-ttu-id="23a85-121">Фабрика данных пропускает обработку среза.</span><span class="sxs-lookup"><span data-stu-id="23a85-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="23a85-122">Повторить.</span><span class="sxs-lookup"><span data-stu-id="23a85-122">Retry.</span></span>
<span data-ttu-id="23a85-123">Фабрика данных искомый запуск, который создает срез.</span><span class="sxs-lookup"><span data-stu-id="23a85-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="23a85-124">"По времени". Обработка данных уже из-за времени.</span><span class="sxs-lookup"><span data-stu-id="23a85-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="23a85-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="23a85-125">PendingValidation.</span></span>
<span data-ttu-id="23a85-126">Срез данных ожидает проверки перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="23a85-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="23a85-127">Повторить проверку.</span><span class="sxs-lookup"><span data-stu-id="23a85-127">Retry Validation.</span></span>
<span data-ttu-id="23a85-128">Фабрика данных искомые проверки для среза.</span><span class="sxs-lookup"><span data-stu-id="23a85-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="23a85-129">Сбой проверки.</span><span class="sxs-lookup"><span data-stu-id="23a85-129">Failed Validation.</span></span>
<span data-ttu-id="23a85-130">Сбой проверки среза.</span><span class="sxs-lookup"><span data-stu-id="23a85-130">Validation of the slice failed.</span></span>
<span data-ttu-id="23a85-131">Для каждого из срезов можно получить дополнительные сведения о запуске, который создается с помощью Get-AzDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="23a85-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="23a85-132">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23a85-132">EXAMPLES</span></span>

### <span data-ttu-id="23a85-133">Пример 1. Получить срезы данных для наборов данных</span><span class="sxs-lookup"><span data-stu-id="23a85-133">Example 1: Get data slices for a dataset</span></span>
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="23a85-134">Эта команда получает все срезы данных для наборов данных WikiAggregatedData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="23a85-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="23a85-135">Эта команда получает отрезки, которые были произведены после времени, заданного параметром StartDateTime.</span><span class="sxs-lookup"><span data-stu-id="23a85-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="23a85-136">В следующем примере код задает доступность для этого набора данных каждый час в файле нотации объектов JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="23a85-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="23a85-137">доступность: { период: "Hour", periodMultiplier: 1 } Некоторые результаты готовы, а другие — PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="23a85-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="23a85-138">Готовые срезы уже работают.</span><span class="sxs-lookup"><span data-stu-id="23a85-138">Ready slices have already run.</span></span>
<span data-ttu-id="23a85-139">В конце каждого часа в интервале, указанном Set-AzDataFactoryPipelineActivePeriod, ожидается запуск срезов, ожидающих запуска.</span><span class="sxs-lookup"><span data-stu-id="23a85-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="23a85-140">В этом примере для начала и окончания периодов в конвейере и на срезе значение одного дня (24 часа).</span><span class="sxs-lookup"><span data-stu-id="23a85-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="23a85-141">Пример 2</span><span class="sxs-lookup"><span data-stu-id="23a85-141">Example 2</span></span>

<span data-ttu-id="23a85-142">Получает срезы данных для наборов данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="23a85-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="23a85-143">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="23a85-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="23a85-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23a85-144">PARAMETERS</span></span>

### <span data-ttu-id="23a85-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="23a85-145">-DataFactory</span></span>
<span data-ttu-id="23a85-146">Указывает объект **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="23a85-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="23a85-147">Этот cmdlet получает срезы, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="23a85-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="23a85-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="23a85-148">-DataFactoryName</span></span>
<span data-ttu-id="23a85-149">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="23a85-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="23a85-150">Этот cmdlet получает срезы, которые относятся к фабрике данных, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="23a85-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="23a85-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="23a85-151">-DatasetName</span></span>
<span data-ttu-id="23a85-152">Определяет имя наборов данных, для которых этот cmdlet получает срезы.</span><span class="sxs-lookup"><span data-stu-id="23a85-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a85-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a85-153">-DefaultProfile</span></span>
<span data-ttu-id="23a85-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="23a85-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23a85-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="23a85-155">-EndDateTime</span></span>
<span data-ttu-id="23a85-156">Окончание периода времени в качестве объекта **даты и** времени.</span><span class="sxs-lookup"><span data-stu-id="23a85-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="23a85-157">Этот cmdlet получает отрезки, произведенные до времени, заданного для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="23a85-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="23a85-158">Чтобы получить дополнительные сведения об **объектах даты и времени,** введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="23a85-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="23a85-159">В формате ISO8601 необходимо указать *endDateTime,* как в следующих примерах: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (тихоокеанское время) По умолчанию часовой пояс имеет значение UTC.</span><span class="sxs-lookup"><span data-stu-id="23a85-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a85-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23a85-160">-ResourceGroupName</span></span>
<span data-ttu-id="23a85-161">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="23a85-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="23a85-162">Этот cmdlet получает срезы, которые относятся к группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="23a85-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="23a85-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="23a85-163">-StartDateTime</span></span>
<span data-ttu-id="23a85-164">Начало периода времени в качестве объекта **даты и** времени.</span><span class="sxs-lookup"><span data-stu-id="23a85-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="23a85-165">Этот cmdlet получает срезы, произведенные после времени, заданного для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="23a85-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a85-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a85-166">CommonParameters</span></span>
<span data-ttu-id="23a85-167">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a85-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a85-168">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a85-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a85-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23a85-169">INPUTS</span></span>

### <span data-ttu-id="23a85-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="23a85-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="23a85-171">System.String</span><span class="sxs-lookup"><span data-stu-id="23a85-171">System.String</span></span>

## <span data-ttu-id="23a85-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23a85-172">OUTPUTS</span></span>

### <span data-ttu-id="23a85-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="23a85-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="23a85-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23a85-174">NOTES</span></span>
* <span data-ttu-id="23a85-175">Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="23a85-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="23a85-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23a85-176">RELATED LINKS</span></span>

[<span data-ttu-id="23a85-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="23a85-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="23a85-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="23a85-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="23a85-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="23a85-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


