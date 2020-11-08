---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247290"
---
# <span data-ttu-id="a21d1-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a21d1-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="a21d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a21d1-102">SYNOPSIS</span></span>
<span data-ttu-id="a21d1-103">Создает объект триггера метрики журнала типа log.</span><span class="sxs-lookup"><span data-stu-id="a21d1-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="a21d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a21d1-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a21d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a21d1-105">DESCRIPTION</span></span>
<span data-ttu-id="a21d1-106">Создает объект триггера метрики журнала и является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a21d1-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="a21d1-107">Это условие триггера для правила запроса метрики, которое должно использоваться, если требуется указать тип измерения метрики для оповещения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="a21d1-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="a21d1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a21d1-108">EXAMPLES</span></span>

### <span data-ttu-id="a21d1-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a21d1-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="a21d1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a21d1-110">PARAMETERS</span></span>

### <span data-ttu-id="a21d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a21d1-111">-DefaultProfile</span></span>
<span data-ttu-id="a21d1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a21d1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a21d1-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="a21d1-113">-MetricColumn</span></span>
<span data-ttu-id="a21d1-114">Столбец, для которого выполняется статистическое значение метрики.</span><span class="sxs-lookup"><span data-stu-id="a21d1-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="a21d1-115">Входные данные не проверяются.</span><span class="sxs-lookup"><span data-stu-id="a21d1-115">The input is not validated.</span></span> <span data-ttu-id="a21d1-116">Сначала оно будет проверяться, когда New-AzScheduledQueryRule в конечном итоге вызывается.</span><span class="sxs-lookup"><span data-stu-id="a21d1-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="a21d1-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="a21d1-117">-MetricTriggerType</span></span>
<span data-ttu-id="a21d1-118">Тип триггера метрики.</span><span class="sxs-lookup"><span data-stu-id="a21d1-118">The metric trigger type.</span></span>
<span data-ttu-id="a21d1-119">Входные данные не проверяются.</span><span class="sxs-lookup"><span data-stu-id="a21d1-119">The input is not validated.</span></span> <span data-ttu-id="a21d1-120">Сначала оно будет проверяться, когда New-AzScheduledQueryRule в конечном итоге вызывается.</span><span class="sxs-lookup"><span data-stu-id="a21d1-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="a21d1-121">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="a21d1-121">-Threshold</span></span>
<span data-ttu-id="a21d1-122">Пороговое значение метрики: последовательные, всего.</span><span class="sxs-lookup"><span data-stu-id="a21d1-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="a21d1-123">Входные данные не проверяются.</span><span class="sxs-lookup"><span data-stu-id="a21d1-123">The input is not validated.</span></span> <span data-ttu-id="a21d1-124">Сначала оно будет проверяться, когда New-AzScheduledQueryRule в конечном итоге вызывается.</span><span class="sxs-lookup"><span data-stu-id="a21d1-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a21d1-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="a21d1-125">-ThresholdOperator</span></span>
<span data-ttu-id="a21d1-126">Оператор порогового значения метрики: GreaterThan, LessThan, Equals.</span><span class="sxs-lookup"><span data-stu-id="a21d1-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="a21d1-127">Входные данные не проверяются.</span><span class="sxs-lookup"><span data-stu-id="a21d1-127">The input is not validated.</span></span> <span data-ttu-id="a21d1-128">Сначала оно будет проверяться, когда New-AzScheduledQueryRule в конечном итоге вызывается.</span><span class="sxs-lookup"><span data-stu-id="a21d1-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="a21d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21d1-129">CommonParameters</span></span>
<span data-ttu-id="a21d1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a21d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21d1-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a21d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21d1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a21d1-132">INPUTS</span></span>

### <span data-ttu-id="a21d1-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="a21d1-133">None</span></span>

## <span data-ttu-id="a21d1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a21d1-134">OUTPUTS</span></span>

### <span data-ttu-id="a21d1-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a21d1-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="a21d1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a21d1-136">NOTES</span></span>

## <span data-ttu-id="a21d1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a21d1-137">RELATED LINKS</span></span>
