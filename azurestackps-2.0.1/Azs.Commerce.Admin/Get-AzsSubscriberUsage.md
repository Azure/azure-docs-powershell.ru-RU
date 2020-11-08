---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075344"
---
# <span data-ttu-id="dfeb7-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="dfeb7-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="dfeb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfeb7-102">SYNOPSIS</span></span>
<span data-ttu-id="dfeb7-103">Возвращает коллекцию SubscriberUsageAggregates, UsageAggregates от пользователей.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="dfeb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfeb7-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dfeb7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfeb7-105">DESCRIPTION</span></span>
<span data-ttu-id="dfeb7-106">Возвращает коллекцию SubscriberUsageAggregates, UsageAggregates от пользователей.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="dfeb7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfeb7-107">EXAMPLES</span></span>

### <span data-ttu-id="dfeb7-108">Пример 1: получение данных об использовании, агрегированных по дням</span><span class="sxs-lookup"><span data-stu-id="dfeb7-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="dfeb7-109">Получите данные об использовании для всего дня 30 декабря 2019 (в формате UTC) для всех клиентов поставщика, агрегированные за день.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="dfeb7-110">ReportedStartTime и ReportedEndTime должны округляться до дней.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="dfeb7-111">При вызываемом качестве администратора службы в этой области отображаются все данные об использовании для каждого клиента.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="dfeb7-112">Пример 2: получение данных об использовании, агрегированных на час</span><span class="sxs-lookup"><span data-stu-id="dfeb7-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="dfeb7-113">Получите данные об использовании между 12am-2am в 30 декабря 2019 (в формате UTC), агрегированные за час.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="dfeb7-114">ReportedStartTime и ReportedEndTime должны округляться до часов.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="dfeb7-115">Аналогичным образом, если он вызывается в качестве администратора службы, это отобразит все данные об использовании для каждого клиента.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="dfeb7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfeb7-116">PARAMETERS</span></span>

### <span data-ttu-id="dfeb7-117">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="dfeb7-117">-AggregationGranularity</span></span>
<span data-ttu-id="dfeb7-118">Гранулярность статистической обработки.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-118">The aggregation granularity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfeb7-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="dfeb7-119">-ContinuationToken</span></span>
<span data-ttu-id="dfeb7-120">Маркер продолжения.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-120">The continuation token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfeb7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfeb7-121">-DefaultProfile</span></span>
<span data-ttu-id="dfeb7-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfeb7-123">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="dfeb7-123">-ReportedEndTime</span></span>
<span data-ttu-id="dfeb7-124">Указанное время окончания (исключающее).</span><span class="sxs-lookup"><span data-stu-id="dfeb7-124">The reported end time (exclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfeb7-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="dfeb7-125">-ReportedStartTime</span></span>
<span data-ttu-id="dfeb7-126">Указанное время начала (включительно).</span><span class="sxs-lookup"><span data-stu-id="dfeb7-126">The reported start time (inclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfeb7-127">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="dfeb7-127">-SubscriberId</span></span>
<span data-ttu-id="dfeb7-128">Идентификатор подписки клиента.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-128">The tenant subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfeb7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfeb7-129">-SubscriptionId</span></span>
<span data-ttu-id="dfeb7-130">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dfeb7-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dfeb7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfeb7-132">CommonParameters</span></span>
<span data-ttu-id="dfeb7-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfeb7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfeb7-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfeb7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfeb7-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfeb7-135">INPUTS</span></span>

## <span data-ttu-id="dfeb7-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfeb7-136">OUTPUTS</span></span>

### <span data-ttu-id="dfeb7-137">Microsoft. Azure. PowerShell. командлеты. Commerce. Models. Api20150601Preview. IUsageAggregate</span><span class="sxs-lookup"><span data-stu-id="dfeb7-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="dfeb7-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfeb7-138">NOTES</span></span>

## <span data-ttu-id="dfeb7-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfeb7-139">RELATED LINKS</span></span>

