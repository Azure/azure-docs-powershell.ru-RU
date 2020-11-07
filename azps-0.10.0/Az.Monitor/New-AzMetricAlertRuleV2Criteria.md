---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: bb72a50c2db43a8db053d273c601ca51e96402f0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910214"
---
# <span data-ttu-id="b4367-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="b4367-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="b4367-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4367-102">SYNOPSIS</span></span>
<span data-ttu-id="b4367-103">Создает локальный объект условия, который можно использовать для создания нового оповещения о метрике.</span><span class="sxs-lookup"><span data-stu-id="b4367-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="b4367-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4367-104">SYNTAX</span></span>

### <span data-ttu-id="b4367-105">StaticThresholdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4367-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4367-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4367-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4367-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4367-107">DESCRIPTION</span></span>
<span data-ttu-id="b4367-108">Командлет **New-AzMetricAlertRuleV2Criteria** создает объект локального критерия метрики, который будет использоваться в качестве входного командлета Add-AzMetricAlertRuleV2, который создает новое правило оповещения метрики.</span><span class="sxs-lookup"><span data-stu-id="b4367-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="b4367-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4367-109">EXAMPLES</span></span>

### <span data-ttu-id="b4367-110">Пример 1: создание критерия оповещения о простое метрика</span><span class="sxs-lookup"><span data-stu-id="b4367-110">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="b4367-111">Эта команда создает условие оповещения о простое метрика, которое можно использовать в правиле оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="b4367-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="b4367-112">Пример 2: Создание динамического условия оповещения для метрики</span><span class="sxs-lookup"><span data-stu-id="b4367-112">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="b4367-113">Эта команда создает динамические критерии оповещения метрики, которые можно использовать в правиле оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="b4367-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="b4367-114">Пример 3: создание более сложных условий оповещения для метрики</span><span class="sxs-lookup"><span data-stu-id="b4367-114">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="b4367-115">Этот набор команд создает более сложные критерии оповещения метрики, включая выбор измерений.</span><span class="sxs-lookup"><span data-stu-id="b4367-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="b4367-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4367-116">PARAMETERS</span></span>

### <span data-ttu-id="b4367-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4367-117">-DefaultProfile</span></span>
<span data-ttu-id="b4367-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4367-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4367-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="b4367-119">-DimensionSelection</span></span>
<span data-ttu-id="b4367-120">Список условий измерения</span><span class="sxs-lookup"><span data-stu-id="b4367-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4367-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="b4367-121">-DynamicThreshold</span></span>
<span data-ttu-id="b4367-122">Параметр, для которого используется динамический тип порогового значения</span><span class="sxs-lookup"><span data-stu-id="b4367-122">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="b4367-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="b4367-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="b4367-124">Общее количество проверенных очков</span><span class="sxs-lookup"><span data-stu-id="b4367-124">The Total number of examined points</span></span>

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

### <span data-ttu-id="b4367-125">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="b4367-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="b4367-126">Параметр IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="b4367-126">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="b4367-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="b4367-127">-MetricName</span></span>
<span data-ttu-id="b4367-128">Имя метрики для правила</span><span class="sxs-lookup"><span data-stu-id="b4367-128">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4367-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="b4367-129">-MetricNamespace</span></span>
<span data-ttu-id="b4367-130">Пространство имен метрики</span><span class="sxs-lookup"><span data-stu-id="b4367-130">The Namespace of the metric</span></span>

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

### <span data-ttu-id="b4367-131">-Operator</span><span class="sxs-lookup"><span data-stu-id="b4367-131">-Operator</span></span>
<span data-ttu-id="b4367-132">Оператор условия для правила</span><span class="sxs-lookup"><span data-stu-id="b4367-132">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4367-133">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="b4367-133">-Threshold</span></span>
<span data-ttu-id="b4367-134">Пороговое значение для условия правила</span><span class="sxs-lookup"><span data-stu-id="b4367-134">The threshold for rule condition</span></span>

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

### <span data-ttu-id="b4367-135">-ThresholdSensitivity</span><span class="sxs-lookup"><span data-stu-id="b4367-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="b4367-136">Условие чувствительности для правила</span><span class="sxs-lookup"><span data-stu-id="b4367-136">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="b4367-137">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="b4367-137">-TimeAggregation</span></span>
<span data-ttu-id="b4367-138">Статистическая операция, используемая для развертывания нескольких значений метрики в интервале между окнами</span><span class="sxs-lookup"><span data-stu-id="b4367-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4367-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="b4367-139">-ViolationCount</span></span>
<span data-ttu-id="b4367-140">Минимальное количество нарушений, необходимых в выбранном окне lookback Time (время), которое требуется для генерации оповещения</span><span class="sxs-lookup"><span data-stu-id="b4367-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="b4367-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4367-141">CommonParameters</span></span>
<span data-ttu-id="b4367-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4367-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4367-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4367-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4367-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4367-144">INPUTS</span></span>

### <span data-ttu-id="b4367-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="b4367-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="b4367-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4367-146">OUTPUTS</span></span>

### <span data-ttu-id="b4367-147">Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="b4367-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="b4367-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4367-148">NOTES</span></span>

## <span data-ttu-id="b4367-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4367-149">RELATED LINKS</span></span>
