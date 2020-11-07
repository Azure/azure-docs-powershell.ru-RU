---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.usageaggregates/get-usageaggregates
schema: 2.0.0
ms.openlocfilehash: 70dda4d40f517d3d7bd7a3a8d64584e74f80310a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913545"
---
# <span data-ttu-id="e4309-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="e4309-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="e4309-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4309-102">SYNOPSIS</span></span>
<span data-ttu-id="e4309-103">Получает указанные данные об использовании подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="e4309-103">Gets the reported Azure subscription usage details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4309-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4309-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4309-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4309-105">DESCRIPTION</span></span>
<span data-ttu-id="e4309-106">Командлет **Get-UsageAggregates** получает Объединенные данные об использовании подписки Azure следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="e4309-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 

- <span data-ttu-id="e4309-107">Время начала и окончания о том, когда была указана загрузка.</span><span class="sxs-lookup"><span data-stu-id="e4309-107">Start and end times of when the usage was reported.</span></span>

- <span data-ttu-id="e4309-108">Точность статистической обработки: ежедневно или ежечасно.</span><span class="sxs-lookup"><span data-stu-id="e4309-108">Aggregation precision, either daily or hourly.</span></span>

- <span data-ttu-id="e4309-109">Сведения об уровне экземпляра для нескольких экземпляров одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="e4309-109">Instance level detail for multiple instances of the same resource.</span></span>

<span data-ttu-id="e4309-110">Для противоречивых результатов возвращаемые данные основываются на том, когда ресурс Azure сообщил об использовании.</span><span class="sxs-lookup"><span data-stu-id="e4309-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>

<span data-ttu-id="e4309-111">Дополнительные сведения можно найти в справочнике API для служб выставления счетов https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c для Azure ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) в сетевой библиотеке разработчиков Microsoft Developer.</span><span class="sxs-lookup"><span data-stu-id="e4309-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="e4309-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4309-112">EXAMPLES</span></span>

### <span data-ttu-id="e4309-113">Пример 1: получение данных подписки</span><span class="sxs-lookup"><span data-stu-id="e4309-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="e4309-114">Эта команда извлекает сведения об использовании для подписки между 5/2/2015 и 5/5/2015.</span><span class="sxs-lookup"><span data-stu-id="e4309-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="e4309-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4309-115">PARAMETERS</span></span>

### <span data-ttu-id="e4309-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="e4309-116">-AggregationGranularity</span></span>
<span data-ttu-id="e4309-117">Определяет точность статистического выражения для данных.</span><span class="sxs-lookup"><span data-stu-id="e4309-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="e4309-118">Допустимые значения: ежедневно и ежечасно.</span><span class="sxs-lookup"><span data-stu-id="e4309-118">Valid values are: Daily and Hourly.</span></span>

<span data-ttu-id="e4309-119">По умолчанию используется значение ежедневно.</span><span class="sxs-lookup"><span data-stu-id="e4309-119">The default value is Daily.</span></span>

```yaml
Type: AggregationGranularity
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4309-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="e4309-120">-ContinuationToken</span></span>
<span data-ttu-id="e4309-121">Указывает токен продолжения, полученный из тела ответа в предыдущем вызове.</span><span class="sxs-lookup"><span data-stu-id="e4309-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="e4309-122">Для большого набора результатов ответы размещаются на странице с помощью маркеров продолжения.</span><span class="sxs-lookup"><span data-stu-id="e4309-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="e4309-123">Маркер продолжения служит закладкой для выполнения.</span><span class="sxs-lookup"><span data-stu-id="e4309-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="e4309-124">Если этот параметр не указан, данные извлекаются с начала дня или часа, указанного в *ReportedStartTime*.</span><span class="sxs-lookup"><span data-stu-id="e4309-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="e4309-125">Мы рекомендуем перейти к следующей ссылке в ответе на страницу "данные".</span><span class="sxs-lookup"><span data-stu-id="e4309-125">We recommend that you follow the next link in the response to page though the data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4309-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4309-126">-DefaultProfile</span></span>
<span data-ttu-id="e4309-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4309-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4309-128">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="e4309-128">-ReportedEndTime</span></span>
<span data-ttu-id="e4309-129">Указывает указанное время окончания регистрации использования ресурсов в системе выставления счетов Azure.</span><span class="sxs-lookup"><span data-stu-id="e4309-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>

<span data-ttu-id="e4309-130">Azure — это распределенная система, включающая в себя несколько центров обработки данных во всем мире, поэтому существует задержка между фактом использования ресурса, а также временем использования ресурсов, а также моментом, когда событие использования достигает системы выставления счетов, которое представляет собой указанное время использования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4309-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="e4309-131">Чтобы получить все события использования для подписки, о которой сообщается за определенный период времени, запрашивается указанное время.</span><span class="sxs-lookup"><span data-stu-id="e4309-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="e4309-132">Несмотря на то, что вы запрашиваете отчет в указанном времени, командлет объединит данные ответа по времени использования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4309-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="e4309-133">Данные об использовании ресурсов — это полезная сводная таблица для анализа данных.</span><span class="sxs-lookup"><span data-stu-id="e4309-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4309-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="e4309-134">-ReportedStartTime</span></span>
<span data-ttu-id="e4309-135">Указывает указанное время начала, по истечении которого в системе выставления счетов Azure была записана загрузка ресурса.</span><span class="sxs-lookup"><span data-stu-id="e4309-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4309-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="e4309-136">-ShowDetails</span></span>
<span data-ttu-id="e4309-137">Указывает, возвращает ли этот командлет сведения на уровне экземпляра с данными об использовании.</span><span class="sxs-lookup"><span data-stu-id="e4309-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>

<span data-ttu-id="e4309-138">Значение по умолчанию — $True.</span><span class="sxs-lookup"><span data-stu-id="e4309-138">The default value is $True.</span></span>

<span data-ttu-id="e4309-139">Если $False, служба объединит результаты на стороне сервера и, следовательно, возвращает меньше групп агрегатов.</span><span class="sxs-lookup"><span data-stu-id="e4309-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="e4309-140">Например, если вы используете три веб-сайта, по умолчанию вы будете получать три позиции для использования на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="e4309-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="e4309-141">Тем не менее, если значение $False, все данные для одного и того же **идентификатора подписки** , **meterId** , **usageStartTime** и **usageEndTime** сворачиваются в один элемент строки.</span><span class="sxs-lookup"><span data-stu-id="e4309-141">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4309-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4309-142">CommonParameters</span></span>
<span data-ttu-id="e4309-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4309-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4309-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4309-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4309-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4309-145">INPUTS</span></span>

### <span data-ttu-id="e4309-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="e4309-146">None</span></span>
<span data-ttu-id="e4309-147">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e4309-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4309-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4309-148">OUTPUTS</span></span>

### <span data-ttu-id="e4309-149">Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="e4309-149">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="e4309-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4309-150">NOTES</span></span>

## <span data-ttu-id="e4309-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4309-151">RELATED LINKS</span></span>

