---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 0158f274ea485262b05fa1a336a2ce071fc64930
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224204"
---
# <span data-ttu-id="19627-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="19627-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="19627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19627-102">SYNOPSIS</span></span>
<span data-ttu-id="19627-103">Создание объекта локальных критериев, который можно использовать для создания нового метрическую оповещения.</span><span class="sxs-lookup"><span data-stu-id="19627-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="19627-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19627-104">SYNTAX</span></span>

### <span data-ttu-id="19627-105">StaticThresholdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19627-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19627-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19627-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19627-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="19627-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19627-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19627-108">DESCRIPTION</span></span>
<span data-ttu-id="19627-109">С помощью **cmdlet New-AzMetricAlertRuleV2Criteria** создается объект локальных метрических критериев, который будет использоваться в качестве входного для параметра [Add-AzMetricAlertRuleV2,](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) который создает новое правило метрических оповещений.</span><span class="sxs-lookup"><span data-stu-id="19627-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2) cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="19627-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19627-110">EXAMPLES</span></span>

### <span data-ttu-id="19627-111">Пример 1. Создание простого критерия метрических оповещений</span><span class="sxs-lookup"><span data-stu-id="19627-111">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="19627-112">Эта команда создает простые критерии метрических оповещений, которые можно использовать в правиле метрических оповещений.</span><span class="sxs-lookup"><span data-stu-id="19627-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="19627-113">Пример 2. Создание динамических метрических критериев оповещения</span><span class="sxs-lookup"><span data-stu-id="19627-113">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="19627-114">Эта команда создает динамические критерии оповещения, которые можно использовать в правиле метрических оповещений.</span><span class="sxs-lookup"><span data-stu-id="19627-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="19627-115">Пример 3. Создание более сложных критериев метрических оповещений</span><span class="sxs-lookup"><span data-stu-id="19627-115">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="19627-116">Этот набор команд создает более сложные критерии метрических оповещений, которые включают выбор измерений.</span><span class="sxs-lookup"><span data-stu-id="19627-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="19627-117">Пример 4. Создание критериев доступности веб-тестов</span><span class="sxs-lookup"><span data-stu-id="19627-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="19627-118">Эта команда создает условия доступности веб-тест, которые можно использовать в правиле метрических оповещений.</span><span class="sxs-lookup"><span data-stu-id="19627-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="19627-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19627-119">PARAMETERS</span></span>

### <span data-ttu-id="19627-120">-ApplicationInsightsId</span><span class="sxs-lookup"><span data-stu-id="19627-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="19627-121">ИД ресурса Application Insights.</span><span class="sxs-lookup"><span data-stu-id="19627-121">The Application Insights resource Id.</span></span>

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

### <span data-ttu-id="19627-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19627-122">-DefaultProfile</span></span>
<span data-ttu-id="19627-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19627-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19627-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="19627-124">-DimensionSelection</span></span>
<span data-ttu-id="19627-125">Список условий измерения</span><span class="sxs-lookup"><span data-stu-id="19627-125">List of dimension conditions</span></span>

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

### <span data-ttu-id="19627-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="19627-126">-DynamicThreshold</span></span>
<span data-ttu-id="19627-127">Параметр переключения для использования динамического порогового типа</span><span class="sxs-lookup"><span data-stu-id="19627-127">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="19627-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="19627-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="19627-129">Общее количество проверяемого балла</span><span class="sxs-lookup"><span data-stu-id="19627-129">The Total number of examined points</span></span>

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

### <span data-ttu-id="19627-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="19627-130">-FailedLocationCount</span></span>
<span data-ttu-id="19627-131">Минимальное количество сбойных мест для оповещения.</span><span class="sxs-lookup"><span data-stu-id="19627-131">The minimum number of failed locations to raise an alert.</span></span>

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

### <span data-ttu-id="19627-132">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="19627-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="19627-133">Параметр IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="19627-133">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="19627-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="19627-134">-MetricName</span></span>
<span data-ttu-id="19627-135">Имя метрики для правила</span><span class="sxs-lookup"><span data-stu-id="19627-135">The metric name for rule</span></span>

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

### <span data-ttu-id="19627-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="19627-136">-MetricNamespace</span></span>
<span data-ttu-id="19627-137">Пространство имен метрик</span><span class="sxs-lookup"><span data-stu-id="19627-137">The Namespace of the metric</span></span>

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

### <span data-ttu-id="19627-138">-Operator</span><span class="sxs-lookup"><span data-stu-id="19627-138">-Operator</span></span>
<span data-ttu-id="19627-139">Оператор условия правила</span><span class="sxs-lookup"><span data-stu-id="19627-139">The rule condition operator</span></span>

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

### <span data-ttu-id="19627-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="19627-140">-SkipMetricValidation</span></span>
<span data-ttu-id="19627-141">Позволяет создать правило оповещения для настраиваемой метрике, которая еще не излучается, из-за чего проверка метрики пропускается.</span><span class="sxs-lookup"><span data-stu-id="19627-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

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

### <span data-ttu-id="19627-142">-Пороговое значение</span><span class="sxs-lookup"><span data-stu-id="19627-142">-Threshold</span></span>
<span data-ttu-id="19627-143">Пороговое значение для условия правила</span><span class="sxs-lookup"><span data-stu-id="19627-143">The threshold for rule condition</span></span>

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

### <span data-ttu-id="19627-144">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="19627-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="19627-145">Конфиденциальность условий правил</span><span class="sxs-lookup"><span data-stu-id="19627-145">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="19627-146">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="19627-146">-TimeAggregation</span></span>
<span data-ttu-id="19627-147">Операция агрегирования, которая использовалась для сужения нескольких метрических значений по интервалу окна.</span><span class="sxs-lookup"><span data-stu-id="19627-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="19627-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="19627-148">-ViolationCount</span></span>
<span data-ttu-id="19627-149">Минимальное количество нарушений, требуемое в выбранном окне времени lookback, необходимое для оповещения</span><span class="sxs-lookup"><span data-stu-id="19627-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="19627-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="19627-150">-WebTest</span></span>
<span data-ttu-id="19627-151">Параметр переключения для использования типа условия доступности</span><span class="sxs-lookup"><span data-stu-id="19627-151">Switch parameter for using availability criteria Type</span></span>

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

### <span data-ttu-id="19627-152">-WebTestId</span><span class="sxs-lookup"><span data-stu-id="19627-152">-WebTestId</span></span>
<span data-ttu-id="19627-153">The Application Insights web test Id.</span><span class="sxs-lookup"><span data-stu-id="19627-153">The Application Insights web test Id.</span></span>

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

### <span data-ttu-id="19627-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19627-154">CommonParameters</span></span>
<span data-ttu-id="19627-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19627-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19627-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19627-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19627-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19627-157">INPUTS</span></span>

### <span data-ttu-id="19627-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span><span class="sxs-lookup"><span data-stu-id="19627-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="19627-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19627-159">OUTPUTS</span></span>

### <span data-ttu-id="19627-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="19627-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="19627-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19627-161">NOTES</span></span>

## <span data-ttu-id="19627-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19627-162">RELATED LINKS</span></span>
