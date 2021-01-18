---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505069"
---
# <span data-ttu-id="f29eb-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="f29eb-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="f29eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f29eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f29eb-103">Создает правило автомасштабии.</span><span class="sxs-lookup"><span data-stu-id="f29eb-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="f29eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f29eb-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f29eb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f29eb-105">DESCRIPTION</span></span>
<span data-ttu-id="f29eb-106">Для создания правила автоматической шкалы будет создаваться **cmdlet New-AzAutoscaleRule.**</span><span class="sxs-lookup"><span data-stu-id="f29eb-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="f29eb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f29eb-107">EXAMPLES</span></span>

### <span data-ttu-id="f29eb-108">Пример 1. Создание правила</span><span class="sxs-lookup"><span data-stu-id="f29eb-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="f29eb-109">Эта команда создает правило.</span><span class="sxs-lookup"><span data-stu-id="f29eb-109">This command creates a rule.</span></span>

### <span data-ttu-id="f29eb-110">Пример 2. Создание двух правил</span><span class="sxs-lookup"><span data-stu-id="f29eb-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="f29eb-111">Первая команда создает правило для метрики "Запросы", а затем сохраняет его в переменной $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="f29eb-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="f29eb-112">Вторая команда создает второе правило для метрики "Запросы", а затем сохраняет его в переменной $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="f29eb-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="f29eb-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f29eb-113">Example 3</span></span>

<span data-ttu-id="f29eb-114">Создает правило автомасштабии.</span><span class="sxs-lookup"><span data-stu-id="f29eb-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="f29eb-115">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="f29eb-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="f29eb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f29eb-116">PARAMETERS</span></span>

### <span data-ttu-id="f29eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29eb-117">-DefaultProfile</span></span>
<span data-ttu-id="f29eb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f29eb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f29eb-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="f29eb-119">-MetricName</span></span>
<span data-ttu-id="f29eb-120">Указывает имя метрик.</span><span class="sxs-lookup"><span data-stu-id="f29eb-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="f29eb-121">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="f29eb-121">-MetricResourceId</span></span>
<span data-ttu-id="f29eb-122">Определяет метрическую единицу ресурса.</span><span class="sxs-lookup"><span data-stu-id="f29eb-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="f29eb-123">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="f29eb-123">-MetricStatistic</span></span>
<span data-ttu-id="f29eb-124">Указывает метрическую статистику.</span><span class="sxs-lookup"><span data-stu-id="f29eb-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="f29eb-125">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="f29eb-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f29eb-126">Среднее значение</span><span class="sxs-lookup"><span data-stu-id="f29eb-126">Average</span></span>
- <span data-ttu-id="f29eb-127">Min</span><span class="sxs-lookup"><span data-stu-id="f29eb-127">Min</span></span>
- <span data-ttu-id="f29eb-128">Максимум</span><span class="sxs-lookup"><span data-stu-id="f29eb-128">Max</span></span>
- <span data-ttu-id="f29eb-129">Сумма</span><span class="sxs-lookup"><span data-stu-id="f29eb-129">Sum</span></span>

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

### <span data-ttu-id="f29eb-130">-Operator</span><span class="sxs-lookup"><span data-stu-id="f29eb-130">-Operator</span></span>
<span data-ttu-id="f29eb-131">Оператор.</span><span class="sxs-lookup"><span data-stu-id="f29eb-131">Specifies the operator.</span></span>
<span data-ttu-id="f29eb-132">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="f29eb-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f29eb-133">Равно</span><span class="sxs-lookup"><span data-stu-id="f29eb-133">Equals</span></span>
- <span data-ttu-id="f29eb-134">NotEquals</span><span class="sxs-lookup"><span data-stu-id="f29eb-134">NotEquals</span></span>
- <span data-ttu-id="f29eb-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="f29eb-135">GreaterThan</span></span>
- <span data-ttu-id="f29eb-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f29eb-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="f29eb-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="f29eb-137">LessThan</span></span>
- <span data-ttu-id="f29eb-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="f29eb-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="f29eb-139">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="f29eb-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="f29eb-140">Указывает время завершения действия по шкале.</span><span class="sxs-lookup"><span data-stu-id="f29eb-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="f29eb-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="f29eb-141">-ScaleActionDirection</span></span>
<span data-ttu-id="f29eb-142">Определяет направление действия масштаба.</span><span class="sxs-lookup"><span data-stu-id="f29eb-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="f29eb-143">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f29eb-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f29eb-144">Нет</span><span class="sxs-lookup"><span data-stu-id="f29eb-144">None</span></span>
- <span data-ttu-id="f29eb-145">Увеличить</span><span class="sxs-lookup"><span data-stu-id="f29eb-145">Increase</span></span>
- <span data-ttu-id="f29eb-146">Уменьшить</span><span class="sxs-lookup"><span data-stu-id="f29eb-146">Decrease</span></span>

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

### <span data-ttu-id="f29eb-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="f29eb-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="f29eb-148">Определяет тип шкалы.</span><span class="sxs-lookup"><span data-stu-id="f29eb-148">Specifies the scale type.</span></span>
<span data-ttu-id="f29eb-149">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f29eb-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f29eb-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="f29eb-150">ChangeSize</span></span>
- <span data-ttu-id="f29eb-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="f29eb-151">ChangeCount</span></span>
- <span data-ttu-id="f29eb-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="f29eb-152">PercentChangeCount</span></span>
- <span data-ttu-id="f29eb-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="f29eb-153">ExactCount</span></span>

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

### <span data-ttu-id="f29eb-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="f29eb-154">-ScaleActionValue</span></span>
<span data-ttu-id="f29eb-155">Определяет значение действия.</span><span class="sxs-lookup"><span data-stu-id="f29eb-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="f29eb-156">-Пороговое значение</span><span class="sxs-lookup"><span data-stu-id="f29eb-156">-Threshold</span></span>
<span data-ttu-id="f29eb-157">Пороговое значение метрик.</span><span class="sxs-lookup"><span data-stu-id="f29eb-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="f29eb-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="f29eb-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="f29eb-159">Определяет оператор агрегирования времени.</span><span class="sxs-lookup"><span data-stu-id="f29eb-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="f29eb-160">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="f29eb-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f29eb-161">Среднее значение</span><span class="sxs-lookup"><span data-stu-id="f29eb-161">Average</span></span>
- <span data-ttu-id="f29eb-162">Минимум</span><span class="sxs-lookup"><span data-stu-id="f29eb-162">Minimum</span></span>
- <span data-ttu-id="f29eb-163">Максимальное значение</span><span class="sxs-lookup"><span data-stu-id="f29eb-163">Maximum</span></span>
- <span data-ttu-id="f29eb-164">Last</span><span class="sxs-lookup"><span data-stu-id="f29eb-164">Last</span></span>
- <span data-ttu-id="f29eb-165">Итого, количество</span><span class="sxs-lookup"><span data-stu-id="f29eb-165">Total, Count</span></span>

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

### <span data-ttu-id="f29eb-166">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="f29eb-166">-TimeGrain</span></span>
<span data-ttu-id="f29eb-167">Определяет время, указанное в этом проекте.</span><span class="sxs-lookup"><span data-stu-id="f29eb-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="f29eb-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="f29eb-168">-TimeWindow</span></span>
<span data-ttu-id="f29eb-169">Указывает время.</span><span class="sxs-lookup"><span data-stu-id="f29eb-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="f29eb-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29eb-170">CommonParameters</span></span>
<span data-ttu-id="f29eb-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f29eb-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29eb-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f29eb-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29eb-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f29eb-173">INPUTS</span></span>

### <span data-ttu-id="f29eb-174">System.String</span><span class="sxs-lookup"><span data-stu-id="f29eb-174">System.String</span></span>

### <span data-ttu-id="f29eb-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="f29eb-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="f29eb-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="f29eb-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="f29eb-177">System.Double</span><span class="sxs-lookup"><span data-stu-id="f29eb-177">System.Double</span></span>

### <span data-ttu-id="f29eb-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="f29eb-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="f29eb-179">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="f29eb-179">System.TimeSpan</span></span>

### <span data-ttu-id="f29eb-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="f29eb-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="f29eb-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span><span class="sxs-lookup"><span data-stu-id="f29eb-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="f29eb-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f29eb-182">OUTPUTS</span></span>

### <span data-ttu-id="f29eb-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span><span class="sxs-lookup"><span data-stu-id="f29eb-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="f29eb-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f29eb-184">NOTES</span></span>

## <span data-ttu-id="f29eb-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f29eb-185">RELATED LINKS</span></span>

[<span data-ttu-id="f29eb-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f29eb-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="f29eb-187">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="f29eb-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="f29eb-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f29eb-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="f29eb-189">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="f29eb-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="f29eb-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f29eb-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


