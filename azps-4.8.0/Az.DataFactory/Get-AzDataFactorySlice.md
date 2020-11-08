---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236804"
---
# <span data-ttu-id="98a01-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="98a01-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="98a01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98a01-102">SYNOPSIS</span></span>
<span data-ttu-id="98a01-103">Получает срезы данных для набора данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="98a01-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="98a01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98a01-104">SYNTAX</span></span>

### <span data-ttu-id="98a01-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98a01-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98a01-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="98a01-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98a01-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98a01-107">DESCRIPTION</span></span>
<span data-ttu-id="98a01-108">Командлет **Get-AzDataFactorySlice** получает срезы данных для набора данных в службе фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="98a01-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="98a01-109">Укажите время начала и время окончания, чтобы определить диапазон срезов данных для просмотра.</span><span class="sxs-lookup"><span data-stu-id="98a01-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="98a01-110">Состояние среза данных — одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="98a01-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="98a01-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="98a01-111">PendingExecution.</span></span>
<span data-ttu-id="98a01-112">Обработка данных не начата.</span><span class="sxs-lookup"><span data-stu-id="98a01-112">Data processing has not started.</span></span> 
- <span data-ttu-id="98a01-113">Выполняется.</span><span class="sxs-lookup"><span data-stu-id="98a01-113">InProgress.</span></span>
<span data-ttu-id="98a01-114">Выполняется обработка данных.</span><span class="sxs-lookup"><span data-stu-id="98a01-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="98a01-115">Начать.</span><span class="sxs-lookup"><span data-stu-id="98a01-115">Ready.</span></span>
<span data-ttu-id="98a01-116">Обработка данных завершена.</span><span class="sxs-lookup"><span data-stu-id="98a01-116">Data processing is completed.</span></span>
<span data-ttu-id="98a01-117">Срез данных готов к зависимым сегментам, чтобы использовать его.</span><span class="sxs-lookup"><span data-stu-id="98a01-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="98a01-118">Ошибкой.</span><span class="sxs-lookup"><span data-stu-id="98a01-118">Failed.</span></span>
<span data-ttu-id="98a01-119">Не удалось выполнить вызов, создающий срез.</span><span class="sxs-lookup"><span data-stu-id="98a01-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="98a01-120">Пуст.</span><span class="sxs-lookup"><span data-stu-id="98a01-120">Skip.</span></span>
<span data-ttu-id="98a01-121">Фабрика данных пропускает обработку среза.</span><span class="sxs-lookup"><span data-stu-id="98a01-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="98a01-122">Повторить.</span><span class="sxs-lookup"><span data-stu-id="98a01-122">Retry.</span></span>
<span data-ttu-id="98a01-123">Фабрика данных повторяет запуск, создающий срез.</span><span class="sxs-lookup"><span data-stu-id="98a01-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="98a01-124">Время ожидания истекло. Превышено время ожидания обработки данных.</span><span class="sxs-lookup"><span data-stu-id="98a01-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="98a01-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="98a01-125">PendingValidation.</span></span>
<span data-ttu-id="98a01-126">Срез данных ожидает подтверждения перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="98a01-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="98a01-127">Повторите проверку.</span><span class="sxs-lookup"><span data-stu-id="98a01-127">Retry Validation.</span></span>
<span data-ttu-id="98a01-128">Фабрика данных повторяет проверку среза.</span><span class="sxs-lookup"><span data-stu-id="98a01-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="98a01-129">Проверка не удалась.</span><span class="sxs-lookup"><span data-stu-id="98a01-129">Failed Validation.</span></span>
<span data-ttu-id="98a01-130">Проверка среза завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="98a01-130">Validation of the slice failed.</span></span>
<span data-ttu-id="98a01-131">Для каждого сектора вы можете просмотреть дополнительные сведения о запуске, который создает срез с помощью командлета Get-AzDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="98a01-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="98a01-132">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98a01-132">EXAMPLES</span></span>

### <span data-ttu-id="98a01-133">Пример 1: получение срезов данных для набора данных</span><span class="sxs-lookup"><span data-stu-id="98a01-133">Example 1: Get data slices for a dataset</span></span>
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

<span data-ttu-id="98a01-134">Эта команда получает все срезы данных для набора данных с именем WikiAggregatedData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="98a01-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="98a01-135">Команда получает срезы, созданные после того, как указан параметр StartDateTime.</span><span class="sxs-lookup"><span data-stu-id="98a01-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="98a01-136">Следующий пример кода задает доступность для этого набора данных каждый час в файле нотации JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="98a01-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="98a01-137">доступность: {period: "Hour"; periodMultiplier: 1} некоторые результаты готовы, а другие — PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="98a01-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="98a01-138">Готовые срезы уже запущены.</span><span class="sxs-lookup"><span data-stu-id="98a01-138">Ready slices have already run.</span></span>
<span data-ttu-id="98a01-139">Ожидающие отрезки выполняются в конце каждого часа в интервале, указанном в командлете Set-AzDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="98a01-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="98a01-140">В этом примере начальные и конечные периоды для конвейера и среза имеют значение один день (24 часа).</span><span class="sxs-lookup"><span data-stu-id="98a01-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="98a01-141">Пример 2</span><span class="sxs-lookup"><span data-stu-id="98a01-141">Example 2</span></span>

<span data-ttu-id="98a01-142">Получает срезы данных для набора данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="98a01-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="98a01-143">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="98a01-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="98a01-144">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98a01-144">PARAMETERS</span></span>

### <span data-ttu-id="98a01-145">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="98a01-145">-DataFactory</span></span>
<span data-ttu-id="98a01-146">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="98a01-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="98a01-147">Этот командлет получает срезы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="98a01-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98a01-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="98a01-148">-DataFactoryName</span></span>
<span data-ttu-id="98a01-149">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="98a01-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="98a01-150">Этот командлет получает срезы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="98a01-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="98a01-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="98a01-151">-DatasetName</span></span>
<span data-ttu-id="98a01-152">Указывает имя набора данных, для которого этот командлет получает срезы.</span><span class="sxs-lookup"><span data-stu-id="98a01-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="98a01-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a01-153">-DefaultProfile</span></span>
<span data-ttu-id="98a01-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="98a01-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98a01-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="98a01-155">-EndDateTime</span></span>
<span data-ttu-id="98a01-156">Указывает конец периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="98a01-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="98a01-157">Этот командлет получает срезы, созданные до того момента, когда этот параметр указан.</span><span class="sxs-lookup"><span data-stu-id="98a01-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="98a01-158">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="98a01-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="98a01-159">*EndDateTime* должен быть указан в формате ISO8601, как показано в следующих примерах: 2015-01-01Z 2015-01-01T00:00-1-01:00Z 1:00:01T00 z (UTC) 2015-0,01-: 00.00 – 8 – 00.000</span><span class="sxs-lookup"><span data-stu-id="98a01-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="98a01-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98a01-160">-ResourceGroupName</span></span>
<span data-ttu-id="98a01-161">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="98a01-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="98a01-162">Этот командлет получает срезы, которые относятся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="98a01-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="98a01-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="98a01-163">-StartDateTime</span></span>
<span data-ttu-id="98a01-164">Задает начало периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="98a01-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="98a01-165">Этот командлет получает срезы, созданные после того, как указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="98a01-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="98a01-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a01-166">CommonParameters</span></span>
<span data-ttu-id="98a01-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98a01-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a01-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a01-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a01-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98a01-169">INPUTS</span></span>

### <span data-ttu-id="98a01-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="98a01-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="98a01-171">System. String</span><span class="sxs-lookup"><span data-stu-id="98a01-171">System.String</span></span>

## <span data-ttu-id="98a01-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98a01-172">OUTPUTS</span></span>

### <span data-ttu-id="98a01-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="98a01-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="98a01-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="98a01-174">NOTES</span></span>
* <span data-ttu-id="98a01-175">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="98a01-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="98a01-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98a01-176">RELATED LINKS</span></span>

[<span data-ttu-id="98a01-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="98a01-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="98a01-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="98a01-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="98a01-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="98a01-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

