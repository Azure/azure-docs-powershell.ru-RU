---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 510d0ee001e4c291dad3cc024f593d1f29c7ddca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909330"
---
# Get-UsageAggregates

## КРАТКИй обзор
Получает указанные данные об использовании подписки Azure.

## Максимальное

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-UsageAggregates** получает Объединенные данные об использовании подписки Azure следующими свойствами: 
- Время начала и окончания о том, когда была указана загрузка.
- Точность статистической обработки: ежедневно или ежечасно.
- Сведения об уровне экземпляра для нескольких экземпляров одного и того же ресурса.
Для противоречивых результатов возвращаемые данные основываются на том, когда ресурс Azure сообщил об использовании.
Дополнительные сведения можно найти в справочнике API для служб выставления счетов https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c для Azure ( https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) в сетевой библиотеке разработчиков Microsoft Developer.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение данных подписки
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

Эта команда извлекает сведения об использовании для подписки между 5/2/2015 и 5/5/2015.

## ПАРАМЕТРЫ

### -AggregationGranularity
Определяет точность статистического выражения для данных.
Допустимые значения: ежедневно и ежечасно.
По умолчанию используется значение ежедневно.

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

### -ContinuationToken
Указывает токен продолжения, полученный из тела ответа в предыдущем вызове.
Для большого набора результатов ответы размещаются на странице с помощью маркеров продолжения.
Маркер продолжения служит закладкой для выполнения.
Если этот параметр не указан, данные извлекаются с начала дня или часа, указанного в *ReportedStartTime*.
Мы рекомендуем перейти к следующей ссылке в ответе на страницу "данные".

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -ReportedEndTime
Указывает указанное время окончания регистрации использования ресурсов в системе выставления счетов Azure.
Azure — это распределенная система, включающая в себя несколько центров обработки данных во всем мире, поэтому существует задержка между фактом использования ресурса, а также временем использования ресурсов, а также моментом, когда событие использования достигает системы выставления счетов, которое представляет собой указанное время использования ресурсов.
Чтобы получить все события использования для подписки, о которой сообщается за определенный период времени, запрашивается указанное время.
Несмотря на то, что вы запрашиваете отчет в указанном времени, командлет объединит данные ответа по времени использования ресурсов.
Данные об использовании ресурсов — это полезная сводная таблица для анализа данных.

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

### -ReportedStartTime
Указывает указанное время начала, по истечении которого в системе выставления счетов Azure была записана загрузка ресурса.

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

### -ShowDetails
Указывает, возвращает ли этот командлет сведения на уровне экземпляра с данными об использовании.
Значение по умолчанию — $True.
Если $False, служба объединит результаты на стороне сервера и, следовательно, возвращает меньше групп агрегатов.
Например, если вы используете три веб-сайта, по умолчанию вы будете получать три позиции для использования на веб-сайте.
Тем не менее, если значение $False, все данные для одного и того же **идентификатора подписки** , **meterId** , **usageStartTime** и **usageEndTime** сворачиваются в один элемент строки.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commerce. UsageAggregates. Models. UsageAggregationGetResponse

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ