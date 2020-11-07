---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 63ade199b63e57cc72e965002942773f47214494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732264"
---
# <span data-ttu-id="05bde-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="05bde-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="05bde-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05bde-102">SYNOPSIS</span></span>
<span data-ttu-id="05bde-103">Возвращает значения метрик ресурса.</span><span class="sxs-lookup"><span data-stu-id="05bde-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05bde-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05bde-104">SYNTAX</span></span>

### <span data-ttu-id="05bde-105">GetWithDefaultParameters</span><span class="sxs-lookup"><span data-stu-id="05bde-105">GetWithDefaultParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05bde-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="05bde-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05bde-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05bde-107">DESCRIPTION</span></span>
<span data-ttu-id="05bde-108">Командлет **Get-AzureRmMetric** получает значения метрик для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="05bde-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="05bde-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05bde-109">EXAMPLES</span></span>

### <span data-ttu-id="05bde-110">Пример 1: получение метрики с суммарным выводом</span><span class="sxs-lookup"><span data-stu-id="05bde-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="05bde-111">Эта команда возвращает значения метрик для website3 с програнкой времени в 1 минуту.</span><span class="sxs-lookup"><span data-stu-id="05bde-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="05bde-112">Пример 2: получение метрики с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="05bde-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="05bde-113">Эта команда возвращает значения метрик для website3 с програнкой времени в 1 минуту.</span><span class="sxs-lookup"><span data-stu-id="05bde-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="05bde-114">Вывод будет подробным.</span><span class="sxs-lookup"><span data-stu-id="05bde-114">The output is detailed.</span></span>

### <span data-ttu-id="05bde-115">Пример 3: получение подробных выходных данных для указанной метрики</span><span class="sxs-lookup"><span data-stu-id="05bde-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
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

<span data-ttu-id="05bde-116">Эта команда получает подробный вывод для метрики запросов.</span><span class="sxs-lookup"><span data-stu-id="05bde-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="05bde-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05bde-117">PARAMETERS</span></span>

### <span data-ttu-id="05bde-118">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="05bde-118">-AggregationType</span></span>
<span data-ttu-id="05bde-119">Тип статистической обработки запроса</span><span class="sxs-lookup"><span data-stu-id="05bde-119">The aggregation type of the query</span></span>

```yaml
Type: AggregationType
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05bde-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bde-120">-DefaultProfile</span></span>
<span data-ttu-id="05bde-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05bde-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05bde-122">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="05bde-122">-DetailedOutput</span></span>
<span data-ttu-id="05bde-123">Указывает на то, что этот командлет отображает подробный вывод.</span><span class="sxs-lookup"><span data-stu-id="05bde-123">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="05bde-124">По умолчанию выводятся итоги.</span><span class="sxs-lookup"><span data-stu-id="05bde-124">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05bde-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="05bde-125">-EndTime</span></span>
<span data-ttu-id="05bde-126">Указывает время окончания запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="05bde-126">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="05bde-127">Значение по умолчанию — текущее время.</span><span class="sxs-lookup"><span data-stu-id="05bde-127">The default is the current time.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05bde-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="05bde-128">-MetricName</span></span>
<span data-ttu-id="05bde-129">Указывает массив имен метрик.</span><span class="sxs-lookup"><span data-stu-id="05bde-129">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False (GetWithDefaultParameters), True (GetAzureRmAMetricFullParamGroup)
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: GetWithFullParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05bde-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05bde-130">-ResourceId</span></span>
<span data-ttu-id="05bde-131">Указывает идентификатор ресурса метрики.</span><span class="sxs-lookup"><span data-stu-id="05bde-131">Specifies the resource ID of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05bde-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="05bde-132">-StartTime</span></span>
<span data-ttu-id="05bde-133">Задает время начала запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="05bde-133">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="05bde-134">По умолчанию используется текущее местное время минус один час.</span><span class="sxs-lookup"><span data-stu-id="05bde-134">The default is the current local time minus one hour.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05bde-135">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="05bde-135">-TimeGrain</span></span>
<span data-ttu-id="05bde-136">Задает Гран времени метрики в качестве объекта **TimeSpan** в формате чч: мм: СС.</span><span class="sxs-lookup"><span data-stu-id="05bde-136">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05bde-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bde-137">CommonParameters</span></span>
<span data-ttu-id="05bde-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05bde-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bde-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05bde-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bde-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05bde-140">INPUTS</span></span>

### <span data-ttu-id="05bde-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="05bde-141">None</span></span>
<span data-ttu-id="05bde-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="05bde-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05bde-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05bde-143">OUTPUTS</span></span>

### <span data-ttu-id="05bde-144">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="05bde-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="05bde-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="05bde-145">NOTES</span></span>

## <span data-ttu-id="05bde-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05bde-146">RELATED LINKS</span></span>

[<span data-ttu-id="05bde-147">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="05bde-147">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


