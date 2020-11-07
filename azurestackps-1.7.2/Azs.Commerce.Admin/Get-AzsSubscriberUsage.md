---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 12b98727cdb8e6d31fb1aaf1a2215b79a6b982e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906381"
---
# <span data-ttu-id="43680-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="43680-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="43680-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43680-102">SYNOPSIS</span></span>
<span data-ttu-id="43680-103">Получение данных об использовании в течение указанного интервала времени.</span><span class="sxs-lookup"><span data-stu-id="43680-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="43680-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43680-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="43680-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43680-105">DESCRIPTION</span></span>
<span data-ttu-id="43680-106">Получение данных об использовании в течение указанного интервала времени.</span><span class="sxs-lookup"><span data-stu-id="43680-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="43680-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43680-107">EXAMPLES</span></span>

### <span data-ttu-id="43680-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="43680-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="43680-109">Получение данных об использовании за последние 24 часа.</span><span class="sxs-lookup"><span data-stu-id="43680-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="43680-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43680-110">PARAMETERS</span></span>

### <span data-ttu-id="43680-111">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="43680-111">-AggregationGranularity</span></span>
<span data-ttu-id="43680-112">Гранулярность статистической обработки.</span><span class="sxs-lookup"><span data-stu-id="43680-112">The aggregation granularity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43680-113">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="43680-113">-ContinuationToken</span></span>
<span data-ttu-id="43680-114">Маркер продолжения.</span><span class="sxs-lookup"><span data-stu-id="43680-114">The continuation token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43680-115">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="43680-115">-ReportedEndTime</span></span>
<span data-ttu-id="43680-116">Указанное время окончания (исключающее).</span><span class="sxs-lookup"><span data-stu-id="43680-116">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43680-117">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="43680-117">-ReportedStartTime</span></span>
<span data-ttu-id="43680-118">Указанное время начала (включительно).</span><span class="sxs-lookup"><span data-stu-id="43680-118">The reported start time (inclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43680-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="43680-119">-Skip</span></span>
<span data-ttu-id="43680-120">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="43680-120">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43680-121">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="43680-121">-SubscriberId</span></span>
<span data-ttu-id="43680-122">Идентификатор подписки клиента.</span><span class="sxs-lookup"><span data-stu-id="43680-122">The tenant subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43680-123">-Top</span><span class="sxs-lookup"><span data-stu-id="43680-123">-Top</span></span>
<span data-ttu-id="43680-124">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="43680-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="43680-125">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="43680-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43680-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43680-126">CommonParameters</span></span>
<span data-ttu-id="43680-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43680-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43680-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43680-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43680-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43680-129">INPUTS</span></span>

## <span data-ttu-id="43680-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43680-130">OUTPUTS</span></span>

### <span data-ttu-id="43680-131">Microsoft. AzureStack. Management. Commerce. admin. Models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="43680-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="43680-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="43680-132">NOTES</span></span>

## <span data-ttu-id="43680-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43680-133">RELATED LINKS</span></span>

