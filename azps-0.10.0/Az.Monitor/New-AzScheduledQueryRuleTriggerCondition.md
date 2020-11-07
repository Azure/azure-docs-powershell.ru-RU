---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruletriggercondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleTriggerCondition.md
ms.openlocfilehash: 53331c82a2ea1ac16b67c32f67545fec7d08e3dd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910196"
---
# <span data-ttu-id="f0ad3-101">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f0ad3-101">New-AzScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="f0ad3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ad3-103">Создает объект условия триггера типа</span><span class="sxs-lookup"><span data-stu-id="f0ad3-103">Creates an object of type Trigger Condition</span></span>

## <span data-ttu-id="f0ad3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0ad3-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator <String> -Threshold <Double>
 [-MetricTrigger <PSScheduledQueryRuleLogMetricTrigger>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0ad3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0ad3-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ad3-106">Создает объект условия триггера типа.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-106">Creates an object of type Trigger Condition.</span></span>
<span data-ttu-id="f0ad3-107">Этот объект передается команде, которая создает объект действия оповещения</span><span class="sxs-lookup"><span data-stu-id="f0ad3-107">This object is to be passed to the command that creates Alerting Action object</span></span>

## <span data-ttu-id="f0ad3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0ad3-108">EXAMPLES</span></span>

### <span data-ttu-id="f0ad3-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0ad3-109">Example 1</span></span>
```powershell
PS C:\>  $triggerCondition = New-AzScheduledQueryRuleTriggerCondition -ThresholdOperator "GreaterThan" -Threshold 3 -MetricTrigger $metricTrigger
```

## <span data-ttu-id="f0ad3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0ad3-110">PARAMETERS</span></span>

### <span data-ttu-id="f0ad3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ad3-111">-DefaultProfile</span></span>
<span data-ttu-id="f0ad3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ad3-113">-MetricTrigger</span><span class="sxs-lookup"><span data-stu-id="f0ad3-113">-MetricTrigger</span></span>
<span data-ttu-id="f0ad3-114">Условие запуска для правила запроса метрики</span><span class="sxs-lookup"><span data-stu-id="f0ad3-114">Trigger condition for metric query rule</span></span>

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

### <span data-ttu-id="f0ad3-115">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="f0ad3-115">-Threshold</span></span>
<span data-ttu-id="f0ad3-116">Пороговое значение, над которым генерируется оповещение</span><span class="sxs-lookup"><span data-stu-id="f0ad3-116">The threshold above which alert gets fired</span></span>

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

### <span data-ttu-id="f0ad3-117">-ThresholdOperator</span><span class="sxs-lookup"><span data-stu-id="f0ad3-117">-ThresholdOperator</span></span>
<span data-ttu-id="f0ad3-118">Пороговый оператор: GreaterThan, LessThan или Equals</span><span class="sxs-lookup"><span data-stu-id="f0ad3-118">The threshold operator : GreaterThan, LessThan or Equal</span></span>

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

### <span data-ttu-id="f0ad3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ad3-119">CommonParameters</span></span>
<span data-ttu-id="f0ad3-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0ad3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ad3-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0ad3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ad3-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0ad3-122">INPUTS</span></span>

### <span data-ttu-id="f0ad3-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="f0ad3-123">None</span></span>

## <span data-ttu-id="f0ad3-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0ad3-124">OUTPUTS</span></span>

### <span data-ttu-id="f0ad3-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="f0ad3-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition</span></span>

## <span data-ttu-id="f0ad3-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0ad3-126">NOTES</span></span>

## <span data-ttu-id="f0ad3-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0ad3-127">RELATED LINKS</span></span>
