---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568776"
---
# <span data-ttu-id="d4f12-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="d4f12-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="d4f12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4f12-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f12-103">Создает правило автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="d4f12-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4f12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4f12-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4f12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4f12-105">DESCRIPTION</span></span>
<span data-ttu-id="d4f12-106">Командлет **New-AzureRmAutoscaleRule** создает правило автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="d4f12-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="d4f12-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4f12-107">EXAMPLES</span></span>

### <span data-ttu-id="d4f12-108">Пример 1: Создание правила</span><span class="sxs-lookup"><span data-stu-id="d4f12-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="d4f12-109">Эта команда создает правило.</span><span class="sxs-lookup"><span data-stu-id="d4f12-109">This command creates a rule.</span></span>

### <span data-ttu-id="d4f12-110">Пример 2: создание двух правил</span><span class="sxs-lookup"><span data-stu-id="d4f12-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="d4f12-111">Первая команда создает правило для метрики запросов, а затем сохраняет его в переменной $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="d4f12-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="d4f12-112">Вторая команда создает второе правило для метрики запросов, а затем сохраняет его в переменной $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="d4f12-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="d4f12-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4f12-113">PARAMETERS</span></span>

### <span data-ttu-id="d4f12-114">-MetricName</span><span class="sxs-lookup"><span data-stu-id="d4f12-114">-MetricName</span></span>
<span data-ttu-id="d4f12-115">Указывает имя метрики.</span><span class="sxs-lookup"><span data-stu-id="d4f12-115">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-116">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="d4f12-116">-MetricResourceId</span></span>
<span data-ttu-id="d4f12-117">Указывает идентификатор ресурса метрики.</span><span class="sxs-lookup"><span data-stu-id="d4f12-117">Specifies the metric resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-118">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="d4f12-118">-MetricStatistic</span></span>
<span data-ttu-id="d4f12-119">Указывает статистику метрики.</span><span class="sxs-lookup"><span data-stu-id="d4f12-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="d4f12-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d4f12-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4f12-121">Среднем</span><span class="sxs-lookup"><span data-stu-id="d4f12-121">Average</span></span>
- <span data-ttu-id="d4f12-122">Наименьш</span><span class="sxs-lookup"><span data-stu-id="d4f12-122">Min</span></span>
- <span data-ttu-id="d4f12-123">Развертывания</span><span class="sxs-lookup"><span data-stu-id="d4f12-123">Max</span></span>
- <span data-ttu-id="d4f12-124">Сумма</span><span class="sxs-lookup"><span data-stu-id="d4f12-124">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-125">-Operator</span><span class="sxs-lookup"><span data-stu-id="d4f12-125">-Operator</span></span>
<span data-ttu-id="d4f12-126">Указывает оператор.</span><span class="sxs-lookup"><span data-stu-id="d4f12-126">Specifies the operator.</span></span>
<span data-ttu-id="d4f12-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d4f12-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4f12-128">Соответствует</span><span class="sxs-lookup"><span data-stu-id="d4f12-128">Equals</span></span>
- <span data-ttu-id="d4f12-129">NotEquals</span><span class="sxs-lookup"><span data-stu-id="d4f12-129">NotEquals</span></span>
- <span data-ttu-id="d4f12-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="d4f12-130">GreaterThan</span></span>
- <span data-ttu-id="d4f12-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="d4f12-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="d4f12-132">LessThan</span><span class="sxs-lookup"><span data-stu-id="d4f12-132">LessThan</span></span>
- <span data-ttu-id="d4f12-133">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="d4f12-133">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-134">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="d4f12-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="d4f12-135">Задает время cooldown действия автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="d4f12-135">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="d4f12-136">-ScaleActionDirection</span></span>
<span data-ttu-id="d4f12-137">Задает направление действия масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d4f12-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="d4f12-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d4f12-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4f12-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="d4f12-139">None</span></span>
- <span data-ttu-id="d4f12-140">Освободит</span><span class="sxs-lookup"><span data-stu-id="d4f12-140">Increase</span></span>
- <span data-ttu-id="d4f12-141">Уменьшить</span><span class="sxs-lookup"><span data-stu-id="d4f12-141">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="d4f12-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="d4f12-143">Указывает тип шкалы.</span><span class="sxs-lookup"><span data-stu-id="d4f12-143">Specifies the scale type.</span></span>
<span data-ttu-id="d4f12-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d4f12-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4f12-145">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="d4f12-145">ChangeSize</span></span>
- <span data-ttu-id="d4f12-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="d4f12-146">ChangeCount</span></span>
- <span data-ttu-id="d4f12-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="d4f12-147">PercentChangeCount</span></span>
- <span data-ttu-id="d4f12-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="d4f12-148">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="d4f12-149">-ScaleActionValue</span></span>
<span data-ttu-id="d4f12-150">Задает значение действия.</span><span class="sxs-lookup"><span data-stu-id="d4f12-150">Specifies the action value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-151">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="d4f12-151">-Threshold</span></span>
<span data-ttu-id="d4f12-152">Указывает порог значения метрики.</span><span class="sxs-lookup"><span data-stu-id="d4f12-152">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="d4f12-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="d4f12-154">Указывает оператор агрегата времени.</span><span class="sxs-lookup"><span data-stu-id="d4f12-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="d4f12-155">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d4f12-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4f12-156">Среднем</span><span class="sxs-lookup"><span data-stu-id="d4f12-156">Average</span></span>
- <span data-ttu-id="d4f12-157">Минимум</span><span class="sxs-lookup"><span data-stu-id="d4f12-157">Minimum</span></span>
- <span data-ttu-id="d4f12-158">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4f12-158">Maximum</span></span>
- <span data-ttu-id="d4f12-159">Времени</span><span class="sxs-lookup"><span data-stu-id="d4f12-159">Last</span></span>
- <span data-ttu-id="d4f12-160">Итого, количество</span><span class="sxs-lookup"><span data-stu-id="d4f12-160">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-161">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="d4f12-161">-TimeGrain</span></span>
<span data-ttu-id="d4f12-162">Указывает промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="d4f12-162">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4f12-163">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="d4f12-163">-TimeWindow</span></span>
<span data-ttu-id="d4f12-164">Указывает окно времени.</span><span class="sxs-lookup"><span data-stu-id="d4f12-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="d4f12-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f12-165">-DefaultProfile</span></span>
<span data-ttu-id="d4f12-166">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4f12-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4f12-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f12-167">CommonParameters</span></span>
<span data-ttu-id="d4f12-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4f12-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f12-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4f12-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f12-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4f12-170">INPUTS</span></span>

## <span data-ttu-id="d4f12-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4f12-171">OUTPUTS</span></span>

### <span data-ttu-id="d4f12-172">Microsoft. Azure. Management. Monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="d4f12-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="d4f12-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4f12-173">NOTES</span></span>

## <span data-ttu-id="d4f12-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4f12-174">RELATED LINKS</span></span>

[<span data-ttu-id="d4f12-175">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d4f12-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="d4f12-176">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="d4f12-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="d4f12-177">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d4f12-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="d4f12-178">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="d4f12-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="d4f12-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d4f12-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


