---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 1947b060f6b1d2fcf7e4380d3a1ece808ea29785
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988490"
---
# <span data-ttu-id="d22d6-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="d22d6-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="d22d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d22d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d22d6-103">Получает сведения об использовании подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d22d6-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="d22d6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d22d6-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d22d6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d22d6-105">DESCRIPTION</span></span>
<span data-ttu-id="d22d6-106">С **помощью cmdlet Get-UsageAggregates** можно получить агрегированные данные об использовании подписки Azure по следующим свойствам:</span><span class="sxs-lookup"><span data-stu-id="d22d6-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="d22d6-107">Время начала и окончания данных об использовании.</span><span class="sxs-lookup"><span data-stu-id="d22d6-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="d22d6-108">Точность агрегирования ( ежедневно или почасовая).</span><span class="sxs-lookup"><span data-stu-id="d22d6-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="d22d6-109">Детализация на уровне экземпляра для нескольких экземпляров одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="d22d6-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="d22d6-110">Для поиска согласованных результатов возвращаемая информация основана на том, когда ресурс Azure сообщил сведения об использовании.</span><span class="sxs-lookup"><span data-stu-id="d22d6-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="d22d6-111">Дополнительные сведения см. в справочнике azure Billing REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) (Microsoft Developer Network библиотеке).</span><span class="sxs-lookup"><span data-stu-id="d22d6-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="d22d6-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d22d6-112">EXAMPLES</span></span>

### <span data-ttu-id="d22d6-113">Пример 1. Извлечение данных подписки</span><span class="sxs-lookup"><span data-stu-id="d22d6-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="d22d6-114">Эта команда извлекает данные об использовании подписки с 02.05.2015 по 05.05.2015.</span><span class="sxs-lookup"><span data-stu-id="d22d6-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="d22d6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d22d6-115">PARAMETERS</span></span>

### <span data-ttu-id="d22d6-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="d22d6-116">-AggregationGranularity</span></span>
<span data-ttu-id="d22d6-117">Определяет точность агрегирования для данных.</span><span class="sxs-lookup"><span data-stu-id="d22d6-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="d22d6-118">Допустимые значения: ежедневно и почасово.</span><span class="sxs-lookup"><span data-stu-id="d22d6-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="d22d6-119">Значение по умолчанию — "Ежедневно".</span><span class="sxs-lookup"><span data-stu-id="d22d6-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22d6-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="d22d6-120">-ContinuationToken</span></span>
<span data-ttu-id="d22d6-121">Определяет маркер продолжения, полученный из ответа во время предыдущего вызова.</span><span class="sxs-lookup"><span data-stu-id="d22d6-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="d22d6-122">Для большого набора результатов ответы по страницам высвеяются с помощью маркеров продолжения.</span><span class="sxs-lookup"><span data-stu-id="d22d6-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="d22d6-123">Маркер продолжения служит закладкой для выполнения.</span><span class="sxs-lookup"><span data-stu-id="d22d6-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="d22d6-124">Если этот параметр не задан, данные извлекаются с начала дня или часа, указанного в *ReportedStartTime.*</span><span class="sxs-lookup"><span data-stu-id="d22d6-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="d22d6-125">При этом мы рекомендуем следующую ссылку в ответе на страницу.</span><span class="sxs-lookup"><span data-stu-id="d22d6-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="d22d6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d22d6-126">-DefaultProfile</span></span>
<span data-ttu-id="d22d6-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d22d6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d22d6-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="d22d6-128">-ReportedEndTime</span></span>
<span data-ttu-id="d22d6-129">Время окончания, указанное для записи использования ресурсов в системе вычитания Azure.</span><span class="sxs-lookup"><span data-stu-id="d22d6-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="d22d6-130">Azure — это распределенная система, охватывающая несколько центрах обработки данных по всему миру, поэтому существует задержка между фактическим использованием ресурса, т. е. временем использования ресурса, и когда событие использования достигло системы вычитания , т. е. времени, за который было положено использование ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d22d6-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="d22d6-131">Чтобы получить все события использования подписки, о чем сообщалось за период времени, вы можете сделать запрос по отчитаемой информации о времени.</span><span class="sxs-lookup"><span data-stu-id="d22d6-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="d22d6-132">Хотя запрос был запросчитано по времени, с помощью cmdlet можно агрегировать данные ответов по времени использования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d22d6-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="d22d6-133">Данные об использовании ресурсов удобно использовать для анализа данных.</span><span class="sxs-lookup"><span data-stu-id="d22d6-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="d22d6-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="d22d6-134">-ReportedStartTime</span></span>
<span data-ttu-id="d22d6-135">Время начала, указанное для записи использования ресурсов в системе вычитания Azure.</span><span class="sxs-lookup"><span data-stu-id="d22d6-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="d22d6-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="d22d6-136">-ShowDetails</span></span>
<span data-ttu-id="d22d6-137">Указывает, возвращает ли этот cmdlet сведения на уровне экземпляра с данными об использовании.</span><span class="sxs-lookup"><span data-stu-id="d22d6-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="d22d6-138">Значение по умолчанию — $True.</span><span class="sxs-lookup"><span data-stu-id="d22d6-138">The default value is $True.</span></span>
<span data-ttu-id="d22d6-139">Если $False, служба собирает результаты на стороне сервера и поэтому возвращает меньше групп.</span><span class="sxs-lookup"><span data-stu-id="d22d6-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="d22d6-140">Например, если вы работаете на трех веб-сайтах, по умолчанию вы получите три строки для использования веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="d22d6-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="d22d6-141">Однако если значение $False, все данные для одного и того же **subscriptionId,** **meterId,** **usageStartTime** и **usageEndTime** свернуты в один элемент строки.</span><span class="sxs-lookup"><span data-stu-id="d22d6-141">However, when the value is $False, all the data for the same **subscriptionId**, **meterId**, **usageStartTime**, and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d22d6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d22d6-142">CommonParameters</span></span>
<span data-ttu-id="d22d6-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d22d6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d22d6-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d22d6-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d22d6-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d22d6-145">INPUTS</span></span>

### <span data-ttu-id="d22d6-146">Нет</span><span class="sxs-lookup"><span data-stu-id="d22d6-146">None</span></span>

## <span data-ttu-id="d22d6-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d22d6-147">OUTPUTS</span></span>

### <span data-ttu-id="d22d6-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="d22d6-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="d22d6-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d22d6-149">NOTES</span></span>

## <span data-ttu-id="d22d6-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d22d6-150">RELATED LINKS</span></span>
