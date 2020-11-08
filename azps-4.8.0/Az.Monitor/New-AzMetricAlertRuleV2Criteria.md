---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 101d522c1f8ae3b44545bdb204bad01fbe21df9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244425"
---
# <span data-ttu-id="27fdf-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="27fdf-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="27fdf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="27fdf-103">Создает локальный объект условия, который можно использовать для создания нового оповещения о метрике.</span><span class="sxs-lookup"><span data-stu-id="27fdf-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="27fdf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27fdf-104">SYNTAX</span></span>

### <span data-ttu-id="27fdf-105">StaticThresholdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27fdf-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27fdf-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27fdf-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27fdf-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="27fdf-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27fdf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27fdf-108">DESCRIPTION</span></span>
<span data-ttu-id="27fdf-109">Командлет **New-AzMetricAlertRuleV2Criteria** создает объект локального критерия метрики, который будет использоваться в качестве входного командлета Add-AzMetricAlertRuleV2, который создает новое правило оповещения метрики.</span><span class="sxs-lookup"><span data-stu-id="27fdf-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="27fdf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27fdf-110">EXAMPLES</span></span>

### <span data-ttu-id="27fdf-111">Пример 1: создание критерия оповещения о простое метрика</span><span class="sxs-lookup"><span data-stu-id="27fdf-111">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="27fdf-112">Эта команда создает условие оповещения о простое метрика, которое можно использовать в правиле оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="27fdf-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="27fdf-113">Пример 2: Создание динамического условия оповещения для метрики</span><span class="sxs-lookup"><span data-stu-id="27fdf-113">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="27fdf-114">Эта команда создает динамические критерии оповещения метрики, которые можно использовать в правиле оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="27fdf-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="27fdf-115">Пример 3: создание более сложных условий оповещения для метрики</span><span class="sxs-lookup"><span data-stu-id="27fdf-115">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="27fdf-116">Этот набор команд создает более сложные критерии оповещения метрики, включая выбор измерений.</span><span class="sxs-lookup"><span data-stu-id="27fdf-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="27fdf-117">Пример 4: Создание критериев доступности веб-теста</span><span class="sxs-lookup"><span data-stu-id="27fdf-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="27fdf-118">Эта команда создает критерии доступности веб-теста, которые можно использовать в правиле оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="27fdf-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="27fdf-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27fdf-119">PARAMETERS</span></span>

### <span data-ttu-id="27fdf-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="27fdf-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="27fdf-121">Идентификатор ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="27fdf-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27fdf-122">-DefaultProfile</span></span>
<span data-ttu-id="27fdf-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27fdf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27fdf-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="27fdf-124">-DimensionSelection</span></span>
<span data-ttu-id="27fdf-125">Список условий измерения</span><span class="sxs-lookup"><span data-stu-id="27fdf-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="27fdf-126">-DynamicThreshold</span></span>
<span data-ttu-id="27fdf-127">Параметр, для которого используется динамический тип порогового значения</span><span class="sxs-lookup"><span data-stu-id="27fdf-127">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="27fdf-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="27fdf-129">Общее количество проверенных очков</span><span class="sxs-lookup"><span data-stu-id="27fdf-129">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="27fdf-130">-FailedLocationCount</span></span>
<span data-ttu-id="27fdf-131">Минимальное количество ошибочных местоположений для генерации оповещения.</span><span class="sxs-lookup"><span data-stu-id="27fdf-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="27fdf-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="27fdf-133">Параметр IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="27fdf-133">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="27fdf-134">-MetricName</span></span>
<span data-ttu-id="27fdf-135">Имя метрики для правила</span><span class="sxs-lookup"><span data-stu-id="27fdf-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="27fdf-136">-MetricNamespace</span></span>
<span data-ttu-id="27fdf-137">Пространство имен метрики</span><span class="sxs-lookup"><span data-stu-id="27fdf-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-138">-Operator</span><span class="sxs-lookup"><span data-stu-id="27fdf-138">-Operator</span></span>
<span data-ttu-id="27fdf-139">Оператор условия для правила</span><span class="sxs-lookup"><span data-stu-id="27fdf-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="27fdf-140">-SkipMetricValidation</span></span>
<span data-ttu-id="27fdf-141">Позволяет создавать правила оповещения для настраиваемой метрики, которая еще не выпущена, вызвав тем самым, что проверка метрики будет пропущена.</span><span class="sxs-lookup"><span data-stu-id="27fdf-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-142">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="27fdf-142">-Threshold</span></span>
<span data-ttu-id="27fdf-143">Пороговое значение для условия правила</span><span class="sxs-lookup"><span data-stu-id="27fdf-143">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="27fdf-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="27fdf-145">Условие чувствительности для правила</span><span class="sxs-lookup"><span data-stu-id="27fdf-145">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="27fdf-146">-TimeAggregation</span></span>
<span data-ttu-id="27fdf-147">Статистическая операция, используемая для развертывания нескольких значений метрики в интервале между окнами</span><span class="sxs-lookup"><span data-stu-id="27fdf-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="27fdf-148">-ViolationCount</span></span>
<span data-ttu-id="27fdf-149">Минимальное количество нарушений, необходимых в выбранном окне lookback Time (время), которое требуется для генерации оповещения</span><span class="sxs-lookup"><span data-stu-id="27fdf-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="27fdf-150">-WebTest</span></span>
<span data-ttu-id="27fdf-151">Параметр "переключить" для использования типа условий доступности</span><span class="sxs-lookup"><span data-stu-id="27fdf-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="27fdf-152">-WebTestId</span></span>
<span data-ttu-id="27fdf-153">Идентификатор веб-теста Application Insights.</span><span class="sxs-lookup"><span data-stu-id="27fdf-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fdf-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27fdf-154">CommonParameters</span></span>
<span data-ttu-id="27fdf-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27fdf-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27fdf-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27fdf-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27fdf-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27fdf-157">INPUTS</span></span>

### <span data-ttu-id="27fdf-158">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="27fdf-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="27fdf-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27fdf-159">OUTPUTS</span></span>

### <span data-ttu-id="27fdf-160">Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="27fdf-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="27fdf-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="27fdf-161">NOTES</span></span>

## <span data-ttu-id="27fdf-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27fdf-162">RELATED LINKS</span></span>
