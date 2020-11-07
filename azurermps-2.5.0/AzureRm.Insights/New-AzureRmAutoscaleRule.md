---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
ms.openlocfilehash: 785424560ebd0af3ce7035265e9fb64b22713049
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913891"
---
# <span data-ttu-id="abd6c-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="abd6c-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="abd6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="abd6c-102">SYNOPSIS</span></span>
<span data-ttu-id="abd6c-103">Создает правило автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="abd6c-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abd6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abd6c-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abd6c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abd6c-105">DESCRIPTION</span></span>
<span data-ttu-id="abd6c-106">Командлет **New-AzureRmAutoscaleRule** создает правило автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="abd6c-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="abd6c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="abd6c-107">EXAMPLES</span></span>

### <span data-ttu-id="abd6c-108">Пример 1: Создание правила</span><span class="sxs-lookup"><span data-stu-id="abd6c-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="abd6c-109">Эта команда создает правило.</span><span class="sxs-lookup"><span data-stu-id="abd6c-109">This command creates a rule.</span></span>

### <span data-ttu-id="abd6c-110">Пример 2: создание двух правил</span><span class="sxs-lookup"><span data-stu-id="abd6c-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="abd6c-111">Первая команда создает правило для метрики запросов, а затем сохраняет его в переменной $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="abd6c-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="abd6c-112">Вторая команда создает второе правило для метрики запросов, а затем сохраняет его в переменной $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="abd6c-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="abd6c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="abd6c-113">PARAMETERS</span></span>

### <span data-ttu-id="abd6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd6c-114">-DefaultProfile</span></span>
<span data-ttu-id="abd6c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="abd6c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abd6c-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="abd6c-116">-MetricName</span></span>
<span data-ttu-id="abd6c-117">Указывает имя метрики.</span><span class="sxs-lookup"><span data-stu-id="abd6c-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="abd6c-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="abd6c-118">-MetricResourceId</span></span>
<span data-ttu-id="abd6c-119">Указывает идентификатор ресурса метрики.</span><span class="sxs-lookup"><span data-stu-id="abd6c-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="abd6c-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="abd6c-120">-MetricStatistic</span></span>
<span data-ttu-id="abd6c-121">Указывает статистику метрики.</span><span class="sxs-lookup"><span data-stu-id="abd6c-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="abd6c-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="abd6c-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abd6c-123">Среднем</span><span class="sxs-lookup"><span data-stu-id="abd6c-123">Average</span></span>
- <span data-ttu-id="abd6c-124">Наименьш</span><span class="sxs-lookup"><span data-stu-id="abd6c-124">Min</span></span>
- <span data-ttu-id="abd6c-125">Развертывания</span><span class="sxs-lookup"><span data-stu-id="abd6c-125">Max</span></span>
- <span data-ttu-id="abd6c-126">Сумма</span><span class="sxs-lookup"><span data-stu-id="abd6c-126">Sum</span></span>

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

### <span data-ttu-id="abd6c-127">-Operator</span><span class="sxs-lookup"><span data-stu-id="abd6c-127">-Operator</span></span>
<span data-ttu-id="abd6c-128">Указывает оператор.</span><span class="sxs-lookup"><span data-stu-id="abd6c-128">Specifies the operator.</span></span>
<span data-ttu-id="abd6c-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="abd6c-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abd6c-130">Соответствует</span><span class="sxs-lookup"><span data-stu-id="abd6c-130">Equals</span></span>
- <span data-ttu-id="abd6c-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="abd6c-131">NotEquals</span></span>
- <span data-ttu-id="abd6c-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="abd6c-132">GreaterThan</span></span>
- <span data-ttu-id="abd6c-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="abd6c-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="abd6c-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="abd6c-134">LessThan</span></span>
- <span data-ttu-id="abd6c-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="abd6c-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="abd6c-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="abd6c-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="abd6c-137">Задает время cooldown действия автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="abd6c-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="abd6c-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="abd6c-138">-ScaleActionDirection</span></span>
<span data-ttu-id="abd6c-139">Задает направление действия масштабирования.</span><span class="sxs-lookup"><span data-stu-id="abd6c-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="abd6c-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="abd6c-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abd6c-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="abd6c-141">None</span></span>
- <span data-ttu-id="abd6c-142">Освободит</span><span class="sxs-lookup"><span data-stu-id="abd6c-142">Increase</span></span>
- <span data-ttu-id="abd6c-143">Уменьшить</span><span class="sxs-lookup"><span data-stu-id="abd6c-143">Decrease</span></span>

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

### <span data-ttu-id="abd6c-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="abd6c-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="abd6c-145">Указывает тип шкалы.</span><span class="sxs-lookup"><span data-stu-id="abd6c-145">Specifies the scale type.</span></span>
<span data-ttu-id="abd6c-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="abd6c-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abd6c-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="abd6c-147">ChangeSize</span></span>
- <span data-ttu-id="abd6c-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="abd6c-148">ChangeCount</span></span>
- <span data-ttu-id="abd6c-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="abd6c-149">PercentChangeCount</span></span>
- <span data-ttu-id="abd6c-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="abd6c-150">ExactCount</span></span>

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

### <span data-ttu-id="abd6c-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="abd6c-151">-ScaleActionValue</span></span>
<span data-ttu-id="abd6c-152">Задает значение действия.</span><span class="sxs-lookup"><span data-stu-id="abd6c-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="abd6c-153">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="abd6c-153">-Threshold</span></span>
<span data-ttu-id="abd6c-154">Указывает порог значения метрики.</span><span class="sxs-lookup"><span data-stu-id="abd6c-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="abd6c-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="abd6c-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="abd6c-156">Указывает оператор агрегата времени.</span><span class="sxs-lookup"><span data-stu-id="abd6c-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="abd6c-157">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="abd6c-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="abd6c-158">Среднем</span><span class="sxs-lookup"><span data-stu-id="abd6c-158">Average</span></span>
- <span data-ttu-id="abd6c-159">Минимум</span><span class="sxs-lookup"><span data-stu-id="abd6c-159">Minimum</span></span>
- <span data-ttu-id="abd6c-160">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abd6c-160">Maximum</span></span>
- <span data-ttu-id="abd6c-161">Времени</span><span class="sxs-lookup"><span data-stu-id="abd6c-161">Last</span></span>
- <span data-ttu-id="abd6c-162">Итого, количество</span><span class="sxs-lookup"><span data-stu-id="abd6c-162">Total, Count</span></span>

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

### <span data-ttu-id="abd6c-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="abd6c-163">-TimeGrain</span></span>
<span data-ttu-id="abd6c-164">Указывает промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="abd6c-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="abd6c-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="abd6c-165">-TimeWindow</span></span>
<span data-ttu-id="abd6c-166">Указывает окно времени.</span><span class="sxs-lookup"><span data-stu-id="abd6c-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="abd6c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd6c-167">CommonParameters</span></span>
<span data-ttu-id="abd6c-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="abd6c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd6c-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd6c-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd6c-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="abd6c-170">INPUTS</span></span>

### <span data-ttu-id="abd6c-171">System. String</span><span class="sxs-lookup"><span data-stu-id="abd6c-171">System.String</span></span>

### <span data-ttu-id="abd6c-172">Microsoft. Azure. Management. Monitor. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="abd6c-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="abd6c-173">Microsoft. Azure. Management. Monitor. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="abd6c-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="abd6c-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="abd6c-174">System.Double</span></span>

### <span data-ttu-id="abd6c-175">Microsoft. Azure. Management. Monitor. Management. Models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="abd6c-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="abd6c-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="abd6c-176">System.TimeSpan</span></span>

### <span data-ttu-id="abd6c-177">Microsoft. Azure. Management. Monitor. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="abd6c-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="abd6c-178">Microsoft. Azure. Management. Monitor. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="abd6c-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="abd6c-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="abd6c-179">OUTPUTS</span></span>

### <span data-ttu-id="abd6c-180">Microsoft. Azure. Management. Monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="abd6c-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="abd6c-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="abd6c-181">NOTES</span></span>

## <span data-ttu-id="abd6c-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abd6c-182">RELATED LINKS</span></span>

[<span data-ttu-id="abd6c-183">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="abd6c-183">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="abd6c-184">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="abd6c-184">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="abd6c-185">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="abd6c-185">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="abd6c-186">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="abd6c-186">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="abd6c-187">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="abd6c-187">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


