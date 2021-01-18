---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 0fffbc11291fcf3cd7d3989e211bcbb0d202ea9b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506203"
---
# <span data-ttu-id="893d4-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="893d4-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="893d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="893d4-102">SYNOPSIS</span></span>
<span data-ttu-id="893d4-103">Создание объекта условия триггера типа</span><span class="sxs-lookup"><span data-stu-id="893d4-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="893d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="893d4-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="893d4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="893d4-105">DESCRIPTION</span></span>
<span data-ttu-id="893d4-106">Создает объект условия триггера типа.</span><span class="sxs-lookup"><span data-stu-id="893d4-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="893d4-107">Этот объект передается команде, которая создает объект action alerting</span><span class="sxs-lookup"><span data-stu-id="893d4-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="893d4-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="893d4-108">EXAMPLES</span></span>

### <span data-ttu-id="893d4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="893d4-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="893d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="893d4-110">PARAMETERS</span></span>

### <span data-ttu-id="893d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893d4-111">-DefaultProfile</span></span>
<span data-ttu-id="893d4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="893d4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="893d4-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="893d4-113">-MetricTrigger</span></span>
<span data-ttu-id="893d4-114">Условие триггера для правила запроса метрики</span><span class="sxs-lookup"><span data-stu-id="893d4-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="893d4-115">-Пороговое значение</span><span class="sxs-lookup"><span data-stu-id="893d4-115">-Threshold</span></span>
<span data-ttu-id="893d4-116">Пороговое значение, пре превышенное для оповещения</span><span class="sxs-lookup"><span data-stu-id="893d4-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="893d4-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="893d4-117">-ThresholdOperator</span></span>
<span data-ttu-id="893d4-118">Оператор порогового значения: большее, меньшее или равное</span><span class="sxs-lookup"><span data-stu-id="893d4-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="893d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893d4-119">CommonParameters</span></span>
<span data-ttu-id="893d4-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="893d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893d4-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="893d4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893d4-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="893d4-122">INPUTS</span></span>

### <span data-ttu-id="893d4-123">Нет</span><span class="sxs-lookup"><span data-stu-id="893d4-123">None</span></span>

## <span data-ttu-id="893d4-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="893d4-124">OUTPUTS</span></span>

### <span data-ttu-id="893d4-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="893d4-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="893d4-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="893d4-126">NOTES</span></span>

## <span data-ttu-id="893d4-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="893d4-127">RELATED LINKS</span></span>
