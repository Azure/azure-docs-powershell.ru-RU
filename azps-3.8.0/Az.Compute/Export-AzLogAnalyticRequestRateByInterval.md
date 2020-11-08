---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/export-azloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Export-AzLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: 90b467ccd046bf7d08b9faff4c03dcc858ae0076
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074651"
---
# <span data-ttu-id="fef18-101">Export-AzLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="fef18-101">Export-AzLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="fef18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fef18-102">SYNOPSIS</span></span>
<span data-ttu-id="fef18-103">Экспортируйте журналы, в которых на заданном временном экране отображаются запросы API, сделанные данной подпиской, чтобы показать действия по регулированию.</span><span class="sxs-lookup"><span data-stu-id="fef18-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

## <span data-ttu-id="fef18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fef18-104">SYNTAX</span></span>

```
Export-AzLogAnalyticRequestRateByInterval [-Location] <String> [-FromTime] <DateTime> [-ToTime] <DateTime>
 [-BlobContainerSasUri] <String> [-IntervalLength] <IntervalInMins> [-GroupByOperationName]
 [-GroupByResourceName] [-GroupByThrottlePolicy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fef18-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fef18-105">DESCRIPTION</span></span>
<span data-ttu-id="fef18-106">Экспортируются статистические данные о вызовах подписки на API Microsoft. COMPUTE при успешном завершении, отказе или состоянии регулирования, в предопределенных интервалах времени.</span><span class="sxs-lookup"><span data-stu-id="fef18-106">Exports statistical data about the subscription's calls to the Microsoft.Compute API by Success, Failure, or Throttled status, in predefined time intervals.</span></span> <span data-ttu-id="fef18-107">Журналы можно дополнительно сгруппировать по трем параметрам: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="fef18-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="fef18-108">Обратите внимание, что этот командлет собирает только журналы вычислительных поставщиков ресурсов; Кроме того, данные о типах ресурсов "диск" и "снимок" пока недоступны.</span><span class="sxs-lookup"><span data-stu-id="fef18-108">Note that this cmdlet collects only Compute Resource Provider logs; moreover, data about the Disk and Snapshot resource types is not yet available.</span></span>

<span data-ttu-id="fef18-109">Общие сведения о регулировании API поставщика ресурсов вычислительной среды содержатся в разделе https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits .</span><span class="sxs-lookup"><span data-stu-id="fef18-109">For an overview of the Compute Resource Provider's API throttling, see https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits.</span></span> 

## <span data-ttu-id="fef18-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fef18-110">EXAMPLES</span></span>

### <span data-ttu-id="fef18-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fef18-111">Example 1</span></span>
```
PS C:\> Export-AzLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="fef18-112">Эта команда хранит объединенные числа вызовов API Microsoft. COMPUTE, разделенных на успех, сбой или отрегулированный интервал между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в указанном URI SAS, агрегированный по имени операции.</span><span class="sxs-lookup"><span data-stu-id="fef18-112">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="fef18-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fef18-113">PARAMETERS</span></span>

### <span data-ttu-id="fef18-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fef18-114">-AsJob</span></span>
<span data-ttu-id="fef18-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fef18-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fef18-116">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="fef18-116">-BlobContainerSasUri</span></span>
<span data-ttu-id="fef18-117">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов для ведения журнала, на который LogAnalytics API записывает выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="fef18-117">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef18-118">-DefaultProfile</span></span>
<span data-ttu-id="fef18-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fef18-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fef18-120">-FromTime</span><span class="sxs-lookup"><span data-stu-id="fef18-120">-FromTime</span></span>
<span data-ttu-id="fef18-121">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="fef18-121">From time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef18-122">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="fef18-122">-GroupByOperationName</span></span>
<span data-ttu-id="fef18-123">Результат запроса группировки по имени операции.</span><span class="sxs-lookup"><span data-stu-id="fef18-123">Group query result by Operation Name.</span></span>

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

### <span data-ttu-id="fef18-124">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="fef18-124">-GroupByResourceName</span></span>
<span data-ttu-id="fef18-125">Результат запроса Group по названию ресурса.</span><span class="sxs-lookup"><span data-stu-id="fef18-125">Group query result by Resource Name.</span></span>

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

### <span data-ttu-id="fef18-126">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="fef18-126">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="fef18-127">Результаты запроса на группировку по политике регулирования.</span><span class="sxs-lookup"><span data-stu-id="fef18-127">Group query result by Throttle Policy applied.</span></span>

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

### <span data-ttu-id="fef18-128">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="fef18-128">-IntervalLength</span></span>
<span data-ttu-id="fef18-129">Интервал времени (в минутах), используемый для создания журналов LogAnalytics звонков.</span><span class="sxs-lookup"><span data-stu-id="fef18-129">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef18-130">-Location</span><span class="sxs-lookup"><span data-stu-id="fef18-130">-Location</span></span>
<span data-ttu-id="fef18-131">Место, на которое запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="fef18-131">The location upon which log analytic is queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef18-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="fef18-132">-NoWait</span></span>
<span data-ttu-id="fef18-133">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="fef18-133">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="fef18-134">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="fef18-134">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="fef18-135">-ToTime</span><span class="sxs-lookup"><span data-stu-id="fef18-135">-ToTime</span></span>
<span data-ttu-id="fef18-136">Время запроса</span><span class="sxs-lookup"><span data-stu-id="fef18-136">To time of the query</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef18-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fef18-137">-Confirm</span></span>
<span data-ttu-id="fef18-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fef18-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fef18-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef18-139">-WhatIf</span></span>
<span data-ttu-id="fef18-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fef18-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fef18-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fef18-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fef18-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef18-142">CommonParameters</span></span>
<span data-ttu-id="fef18-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fef18-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef18-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fef18-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef18-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fef18-145">INPUTS</span></span>

### <span data-ttu-id="fef18-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fef18-146">System.String</span></span>

## <span data-ttu-id="fef18-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fef18-147">OUTPUTS</span></span>

### <span data-ttu-id="fef18-148">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="fef18-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="fef18-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="fef18-149">NOTES</span></span>

## <span data-ttu-id="fef18-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fef18-150">RELATED LINKS</span></span>
