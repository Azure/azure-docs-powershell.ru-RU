---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249921"
---
# <span data-ttu-id="2334c-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2334c-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="2334c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2334c-102">SYNOPSIS</span></span>
<span data-ttu-id="2334c-103">Создает объект условия триггера типа</span><span class="sxs-lookup"><span data-stu-id="2334c-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="2334c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2334c-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2334c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2334c-105">DESCRIPTION</span></span>
<span data-ttu-id="2334c-106">Создает объект условия триггера типа.</span><span class="sxs-lookup"><span data-stu-id="2334c-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="2334c-107">Этот объект передается команде, которая создает объект действия оповещения</span><span class="sxs-lookup"><span data-stu-id="2334c-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="2334c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2334c-108">EXAMPLES</span></span>

### <span data-ttu-id="2334c-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2334c-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="2334c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2334c-110">PARAMETERS</span></span>

### <span data-ttu-id="2334c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2334c-111">-DefaultProfile</span></span>
<span data-ttu-id="2334c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2334c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2334c-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2334c-113">-MetricTrigger</span></span>
<span data-ttu-id="2334c-114">Условие запуска для правила запроса метрики</span><span class="sxs-lookup"><span data-stu-id="2334c-114">Trigger condition for metric query rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleLogMetricTrigger
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2334c-115">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="2334c-115">-Threshold</span></span>
<span data-ttu-id="2334c-116">Пороговое значение, над которым генерируется оповещение</span><span class="sxs-lookup"><span data-stu-id="2334c-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="2334c-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="2334c-117">-ThresholdOperator</span></span>
<span data-ttu-id="2334c-118">Пороговый оператор: GreaterThan, LessThan или Equals</span><span class="sxs-lookup"><span data-stu-id="2334c-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="2334c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2334c-119">CommonParameters</span></span>
<span data-ttu-id="2334c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2334c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2334c-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2334c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2334c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2334c-122">INPUTS</span></span>

### <span data-ttu-id="2334c-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="2334c-123">None</span></span>

## <span data-ttu-id="2334c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2334c-124">OUTPUTS</span></span>

### <span data-ttu-id="2334c-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2334c-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="2334c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="2334c-126">NOTES</span></span>

## <span data-ttu-id="2334c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2334c-127">RELATED LINKS</span></span>