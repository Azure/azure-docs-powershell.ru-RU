---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetric.md
ms.openlocfilehash: d02a6f9ca3f4821fa8a552f92ef90fa24a9e6bd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401924"
---
# <span data-ttu-id="7eab8-101">Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="7eab8-101">Get-AzMetric</span></span>

## <span data-ttu-id="7eab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eab8-102">SYNOPSIS</span></span>
<span data-ttu-id="7eab8-103">Возвращает метрические значения ресурса.</span><span class="sxs-lookup"><span data-stu-id="7eab8-103">Gets the metric values of a resource.</span></span>

## <span data-ttu-id="7eab8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7eab8-104">SYNTAX</span></span>

### <span data-ttu-id="7eab8-105">GetWithDefaultParameters (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7eab8-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7eab8-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="7eab8-106">GetWithFullParameters</span></span>
```
Get-AzMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eab8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eab8-107">DESCRIPTION</span></span>
<span data-ttu-id="7eab8-108">С **помощью cmdlet Get-AzMetric** можно получить метрические значения для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="7eab8-108">The **Get-AzMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="7eab8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7eab8-109">EXAMPLES</span></span>

### <span data-ttu-id="7eab8-110">Пример 1. Метрическая система получения обобщенных результатов</span><span class="sxs-lookup"><span data-stu-id="7eab8-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
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

<span data-ttu-id="7eab8-111">Эта команда получает метрические значения для веб-сайта3 с временем, большим количеством минут.</span><span class="sxs-lookup"><span data-stu-id="7eab8-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="7eab8-112">Пример 2. Метрическая система подробных выходных данных</span><span class="sxs-lookup"><span data-stu-id="7eab8-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="7eab8-113">Эта команда получает метрические значения для веб-сайта3 с временем, большим количеством минут.</span><span class="sxs-lookup"><span data-stu-id="7eab8-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="7eab8-114">Результат будет подробным.</span><span class="sxs-lookup"><span data-stu-id="7eab8-114">The output is detailed.</span></span>

### <span data-ttu-id="7eab8-115">Пример 3. Подробные выходные данные для указанной метрик</span><span class="sxs-lookup"><span data-stu-id="7eab8-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricName "Requests" -TimeGrain 00:01:00 -DetailedOutput
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

<span data-ttu-id="7eab8-116">Эта команда получает подробные выходные данные для метрике "Запросы".</span><span class="sxs-lookup"><span data-stu-id="7eab8-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="7eab8-117">Пример 4. Обобщение результатов для указанной метрик с помощью указанного фильтра измерения</span><span class="sxs-lookup"><span data-stu-id="7eab8-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","Toronto"), (New-AzMetricFilter -Dimension AuthenticationType -Operator eq -Value User))

PS C:\> Get-AzMetric -ResourceId <resourceId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
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

<span data-ttu-id="7eab8-118">Эта команда получает итоговые результаты для метрик PageViews с указанным фильтром измерения и типом агрегирования.</span><span class="sxs-lookup"><span data-stu-id="7eab8-118">This command gets summarized output for the PageViews metric with specified dimension filter and aggregation type.</span></span>

## <span data-ttu-id="7eab8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eab8-119">PARAMETERS</span></span>

### <span data-ttu-id="7eab8-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="7eab8-120">-AggregationType</span></span>
<span data-ttu-id="7eab8-121">Тип агрегирования запроса</span><span class="sxs-lookup"><span data-stu-id="7eab8-121">The aggregation type of the query</span></span>

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

### <span data-ttu-id="7eab8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eab8-122">-DefaultProfile</span></span>
<span data-ttu-id="7eab8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7eab8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eab8-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="7eab8-124">-DetailedOutput</span></span>
<span data-ttu-id="7eab8-125">Указывает на то, что этот cmdlet выводит подробные данные.</span><span class="sxs-lookup"><span data-stu-id="7eab8-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="7eab8-126">По умолчанию выходные данные обобщены.</span><span class="sxs-lookup"><span data-stu-id="7eab8-126">By default, output is summarized.</span></span>

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

### <span data-ttu-id="7eab8-127">-EndTime</span><span class="sxs-lookup"><span data-stu-id="7eab8-127">-EndTime</span></span>
<span data-ttu-id="7eab8-128">Время окончания запроса в локальное время.</span><span class="sxs-lookup"><span data-stu-id="7eab8-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="7eab8-129">Значение по умолчанию — текущее время.</span><span class="sxs-lookup"><span data-stu-id="7eab8-129">The default is the current time.</span></span>

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

### <span data-ttu-id="7eab8-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="7eab8-130">-MetricFilter</span></span>
<span data-ttu-id="7eab8-131">Фильтр метрических измерений для метрики запроса.</span><span class="sxs-lookup"><span data-stu-id="7eab8-131">Specifies the metric dimension filter to query metrics for.</span></span>

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

### <span data-ttu-id="7eab8-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="7eab8-132">-MetricName</span></span>
<span data-ttu-id="7eab8-133">Определяет массив имен метрик.</span><span class="sxs-lookup"><span data-stu-id="7eab8-133">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="7eab8-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="7eab8-134">-MetricNamespace</span></span>
<span data-ttu-id="7eab8-135">Указывает пространство имен метрики, для которого нужно запрашивать метрики.</span><span class="sxs-lookup"><span data-stu-id="7eab8-135">Specifies the metric namespace to query metrics for.</span></span>

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

### <span data-ttu-id="7eab8-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="7eab8-136">-OrderBy</span></span>
<span data-ttu-id="7eab8-137">Определяет агрегат, который будет применяться для сортировки результатов, и направление сортировки (пример: sum asc).</span><span class="sxs-lookup"><span data-stu-id="7eab8-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

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

### <span data-ttu-id="7eab8-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eab8-138">-ResourceId</span></span>
<span data-ttu-id="7eab8-139">Определяет ИД ресурса метрик.</span><span class="sxs-lookup"><span data-stu-id="7eab8-139">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="7eab8-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="7eab8-140">-ResultType</span></span>
<span data-ttu-id="7eab8-141">Тип возвращаемого результата (метаданные или данные).</span><span class="sxs-lookup"><span data-stu-id="7eab8-141">Specifies the result type to be returned (metadata or data).</span></span>

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

### <span data-ttu-id="7eab8-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7eab8-142">-StartTime</span></span>
<span data-ttu-id="7eab8-143">Время начала запроса в локальное время.</span><span class="sxs-lookup"><span data-stu-id="7eab8-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="7eab8-144">По умолчанию за вычетом одного часа за вычетом текущего локального времени.</span><span class="sxs-lookup"><span data-stu-id="7eab8-144">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="7eab8-145">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="7eab8-145">-TimeGrain</span></span>
<span data-ttu-id="7eab8-146">Определяет time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span><span class="sxs-lookup"><span data-stu-id="7eab8-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

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

### <span data-ttu-id="7eab8-147">-Top</span><span class="sxs-lookup"><span data-stu-id="7eab8-147">-Top</span></span>
<span data-ttu-id="7eab8-148">Указывает максимальное количество извлекаемых записей (по умолчанию:10), заданное с помощью $filter.</span><span class="sxs-lookup"><span data-stu-id="7eab8-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

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

### <span data-ttu-id="7eab8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eab8-149">CommonParameters</span></span>
<span data-ttu-id="7eab8-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eab8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eab8-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7eab8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eab8-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7eab8-152">INPUTS</span></span>

### <span data-ttu-id="7eab8-153">System.String</span><span class="sxs-lookup"><span data-stu-id="7eab8-153">System.String</span></span>

### <span data-ttu-id="7eab8-154">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="7eab8-154">System.TimeSpan</span></span>

### <span data-ttu-id="7eab8-155">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7eab8-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7eab8-156">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="7eab8-156">System.DateTime</span></span>

### <span data-ttu-id="7eab8-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7eab8-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7eab8-158">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7eab8-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.21.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="7eab8-159">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7eab8-159">System.String[]</span></span>

### <span data-ttu-id="7eab8-160">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7eab8-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7eab8-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7eab8-161">OUTPUTS</span></span>

### <span data-ttu-id="7eab8-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span><span class="sxs-lookup"><span data-stu-id="7eab8-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="7eab8-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7eab8-163">NOTES</span></span>

<span data-ttu-id="7eab8-164">Дополнительные сведения о поддерживаемых показателях можно найти по https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="7eab8-164">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="7eab8-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7eab8-165">RELATED LINKS</span></span>

<span data-ttu-id="7eab8-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md) 
 [New-AzMetricFilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="7eab8-166">[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


