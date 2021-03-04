---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: 193c0c8b263f7ceee62cc7cb99c47769a22c7633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982648"
---
# <span data-ttu-id="c5812-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="c5812-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="c5812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5812-102">SYNOPSIS</span></span>
<span data-ttu-id="c5812-103">Создает правило автомасштабии.</span><span class="sxs-lookup"><span data-stu-id="c5812-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="c5812-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5812-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5812-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5812-105">DESCRIPTION</span></span>
<span data-ttu-id="c5812-106">Для создания правила автоматической шкалы будет создаваться **cmdlet New-AzAutoscaleRule.**</span><span class="sxs-lookup"><span data-stu-id="c5812-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="c5812-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5812-107">EXAMPLES</span></span>

### <span data-ttu-id="c5812-108">Пример 1. Создание правила</span><span class="sxs-lookup"><span data-stu-id="c5812-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="c5812-109">Эта команда создает правило.</span><span class="sxs-lookup"><span data-stu-id="c5812-109">This command creates a rule.</span></span>

### <span data-ttu-id="c5812-110">Пример 2. Создание двух правил</span><span class="sxs-lookup"><span data-stu-id="c5812-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="c5812-111">Первая команда создает правило для метрики "Запросы", а затем сохраняет его в переменной $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="c5812-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="c5812-112">Вторая команда создает второе правило для метрики "Запросы", а затем сохраняет его в переменной $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="c5812-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="c5812-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c5812-113">Example 3</span></span>

<span data-ttu-id="c5812-114">Создает правило автомасштабии.</span><span class="sxs-lookup"><span data-stu-id="c5812-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="c5812-115">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c5812-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="c5812-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5812-116">PARAMETERS</span></span>

### <span data-ttu-id="c5812-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5812-117">-DefaultProfile</span></span>
<span data-ttu-id="c5812-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c5812-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5812-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="c5812-119">-MetricName</span></span>
<span data-ttu-id="c5812-120">Указывает имя метрик.</span><span class="sxs-lookup"><span data-stu-id="c5812-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="c5812-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="c5812-121">-MetricResourceId</span></span>
<span data-ttu-id="c5812-122">Определяет метрическую единицу ресурса.</span><span class="sxs-lookup"><span data-stu-id="c5812-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="c5812-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="c5812-123">-MetricStatistic</span></span>
<span data-ttu-id="c5812-124">Указывает метрическую статистику.</span><span class="sxs-lookup"><span data-stu-id="c5812-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="c5812-125">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c5812-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c5812-126">Среднее значение</span><span class="sxs-lookup"><span data-stu-id="c5812-126">Average</span></span>
- <span data-ttu-id="c5812-127">Min</span><span class="sxs-lookup"><span data-stu-id="c5812-127">Min</span></span>
- <span data-ttu-id="c5812-128">Максимум</span><span class="sxs-lookup"><span data-stu-id="c5812-128">Max</span></span>
- <span data-ttu-id="c5812-129">Сумма</span><span class="sxs-lookup"><span data-stu-id="c5812-129">Sum</span></span>

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

### <span data-ttu-id="c5812-130">-Operator</span><span class="sxs-lookup"><span data-stu-id="c5812-130">-Operator</span></span>
<span data-ttu-id="c5812-131">Оператор.</span><span class="sxs-lookup"><span data-stu-id="c5812-131">Specifies the operator.</span></span>
<span data-ttu-id="c5812-132">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c5812-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c5812-133">Равно</span><span class="sxs-lookup"><span data-stu-id="c5812-133">Equals</span></span>
- <span data-ttu-id="c5812-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="c5812-134">NotEquals</span></span>
- <span data-ttu-id="c5812-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="c5812-135">GreaterThan</span></span>
- <span data-ttu-id="c5812-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="c5812-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="c5812-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="c5812-137">LessThan</span></span>
- <span data-ttu-id="c5812-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="c5812-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="c5812-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="c5812-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="c5812-140">Время завершения действия по шкале автомасштаба.</span><span class="sxs-lookup"><span data-stu-id="c5812-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="c5812-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="c5812-141">-ScaleActionDirection</span></span>
<span data-ttu-id="c5812-142">Определяет направление действия масштаба.</span><span class="sxs-lookup"><span data-stu-id="c5812-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="c5812-143">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c5812-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c5812-144">Нет</span><span class="sxs-lookup"><span data-stu-id="c5812-144">None</span></span>
- <span data-ttu-id="c5812-145">Увеличить</span><span class="sxs-lookup"><span data-stu-id="c5812-145">Increase</span></span>
- <span data-ttu-id="c5812-146">Уменьшить</span><span class="sxs-lookup"><span data-stu-id="c5812-146">Decrease</span></span>

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

### <span data-ttu-id="c5812-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="c5812-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="c5812-148">Определяет тип шкалы.</span><span class="sxs-lookup"><span data-stu-id="c5812-148">Specifies the scale type.</span></span>
<span data-ttu-id="c5812-149">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c5812-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c5812-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="c5812-150">ChangeSize</span></span>
- <span data-ttu-id="c5812-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="c5812-151">ChangeCount</span></span>
- <span data-ttu-id="c5812-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="c5812-152">PercentChangeCount</span></span>
- <span data-ttu-id="c5812-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="c5812-153">ExactCount</span></span>

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

### <span data-ttu-id="c5812-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="c5812-154">-ScaleActionValue</span></span>
<span data-ttu-id="c5812-155">Определяет значение действия.</span><span class="sxs-lookup"><span data-stu-id="c5812-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="c5812-156">-Пороговое значение</span><span class="sxs-lookup"><span data-stu-id="c5812-156">-Threshold</span></span>
<span data-ttu-id="c5812-157">Пороговое значение метрик.</span><span class="sxs-lookup"><span data-stu-id="c5812-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="c5812-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="c5812-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="c5812-159">Определяет оператор агрегирования времени.</span><span class="sxs-lookup"><span data-stu-id="c5812-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="c5812-160">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="c5812-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c5812-161">Среднее значение</span><span class="sxs-lookup"><span data-stu-id="c5812-161">Average</span></span>
- <span data-ttu-id="c5812-162">Минимум</span><span class="sxs-lookup"><span data-stu-id="c5812-162">Minimum</span></span>
- <span data-ttu-id="c5812-163">Максимальное значение</span><span class="sxs-lookup"><span data-stu-id="c5812-163">Maximum</span></span>
- <span data-ttu-id="c5812-164">Last</span><span class="sxs-lookup"><span data-stu-id="c5812-164">Last</span></span>
- <span data-ttu-id="c5812-165">Итого, количество</span><span class="sxs-lookup"><span data-stu-id="c5812-165">Total, Count</span></span>

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

### <span data-ttu-id="c5812-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c5812-166">-TimeGrain</span></span>
<span data-ttu-id="c5812-167">Определяет время, указанное в этом проекте.</span><span class="sxs-lookup"><span data-stu-id="c5812-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="c5812-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="c5812-168">-TimeWindow</span></span>
<span data-ttu-id="c5812-169">Указывает время.</span><span class="sxs-lookup"><span data-stu-id="c5812-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="c5812-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5812-170">CommonParameters</span></span>
<span data-ttu-id="c5812-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5812-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5812-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5812-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5812-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5812-173">INPUTS</span></span>

### <span data-ttu-id="c5812-174">System.String</span><span class="sxs-lookup"><span data-stu-id="c5812-174">System.String</span></span>

### <span data-ttu-id="c5812-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="c5812-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="c5812-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="c5812-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="c5812-177">System.Double</span><span class="sxs-lookup"><span data-stu-id="c5812-177">System.Double</span></span>

### <span data-ttu-id="c5812-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="c5812-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="c5812-179">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="c5812-179">System.TimeSpan</span></span>

### <span data-ttu-id="c5812-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="c5812-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="c5812-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span><span class="sxs-lookup"><span data-stu-id="c5812-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="c5812-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5812-182">OUTPUTS</span></span>

### <span data-ttu-id="c5812-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span><span class="sxs-lookup"><span data-stu-id="c5812-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="c5812-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5812-184">NOTES</span></span>

## <span data-ttu-id="c5812-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5812-185">RELATED LINKS</span></span>

[<span data-ttu-id="c5812-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c5812-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="c5812-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="c5812-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="c5812-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c5812-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="c5812-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="c5812-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="c5812-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="c5812-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


