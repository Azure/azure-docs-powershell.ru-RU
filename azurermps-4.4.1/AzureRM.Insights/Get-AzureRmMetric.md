---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: d8b7c83ff2804de3e60af7c5ea8ce9f3e2d1eb97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567632"
---
# <span data-ttu-id="965b6-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="965b6-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="965b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="965b6-102">SYNOPSIS</span></span>
<span data-ttu-id="965b6-103">Возвращает значения метрик ресурса.</span><span class="sxs-lookup"><span data-stu-id="965b6-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="965b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="965b6-104">SYNTAX</span></span>

### <span data-ttu-id="965b6-105">Параметры для Get-AzureRmMetric командлета в режиме по умолчанию</span><span class="sxs-lookup"><span data-stu-id="965b6-105">Parameters for Get-AzureRmMetric cmdlet in the default mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="965b6-106">Параметры для Get-AzureRmMetric командлета в режиме полного множества параметров</span><span class="sxs-lookup"><span data-stu-id="965b6-106">Parameters for Get-AzureRmMetric cmdlet in the full param set mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [[-TimeGrain] <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] -MetricNames <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="965b6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="965b6-107">DESCRIPTION</span></span>
<span data-ttu-id="965b6-108">Командлет **Get-AzureRmMetric** получает значения метрик для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="965b6-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="965b6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="965b6-109">EXAMPLES</span></span>

### <span data-ttu-id="965b6-110">Пример 1: получение метрики с суммарным выводом</span><span class="sxs-lookup"><span data-stu-id="965b6-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="965b6-111">Эта команда возвращает значения метрик для website3 с програнкой времени в 1 минуту.</span><span class="sxs-lookup"><span data-stu-id="965b6-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="965b6-112">Пример 2: получение метрики с подробным выводом</span><span class="sxs-lookup"><span data-stu-id="965b6-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="965b6-113">Эта команда возвращает значения метрик для website3 с програнкой времени в 1 минуту.</span><span class="sxs-lookup"><span data-stu-id="965b6-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="965b6-114">Вывод будет подробным.</span><span class="sxs-lookup"><span data-stu-id="965b6-114">The output is detailed.</span></span>

### <span data-ttu-id="965b6-115">Пример 3: получение подробных выходных данных для указанной метрики</span><span class="sxs-lookup"><span data-stu-id="965b6-115">Example 3: Get detailed output for a specified metric</span></span>
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

<span data-ttu-id="965b6-116">Эта команда получает подробный вывод для метрики запросов.</span><span class="sxs-lookup"><span data-stu-id="965b6-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="965b6-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="965b6-117">PARAMETERS</span></span>

### <span data-ttu-id="965b6-118">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="965b6-118">-DetailedOutput</span></span>
<span data-ttu-id="965b6-119">Указывает на то, что этот командлет отображает подробный вывод.</span><span class="sxs-lookup"><span data-stu-id="965b6-119">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="965b6-120">По умолчанию выводятся итоги.</span><span class="sxs-lookup"><span data-stu-id="965b6-120">By default, output is summarized.</span></span>

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

### <span data-ttu-id="965b6-121">-EndTime</span><span class="sxs-lookup"><span data-stu-id="965b6-121">-EndTime</span></span>
<span data-ttu-id="965b6-122">Указывает время окончания запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="965b6-122">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="965b6-123">Значение по умолчанию — текущее время.</span><span class="sxs-lookup"><span data-stu-id="965b6-123">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965b6-124">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="965b6-124">-MetricNames</span></span>
<span data-ttu-id="965b6-125">Указывает массив имен метрик.</span><span class="sxs-lookup"><span data-stu-id="965b6-125">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the default mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965b6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="965b6-126">-ResourceId</span></span>
<span data-ttu-id="965b6-127">Указывает идентификатор ресурса метрики.</span><span class="sxs-lookup"><span data-stu-id="965b6-127">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="965b6-128">-StartTime</span><span class="sxs-lookup"><span data-stu-id="965b6-128">-StartTime</span></span>
<span data-ttu-id="965b6-129">Задает время начала запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="965b6-129">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="965b6-130">По умолчанию используется текущее местное время минус один час.</span><span class="sxs-lookup"><span data-stu-id="965b6-130">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965b6-131">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="965b6-131">-TimeGrain</span></span>
<span data-ttu-id="965b6-132">Задает Гран времени метрики в качестве объекта **TimeSpan** в формате чч: мм: СС.</span><span class="sxs-lookup"><span data-stu-id="965b6-132">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965b6-133">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="965b6-133">-AggregationType</span></span>
<span data-ttu-id="965b6-134">Тип статистической обработки для Quer</span><span class="sxs-lookup"><span data-stu-id="965b6-134">The aggregation type of the quer</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965b6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965b6-135">-DefaultProfile</span></span>
<span data-ttu-id="965b6-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="965b6-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="965b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965b6-137">CommonParameters</span></span>
<span data-ttu-id="965b6-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="965b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965b6-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="965b6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965b6-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="965b6-140">INPUTS</span></span>

## <span data-ttu-id="965b6-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="965b6-141">OUTPUTS</span></span>

### <span data-ttu-id="965b6-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="965b6-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="965b6-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="965b6-143">NOTES</span></span>

## <span data-ttu-id="965b6-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="965b6-144">RELATED LINKS</span></span>

[<span data-ttu-id="965b6-145">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="965b6-145">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


