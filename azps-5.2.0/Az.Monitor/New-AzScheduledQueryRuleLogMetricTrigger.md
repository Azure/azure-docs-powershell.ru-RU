---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulelogmetrictrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleLogMetricTrigger.md
ms.openlocfilehash: c4d44f266a9966f605e009cc4ce5dece0fa5e2ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392143"
---
# <span data-ttu-id="5b4fb-101">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5b4fb-101">New-AzScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="5b4fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4fb-103">Создает объект с триггером метрики журнала.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-103">Creates an object of type Log Metric Trigger.</span></span>

## <span data-ttu-id="5b4fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b4fb-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator <String> -Threshold <Double>
 -MetricTriggerType <String> -MetricColumn <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b4fb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b4fb-105">DESCRIPTION</span></span>
<span data-ttu-id="5b4fb-106">Создает объект с триггером метрики журнала (необязательный).</span><span class="sxs-lookup"><span data-stu-id="5b4fb-106">Creates an object of type Log Metric Trigger and is optional.</span></span>
<span data-ttu-id="5b4fb-107">Это условие триггера для правила запроса метрики, которое будет использоваться, когда нужно указать тип метрических единиц оповещения.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-107">This is the trigger condition for metric query rule, to be used when you need to state metric measurement type of alert.</span></span>

## <span data-ttu-id="5b4fb-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b4fb-108">EXAMPLES</span></span>

### <span data-ttu-id="5b4fb-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b4fb-109">Example 1</span></span>
```powershell
PS C:\> $metricTrigger = New-AzScheduledQueryRuleLogMetricTrigger -ThresholdOperator "GreaterThan" -Threshold 5 -MetricTriggerType "Consecutive" -MetricColumn "Computer"
```

## <span data-ttu-id="5b4fb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b4fb-110">PARAMETERS</span></span>

### <span data-ttu-id="5b4fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4fb-111">-DefaultProfile</span></span>
<span data-ttu-id="5b4fb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b4fb-113">-MetricColumn</span><span class="sxs-lookup"><span data-stu-id="5b4fb-113">-MetricColumn</span></span>
<span data-ttu-id="5b4fb-114">Столбец, по которому агрегируется метрическая величина.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-114">Column on which metric value is being aggregated.</span></span>
<span data-ttu-id="5b4fb-115">Входные данные не проверены.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-115">The input is not validated.</span></span> <span data-ttu-id="5b4fb-116">Сначала она будет проверена, New-AzScheduledQueryRule будет вызвана.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-116">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="5b4fb-117">-MetricTriggerType</span><span class="sxs-lookup"><span data-stu-id="5b4fb-117">-MetricTriggerType</span></span>
<span data-ttu-id="5b4fb-118">Тип триггера метрики.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-118">The metric trigger type.</span></span>
<span data-ttu-id="5b4fb-119">Входные данные не проверены.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-119">The input is not validated.</span></span> <span data-ttu-id="5b4fb-120">Сначала она будет проверена, New-AzScheduledQueryRule будет вызвана.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-120">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="5b4fb-121">-Пороговое значение</span><span class="sxs-lookup"><span data-stu-id="5b4fb-121">-Threshold</span></span>
<span data-ttu-id="5b4fb-122">Пороговое значение метрики: "Последовательный", "Всего".</span><span class="sxs-lookup"><span data-stu-id="5b4fb-122">The metric threshold value: Consecutive, Total.</span></span>
<span data-ttu-id="5b4fb-123">Входные данные не проверены.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-123">The input is not validated.</span></span> <span data-ttu-id="5b4fb-124">Сначала она будет проверена, New-AzScheduledQueryRule будет вызвана.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-124">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="5b4fb-125">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="5b4fb-125">-ThresholdOperator</span></span>
<span data-ttu-id="5b4fb-126">Оператор порогового значения метрики: "БольшеThan", "МеньшеThan", "Равно".</span><span class="sxs-lookup"><span data-stu-id="5b4fb-126">The metric threshold operator : GreaterThan, LessThan, Equal.</span></span>
<span data-ttu-id="5b4fb-127">Входные данные не проверены.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-127">The input is not validated.</span></span> <span data-ttu-id="5b4fb-128">Сначала она будет проверена, New-AzScheduledQueryRule будет вызвана.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-128">It will first be validated when New-AzScheduledQueryRule is eventually called.</span></span>

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

### <span data-ttu-id="5b4fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4fb-129">CommonParameters</span></span>
<span data-ttu-id="5b4fb-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4fb-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b4fb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4fb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b4fb-132">INPUTS</span></span>

### <span data-ttu-id="5b4fb-133">Нет</span><span class="sxs-lookup"><span data-stu-id="5b4fb-133">None</span></span>

## <span data-ttu-id="5b4fb-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b4fb-134">OUTPUTS</span></span>

### <span data-ttu-id="5b4fb-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="5b4fb-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger</span></span>

## <span data-ttu-id="5b4fb-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b4fb-136">NOTES</span></span>

## <span data-ttu-id="5b4fb-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b4fb-137">RELATED LINKS</span></span>
