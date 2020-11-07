---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909158"
---
# <span data-ttu-id="bf499-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="bf499-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="bf499-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf499-102">SYNOPSIS</span></span>
<span data-ttu-id="bf499-103">Получение данных об использовании в течение указанного интервала времени.</span><span class="sxs-lookup"><span data-stu-id="bf499-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="bf499-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf499-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="bf499-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf499-105">DESCRIPTION</span></span>
<span data-ttu-id="bf499-106">Получение данных об использовании в течение указанного интервала времени.</span><span class="sxs-lookup"><span data-stu-id="bf499-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="bf499-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf499-107">EXAMPLES</span></span>

### <span data-ttu-id="bf499-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="bf499-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="bf499-109">Получение данных об использовании за последние 24 часа.</span><span class="sxs-lookup"><span data-stu-id="bf499-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="bf499-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf499-110">PARAMETERS</span></span>

### <span data-ttu-id="bf499-111">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="bf499-111">-SubscriberId</span></span>
<span data-ttu-id="bf499-112">Идентификатор подписки клиента.</span><span class="sxs-lookup"><span data-stu-id="bf499-112">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="bf499-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="bf499-113">-ReportedStartTime</span></span>
<span data-ttu-id="bf499-114">Указанное время начала (включительно).</span><span class="sxs-lookup"><span data-stu-id="bf499-114">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="bf499-115">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="bf499-115">-AggregationGranularity</span></span>
<span data-ttu-id="bf499-116">Гранулярность статистической обработки.</span><span class="sxs-lookup"><span data-stu-id="bf499-116">The aggregation granularity.</span></span>

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

### <span data-ttu-id="bf499-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="bf499-117">-Skip</span></span>
<span data-ttu-id="bf499-118">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="bf499-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bf499-119">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="bf499-119">-ReportedEndTime</span></span>
<span data-ttu-id="bf499-120">Указанное время окончания (исключающее).</span><span class="sxs-lookup"><span data-stu-id="bf499-120">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="bf499-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="bf499-121">-ContinuationToken</span></span>
<span data-ttu-id="bf499-122">Маркер продолжения.</span><span class="sxs-lookup"><span data-stu-id="bf499-122">The continuation token.</span></span>

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

### <span data-ttu-id="bf499-123">-Top</span><span class="sxs-lookup"><span data-stu-id="bf499-123">-Top</span></span>
<span data-ttu-id="bf499-124">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="bf499-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bf499-125">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="bf499-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bf499-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf499-126">CommonParameters</span></span>
<span data-ttu-id="bf499-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf499-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf499-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf499-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf499-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf499-129">INPUTS</span></span>

## <span data-ttu-id="bf499-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf499-130">OUTPUTS</span></span>

### <span data-ttu-id="bf499-131">Microsoft. AzureStack. Management. Commerce. admin. Models. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="bf499-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="bf499-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf499-132">NOTES</span></span>

## <span data-ttu-id="bf499-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf499-133">RELATED LINKS</span></span>
