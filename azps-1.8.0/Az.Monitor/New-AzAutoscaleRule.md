---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: 2464a3b7fb35cce28dd06884cd8ed69e5197eced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899497"
---
# <span data-ttu-id="92e1b-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="92e1b-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="92e1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="92e1b-103">Создает правило автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="92e1b-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="92e1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92e1b-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e1b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92e1b-105">DESCRIPTION</span></span>
<span data-ttu-id="92e1b-106">Командлет **New-AzAutoscaleRule** создает правило автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="92e1b-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="92e1b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92e1b-107">EXAMPLES</span></span>

### <span data-ttu-id="92e1b-108">Пример 1: Создание правила</span><span class="sxs-lookup"><span data-stu-id="92e1b-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="92e1b-109">Эта команда создает правило.</span><span class="sxs-lookup"><span data-stu-id="92e1b-109">This command creates a rule.</span></span>

### <span data-ttu-id="92e1b-110">Пример 2: создание двух правил</span><span class="sxs-lookup"><span data-stu-id="92e1b-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="92e1b-111">Первая команда создает правило для метрики запросов, а затем сохраняет его в переменной $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="92e1b-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="92e1b-112">Вторая команда создает второе правило для метрики запросов, а затем сохраняет его в переменной $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="92e1b-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="92e1b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92e1b-113">PARAMETERS</span></span>

### <span data-ttu-id="92e1b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e1b-114">-DefaultProfile</span></span>
<span data-ttu-id="92e1b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="92e1b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92e1b-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="92e1b-116">-MetricName</span></span>
<span data-ttu-id="92e1b-117">Указывает имя метрики.</span><span class="sxs-lookup"><span data-stu-id="92e1b-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="92e1b-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="92e1b-118">-MetricResourceId</span></span>
<span data-ttu-id="92e1b-119">Указывает идентификатор ресурса метрики.</span><span class="sxs-lookup"><span data-stu-id="92e1b-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="92e1b-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="92e1b-120">-MetricStatistic</span></span>
<span data-ttu-id="92e1b-121">Указывает статистику метрики.</span><span class="sxs-lookup"><span data-stu-id="92e1b-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="92e1b-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="92e1b-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92e1b-123">Среднем</span><span class="sxs-lookup"><span data-stu-id="92e1b-123">Average</span></span>
- <span data-ttu-id="92e1b-124">Наименьш</span><span class="sxs-lookup"><span data-stu-id="92e1b-124">Min</span></span>
- <span data-ttu-id="92e1b-125">Развертывания</span><span class="sxs-lookup"><span data-stu-id="92e1b-125">Max</span></span>
- <span data-ttu-id="92e1b-126">Сумма</span><span class="sxs-lookup"><span data-stu-id="92e1b-126">Sum</span></span>

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

### <span data-ttu-id="92e1b-127">-Operator</span><span class="sxs-lookup"><span data-stu-id="92e1b-127">-Operator</span></span>
<span data-ttu-id="92e1b-128">Указывает оператор.</span><span class="sxs-lookup"><span data-stu-id="92e1b-128">Specifies the operator.</span></span>
<span data-ttu-id="92e1b-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="92e1b-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92e1b-130">Соответствует</span><span class="sxs-lookup"><span data-stu-id="92e1b-130">Equals</span></span>
- <span data-ttu-id="92e1b-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="92e1b-131">NotEquals</span></span>
- <span data-ttu-id="92e1b-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="92e1b-132">GreaterThan</span></span>
- <span data-ttu-id="92e1b-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="92e1b-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="92e1b-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="92e1b-134">LessThan</span></span>
- <span data-ttu-id="92e1b-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="92e1b-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="92e1b-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="92e1b-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="92e1b-137">Задает время cooldown действия автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="92e1b-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="92e1b-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="92e1b-138">-ScaleActionDirection</span></span>
<span data-ttu-id="92e1b-139">Задает направление действия масштабирования.</span><span class="sxs-lookup"><span data-stu-id="92e1b-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="92e1b-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="92e1b-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92e1b-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="92e1b-141">None</span></span>
- <span data-ttu-id="92e1b-142">Освободит</span><span class="sxs-lookup"><span data-stu-id="92e1b-142">Increase</span></span>
- <span data-ttu-id="92e1b-143">Уменьшить</span><span class="sxs-lookup"><span data-stu-id="92e1b-143">Decrease</span></span>

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

### <span data-ttu-id="92e1b-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="92e1b-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="92e1b-145">Указывает тип шкалы.</span><span class="sxs-lookup"><span data-stu-id="92e1b-145">Specifies the scale type.</span></span>
<span data-ttu-id="92e1b-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="92e1b-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92e1b-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="92e1b-147">ChangeSize</span></span>
- <span data-ttu-id="92e1b-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="92e1b-148">ChangeCount</span></span>
- <span data-ttu-id="92e1b-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="92e1b-149">PercentChangeCount</span></span>
- <span data-ttu-id="92e1b-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="92e1b-150">ExactCount</span></span>

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

### <span data-ttu-id="92e1b-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="92e1b-151">-ScaleActionValue</span></span>
<span data-ttu-id="92e1b-152">Задает значение действия.</span><span class="sxs-lookup"><span data-stu-id="92e1b-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="92e1b-153">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="92e1b-153">-Threshold</span></span>
<span data-ttu-id="92e1b-154">Указывает порог значения метрики.</span><span class="sxs-lookup"><span data-stu-id="92e1b-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="92e1b-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="92e1b-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="92e1b-156">Указывает оператор агрегата времени.</span><span class="sxs-lookup"><span data-stu-id="92e1b-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="92e1b-157">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="92e1b-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92e1b-158">Среднем</span><span class="sxs-lookup"><span data-stu-id="92e1b-158">Average</span></span>
- <span data-ttu-id="92e1b-159">Минимум</span><span class="sxs-lookup"><span data-stu-id="92e1b-159">Minimum</span></span>
- <span data-ttu-id="92e1b-160">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92e1b-160">Maximum</span></span>
- <span data-ttu-id="92e1b-161">Времени</span><span class="sxs-lookup"><span data-stu-id="92e1b-161">Last</span></span>
- <span data-ttu-id="92e1b-162">Итого, количество</span><span class="sxs-lookup"><span data-stu-id="92e1b-162">Total, Count</span></span>

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

### <span data-ttu-id="92e1b-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="92e1b-163">-TimeGrain</span></span>
<span data-ttu-id="92e1b-164">Указывает промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="92e1b-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="92e1b-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="92e1b-165">-TimeWindow</span></span>
<span data-ttu-id="92e1b-166">Указывает окно времени.</span><span class="sxs-lookup"><span data-stu-id="92e1b-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="92e1b-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e1b-167">CommonParameters</span></span>
<span data-ttu-id="92e1b-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92e1b-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e1b-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e1b-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e1b-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92e1b-170">INPUTS</span></span>

### <span data-ttu-id="92e1b-171">System. String</span><span class="sxs-lookup"><span data-stu-id="92e1b-171">System.String</span></span>

### <span data-ttu-id="92e1b-172">Microsoft. Azure. Management. Monitor. Management. Models. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="92e1b-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="92e1b-173">Microsoft. Azure. Management. Monitor. Management. Models. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="92e1b-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="92e1b-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="92e1b-174">System.Double</span></span>

### <span data-ttu-id="92e1b-175">Microsoft. Azure. Management. Monitor. Management. Models. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="92e1b-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="92e1b-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="92e1b-176">System.TimeSpan</span></span>

### <span data-ttu-id="92e1b-177">Microsoft. Azure. Management. Monitor. Management. Models. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="92e1b-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="92e1b-178">Microsoft. Azure. Management. Monitor. Management. Models. ScaleType</span><span class="sxs-lookup"><span data-stu-id="92e1b-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="92e1b-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92e1b-179">OUTPUTS</span></span>

### <span data-ttu-id="92e1b-180">Microsoft. Azure. Management. Monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="92e1b-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="92e1b-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="92e1b-181">NOTES</span></span>

## <span data-ttu-id="92e1b-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92e1b-182">RELATED LINKS</span></span>

[<span data-ttu-id="92e1b-183">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="92e1b-183">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="92e1b-184">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="92e1b-184">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="92e1b-185">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="92e1b-185">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="92e1b-186">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="92e1b-186">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="92e1b-187">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="92e1b-187">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


