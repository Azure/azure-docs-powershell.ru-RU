---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c5fb336d7ba105469506bb0a80a5b69036e5474b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910208"
---
# <span data-ttu-id="5dbb2-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5dbb2-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="5dbb2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5dbb2-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbb2-103">Создает объект триггера метрики журнала типа "".</span><span class="sxs-lookup"><span data-stu-id="5dbb2-103">Creates an object of type Log Metric Trigger</span></span>

## <span data-ttu-id="5dbb2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5dbb2-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5dbb2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dbb2-105">DESCRIPTION</span></span>
<span data-ttu-id="5dbb2-106">Создает объект триггера метрики журнала и является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5dbb2-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="5dbb2-107">Это условие триггера для правила запроса метрики, которое должно использоваться, если требуется указать тип измерения метрики для оповещения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5dbb2-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="5dbb2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5dbb2-108">EXAMPLES</span></span>

### <span data-ttu-id="5dbb2-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5dbb2-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="5dbb2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5dbb2-110">PARAMETERS</span></span>

### <span data-ttu-id="5dbb2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dbb2-111">-DefaultProfile</span></span>
<span data-ttu-id="5dbb2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dbb2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dbb2-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="5dbb2-113">-MetricColumn</span></span>
<span data-ttu-id="5dbb2-114">Столбец, для которого выполняется статистическое значение метрики</span><span class="sxs-lookup"><span data-stu-id="5dbb2-114">Column on which metric value is being aggregated</span></span>

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

### <span data-ttu-id="5dbb2-115">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="5dbb2-115">-MetricTriggerType</span></span>
<span data-ttu-id="5dbb2-116">Тип триггера метрики</span><span class="sxs-lookup"><span data-stu-id="5dbb2-116">The metric trigger type</span></span>

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

### <span data-ttu-id="5dbb2-117">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="5dbb2-117">-Threshold</span></span>
<span data-ttu-id="5dbb2-118">Пороговое значение метрики</span><span class="sxs-lookup"><span data-stu-id="5dbb2-118">The metric threshold value</span></span>

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

### <span data-ttu-id="5dbb2-119">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="5dbb2-119">-ThresholdOperator</span></span>
<span data-ttu-id="5dbb2-120">Оператор порогового значения метрики: GreaterThan, LessThan, Equals</span><span class="sxs-lookup"><span data-stu-id="5dbb2-120">The metric threshold operator : GreaterThan, LessThan, Equal</span></span>

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

### <span data-ttu-id="5dbb2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbb2-121">CommonParameters</span></span>
<span data-ttu-id="5dbb2-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5dbb2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbb2-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dbb2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbb2-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5dbb2-124">INPUTS</span></span>

### <span data-ttu-id="5dbb2-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="5dbb2-125">None</span></span>

## <span data-ttu-id="5dbb2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dbb2-126">OUTPUTS</span></span>

### <span data-ttu-id="5dbb2-127">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5dbb2-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="5dbb2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5dbb2-128">NOTES</span></span>

## <span data-ttu-id="5dbb2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dbb2-129">RELATED LINKS</span></span>
