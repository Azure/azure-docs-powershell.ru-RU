---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 8889a0957dec645b987e97012948c18f0527bc92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563023"
---
# <span data-ttu-id="9b340-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="9b340-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="9b340-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b340-102">SYNOPSIS</span></span>
<span data-ttu-id="9b340-103">Возвращает значения метрик ресурса.</span><span class="sxs-lookup"><span data-stu-id="9b340-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b340-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b340-104">SYNTAX</span></span>

### <span data-ttu-id="9b340-105">GetWithDefaultParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b340-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b340-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="9b340-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b340-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b340-107">DESCRIPTION</span></span>
<span data-ttu-id="9b340-108">Командлет **Get-AzureRmMetric** получает значения метрик для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="9b340-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="9b340-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b340-109">EXAMPLES</span></span>

### <span data-ttu-id="9b340-110">Пример 1: получение метрики с суммарным выводом</span><span class="sxs-lookup"><span data-stu-id="9b340-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="9b340-111">Эта команда возвращает значения метрик для website3 с програнкой времени в 1 минуту.</span><span class="sxs-lookup"><span data-stu-id="9b340-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="9b340-112">Пример 2: получение метрики с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="9b340-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="9b340-113">Эта команда возвращает значения метрик для website3 с програнкой времени в 1 минуту.</span><span class="sxs-lookup"><span data-stu-id="9b340-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="9b340-114">Вывод будет подробным.</span><span class="sxs-lookup"><span data-stu-id="9b340-114">The output is detailed.</span></span>

### <span data-ttu-id="9b340-115">Пример 3: получение подробных выходных данных для указанной метрики</span><span class="sxs-lookup"><span data-stu-id="9b340-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricNames "Requests" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="9b340-116">Эта команда получает подробный вывод для метрики запросов.</span><span class="sxs-lookup"><span data-stu-id="9b340-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="9b340-117">Пример 4: получение обобщенного результата для указанной метрики с указанным фильтром измерений</span><span class="sxs-lookup"><span data-stu-id="9b340-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzureRmMetricFilter -Dimension City -Operator eq -Values "Seattle","Toronto"), (New-AzureRmMetricDimensionFilter -Dimension AuthenticationType -Operator eq -Values User))

PS C:\> Get-AzureRmMetricValues -ResourceId <resourcId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="9b340-118">Эта команда возвращает обобщенные выходные данные для метрики PageViews с указанными фильтром dimesion и типом статистической обработки.</span><span class="sxs-lookup"><span data-stu-id="9b340-118">This command gets summarized output for the PageViews metric with specified dimesion filter and aggregation type.</span></span>

## <span data-ttu-id="9b340-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b340-119">PARAMETERS</span></span>

### <span data-ttu-id="9b340-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="9b340-120">-AggregationType</span></span>
<span data-ttu-id="9b340-121">Тип статистической обработки запроса</span><span class="sxs-lookup"><span data-stu-id="9b340-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b340-122">-DefaultProfile</span></span>
<span data-ttu-id="9b340-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b340-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b340-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="9b340-124">-DetailedOutput</span></span>
<span data-ttu-id="9b340-125">Указывает на то, что этот командлет отображает подробный вывод.</span><span class="sxs-lookup"><span data-stu-id="9b340-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="9b340-126">По умолчанию выводятся итоги.</span><span class="sxs-lookup"><span data-stu-id="9b340-126">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9b340-127">-EndTime</span></span>
<span data-ttu-id="9b340-128">Указывает время окончания запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="9b340-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="9b340-129">Значение по умолчанию — текущее время.</span><span class="sxs-lookup"><span data-stu-id="9b340-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="9b340-130">-MetricFilter</span></span>
<span data-ttu-id="9b340-131">Задает фильтр измерения метрики для запроса метрик.</span><span class="sxs-lookup"><span data-stu-id="9b340-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9b340-132">-MetricName</span></span>
<span data-ttu-id="9b340-133">Указывает массив имен метрик.</span><span class="sxs-lookup"><span data-stu-id="9b340-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="9b340-134">-MetricNamespace</span></span>
<span data-ttu-id="9b340-135">Задает пространство имен метрик, для которого нужно запросить метрики запроса.</span><span class="sxs-lookup"><span data-stu-id="9b340-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="9b340-136">-OrderBy</span></span>
<span data-ttu-id="9b340-137">Задает агрегат для сортировки результатов и направления сортировки (пример: Sum ASC).</span><span class="sxs-lookup"><span data-stu-id="9b340-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b340-138">-ResourceId</span></span>
<span data-ttu-id="9b340-139">Указывает идентификатор ресурса метрики.</span><span class="sxs-lookup"><span data-stu-id="9b340-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="9b340-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="9b340-140">-ResultType</span></span>
<span data-ttu-id="9b340-141">Указывает тип возвращаемого результата (метаданные или данные).</span><span class="sxs-lookup"><span data-stu-id="9b340-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9b340-142">-StartTime</span></span>
<span data-ttu-id="9b340-143">Задает время начала запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="9b340-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="9b340-144">По умолчанию используется текущее местное время минус один час.</span><span class="sxs-lookup"><span data-stu-id="9b340-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="9b340-145">-TimeGrain</span></span>
<span data-ttu-id="9b340-146">Задает Гран времени метрики в качестве объекта **TimeSpan** в формате чч: мм: СС.</span><span class="sxs-lookup"><span data-stu-id="9b340-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-147">-Top</span><span class="sxs-lookup"><span data-stu-id="9b340-147">-Top</span></span>
<span data-ttu-id="9b340-148">Задает максимальное число извлекаемых записей (значение по умолчанию: 10), которые должны быть указаны в $filter.</span><span class="sxs-lookup"><span data-stu-id="9b340-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b340-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b340-149">CommonParameters</span></span>
<span data-ttu-id="9b340-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b340-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b340-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b340-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b340-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b340-152">INPUTS</span></span>

### <span data-ttu-id="9b340-153">System. String</span><span class="sxs-lookup"><span data-stu-id="9b340-153">System.String</span></span>

### <span data-ttu-id="9b340-154">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="9b340-154">System.TimeSpan</span></span>

### <span data-ttu-id="9b340-155">System. Nullable "1 [[Microsoft. Azure. Management. Monitor. Models. AggregationType, Microsoft. Azure. Management. Monitor, Version = 0.19.1.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9b340-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9b340-156">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="9b340-156">System.DateTime</span></span>

### <span data-ttu-id="9b340-157">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9b340-157">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9b340-158">System. Nullable "1 [[Microsoft. Azure. Management. Monitor. Model. ResultType, Microsoft. Azure. Management. Monitor, Version = 0.19.1.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9b340-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9b340-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="9b340-159">System.String[]</span></span>

### <span data-ttu-id="9b340-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9b340-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9b340-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b340-161">OUTPUTS</span></span>

### <span data-ttu-id="9b340-162">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric</span><span class="sxs-lookup"><span data-stu-id="9b340-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="9b340-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b340-163">NOTES</span></span>

## <span data-ttu-id="9b340-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b340-164">RELATED LINKS</span></span>

<span data-ttu-id="9b340-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md) 
 [New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="9b340-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>


