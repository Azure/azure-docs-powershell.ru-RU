---
external help file: Microsoft.Azure.Commands.UsageAggregates.dll-Help.xml
Module Name: AzureRM.UsageAggregates
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/UsageAggregates/Commands.UsageAggregates/help/Get-UsageAggregates.md
ms.openlocfilehash: 1c5c705ec55889182a38d1586559f59d57e2d366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561987"
---
# <span data-ttu-id="cc3cd-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="cc3cd-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="cc3cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc3cd-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3cd-103">Получает указанные данные об использовании подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-103">Gets the reported Azure subscription usage details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc3cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc3cd-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc3cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc3cd-105">DESCRIPTION</span></span>
<span data-ttu-id="cc3cd-106">Командлет **Get-UsageAggregates** получает Объединенные данные об использовании подписки Azure следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="cc3cd-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 

- <span data-ttu-id="cc3cd-107">Время начала и окончания о том, когда была указана загрузка.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-107">Start and end times of when the usage was reported.</span></span>

- <span data-ttu-id="cc3cd-108">Точность статистической обработки: ежедневно или ежечасно.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-108">Aggregation precision, either daily or hourly.</span></span>

- <span data-ttu-id="cc3cd-109">Сведения об уровне экземпляра для нескольких экземпляров одного и того же ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-109">Instance level detail for multiple instances of the same resource.</span></span>

<span data-ttu-id="cc3cd-110">Для противоречивых результатов возвращаемые данные основываются на том, когда ресурс Azure сообщил об использовании.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>

<span data-ttu-id="cc3cd-111">Дополнительные сведения можно найти в справочнике API для служб выставления счетов https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c для Azure ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) в сетевой библиотеке разработчиков Microsoft Developer.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="cc3cd-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc3cd-112">EXAMPLES</span></span>

### <span data-ttu-id="cc3cd-113">Пример 1: получение данных подписки</span><span class="sxs-lookup"><span data-stu-id="cc3cd-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="cc3cd-114">Эта команда извлекает сведения об использовании для подписки между 5/2/2015 и 5/5/2015.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="cc3cd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc3cd-115">PARAMETERS</span></span>

### <span data-ttu-id="cc3cd-116">-AggregationGranularity</span><span class="sxs-lookup"><span data-stu-id="cc3cd-116">-AggregationGranularity</span></span>
<span data-ttu-id="cc3cd-117">Определяет точность статистического выражения для данных.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="cc3cd-118">Допустимые значения: ежедневно и ежечасно.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-118">Valid values are: Daily and Hourly.</span></span>

<span data-ttu-id="cc3cd-119">По умолчанию используется значение ежедневно.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-119">The default value is Daily.</span></span>

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

### <span data-ttu-id="cc3cd-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="cc3cd-120">-ContinuationToken</span></span>
<span data-ttu-id="cc3cd-121">Указывает токен продолжения, полученный из тела ответа в предыдущем вызове.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="cc3cd-122">Для большого набора результатов ответы размещаются на странице с помощью маркеров продолжения.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="cc3cd-123">Маркер продолжения служит закладкой для выполнения.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="cc3cd-124">Если этот параметр не указан, данные извлекаются с начала дня или часа, указанного в *ReportedStartTime*.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="cc3cd-125">Мы рекомендуем перейти к следующей ссылке в ответе на страницу "данные".</span><span class="sxs-lookup"><span data-stu-id="cc3cd-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="cc3cd-126">-ReportedEndTime</span><span class="sxs-lookup"><span data-stu-id="cc3cd-126">-ReportedEndTime</span></span>
<span data-ttu-id="cc3cd-127">Указывает указанное время окончания регистрации использования ресурсов в системе выставления счетов Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-127">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>

<span data-ttu-id="cc3cd-128">Azure — это распределенная система, включающая в себя несколько центров обработки данных во всем мире, поэтому существует задержка между фактом использования ресурса, а также временем использования ресурсов, а также моментом, когда событие использования достигает системы выставления счетов, которое представляет собой указанное время использования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-128">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="cc3cd-129">Чтобы получить все события использования для подписки, о которой сообщается за определенный период времени, запрашивается указанное время.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-129">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="cc3cd-130">Несмотря на то, что вы запрашиваете отчет в указанном времени, командлет объединит данные ответа по времени использования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-130">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="cc3cd-131">Данные об использовании ресурсов — это полезная сводная таблица для анализа данных.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-131">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="cc3cd-132">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="cc3cd-132">-ReportedStartTime</span></span>
<span data-ttu-id="cc3cd-133">Указывает указанное время начала, по истечении которого в системе выставления счетов Azure была записана загрузка ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-133">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="cc3cd-134">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="cc3cd-134">-ShowDetails</span></span>
<span data-ttu-id="cc3cd-135">Указывает, возвращает ли этот командлет сведения на уровне экземпляра с данными об использовании.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-135">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>

<span data-ttu-id="cc3cd-136">Значение по умолчанию — $True.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-136">The default value is $True.</span></span>

<span data-ttu-id="cc3cd-137">Если $False, служба объединит результаты на стороне сервера и, следовательно, возвращает меньше групп агрегатов.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-137">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="cc3cd-138">Например, если вы используете три веб-сайта, по умолчанию вы будете получать три позиции для использования на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-138">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="cc3cd-139">Тем не менее, если значение $False, все данные для одного и того же **идентификатора подписки** , **meterId** , **usageStartTime** и **usageEndTime** сворачиваются в один элемент строки.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-139">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

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

### <span data-ttu-id="cc3cd-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc3cd-140">-DefaultProfile</span></span>
<span data-ttu-id="cc3cd-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc3cd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3cd-142">CommonParameters</span></span>
<span data-ttu-id="cc3cd-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3cd-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc3cd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3cd-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc3cd-145">INPUTS</span></span>

## <span data-ttu-id="cc3cd-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc3cd-146">OUTPUTS</span></span>

### <span data-ttu-id="cc3cd-147">Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse</span><span class="sxs-lookup"><span data-stu-id="cc3cd-147">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="cc3cd-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc3cd-148">NOTES</span></span>

## <span data-ttu-id="cc3cd-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc3cd-149">RELATED LINKS</span></span>

