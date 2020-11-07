---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899494"
---
# <span data-ttu-id="30c61-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="30c61-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="30c61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30c61-102">SYNOPSIS</span></span>
<span data-ttu-id="30c61-103">Создает локальный объект условия, который можно использовать для создания нового оповещения о метрике.</span><span class="sxs-lookup"><span data-stu-id="30c61-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="30c61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30c61-104">SYNTAX</span></span>

### <span data-ttu-id="30c61-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30c61-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30c61-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30c61-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30c61-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30c61-107">DESCRIPTION</span></span>
<span data-ttu-id="30c61-108">Командлет **New-AzMetricAlertRuleV2Criteria** создает объект локального критерия метрики, который будет использоваться в качестве входного командлета Add-AzMetricAlertRuleV2, который создает новое правило оповещения метрики.</span><span class="sxs-lookup"><span data-stu-id="30c61-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="30c61-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30c61-109">EXAMPLES</span></span>

### <span data-ttu-id="30c61-110">Пример 1: создание критерия оповещения о простое метрика</span><span class="sxs-lookup"><span data-stu-id="30c61-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="30c61-111">Эта команда создает условие оповещения о простое метрика, которое можно использовать в правиле оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="30c61-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="30c61-112">Пример 2: создание более сложных условий оповещения для метрики</span><span class="sxs-lookup"><span data-stu-id="30c61-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="30c61-113">Этот набор команд создает более сложные критерии оповещения метрики, включая выбор измерений.</span><span class="sxs-lookup"><span data-stu-id="30c61-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="30c61-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30c61-114">PARAMETERS</span></span>

### <span data-ttu-id="30c61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c61-115">-DefaultProfile</span></span>
<span data-ttu-id="30c61-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30c61-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="30c61-117">-DimensionSelection</span></span>
<span data-ttu-id="30c61-118">Список условий измерения</span><span class="sxs-lookup"><span data-stu-id="30c61-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="30c61-119">-DynamicThreshold</span></span>
<span data-ttu-id="30c61-120">Динамическое пороговое значение для условия правила</span><span class="sxs-lookup"><span data-stu-id="30c61-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-121">-FailingPeriod</span><span class="sxs-lookup"><span data-stu-id="30c61-121">-FailingPeriod</span></span>
<span data-ttu-id="30c61-122">Период сбоя для условия правила</span><span class="sxs-lookup"><span data-stu-id="30c61-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-123">-IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="30c61-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="30c61-124">Параметр IgnoreDataBefore</span><span class="sxs-lookup"><span data-stu-id="30c61-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="30c61-125">-MetricName</span></span>
<span data-ttu-id="30c61-126">Имя метрики для правила</span><span class="sxs-lookup"><span data-stu-id="30c61-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="30c61-127">-MetricNamespace</span></span>
<span data-ttu-id="30c61-128">Пространство имен метрики</span><span class="sxs-lookup"><span data-stu-id="30c61-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-129">-Operator</span><span class="sxs-lookup"><span data-stu-id="30c61-129">-Operator</span></span>
<span data-ttu-id="30c61-130">Оператор условия для правила</span><span class="sxs-lookup"><span data-stu-id="30c61-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-131">-Чувствительность</span><span class="sxs-lookup"><span data-stu-id="30c61-131">-Sensitivity</span></span>
<span data-ttu-id="30c61-132">Условие чувствительности для правила</span><span class="sxs-lookup"><span data-stu-id="30c61-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-133">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="30c61-133">-Threshold</span></span>
<span data-ttu-id="30c61-134">Пороговое значение для условия правила</span><span class="sxs-lookup"><span data-stu-id="30c61-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-135">-TimeAggregation</span><span class="sxs-lookup"><span data-stu-id="30c61-135">-TimeAggregation</span></span>
<span data-ttu-id="30c61-136">Статистическая операция, используемая для развертывания нескольких значений метрики в интервале между окнами</span><span class="sxs-lookup"><span data-stu-id="30c61-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-137">-TotalPeriod</span><span class="sxs-lookup"><span data-stu-id="30c61-137">-TotalPeriod</span></span>
<span data-ttu-id="30c61-138">Общий период для условия правила</span><span class="sxs-lookup"><span data-stu-id="30c61-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c61-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c61-139">CommonParameters</span></span>
<span data-ttu-id="30c61-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30c61-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="30c61-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c61-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c61-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30c61-142">INPUTS</span></span>

### <span data-ttu-id="30c61-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="30c61-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="30c61-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30c61-144">OUTPUTS</span></span>

### <span data-ttu-id="30c61-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="30c61-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="30c61-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="30c61-146">NOTES</span></span>

## <span data-ttu-id="30c61-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30c61-147">RELATED LINKS</span></span>
