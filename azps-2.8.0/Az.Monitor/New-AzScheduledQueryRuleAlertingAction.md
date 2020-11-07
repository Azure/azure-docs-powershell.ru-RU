---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 382aa35b9967e016ce87da982b32c97148c9f3c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903269"
---
# <span data-ttu-id="9949b-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="9949b-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="9949b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9949b-102">SYNOPSIS</span></span>
<span data-ttu-id="9949b-103">Создает объект действия оповещения типа</span><span class="sxs-lookup"><span data-stu-id="9949b-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="9949b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9949b-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9949b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9949b-105">DESCRIPTION</span></span>
<span data-ttu-id="9949b-106">Создает объект типа "действие оповещения". Этот объект будет передан команде, которая создает правило оповещения в журнале.</span><span class="sxs-lookup"><span data-stu-id="9949b-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="9949b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9949b-107">EXAMPLES</span></span>

### <span data-ttu-id="9949b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9949b-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="9949b-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9949b-109">PARAMETERS</span></span>

### <span data-ttu-id="9949b-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="9949b-110">-AznsAction</span></span>
<span data-ttu-id="9949b-111">Сведения о действии AzNS</span><span class="sxs-lookup"><span data-stu-id="9949b-111">The AzNS action details</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9949b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9949b-112">-DefaultProfile</span></span>
<span data-ttu-id="9949b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9949b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9949b-114">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="9949b-114">-Severity</span></span>
<span data-ttu-id="9949b-115">Уровень важности для этого оповещения.</span><span class="sxs-lookup"><span data-stu-id="9949b-115">The severity for this alert</span></span>

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

### <span data-ttu-id="9949b-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="9949b-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="9949b-117">Продолжительность (в минутах), за которую следует регулировать оповещение</span><span class="sxs-lookup"><span data-stu-id="9949b-117">The duration in minutes for which alert should be throttled</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9949b-118">-Триггер</span><span class="sxs-lookup"><span data-stu-id="9949b-118">-Trigger</span></span>
<span data-ttu-id="9949b-119">Условие триггера оповещения</span><span class="sxs-lookup"><span data-stu-id="9949b-119">The alert trigger condition</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleTriggerCondition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9949b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9949b-120">CommonParameters</span></span>
<span data-ttu-id="9949b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9949b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9949b-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9949b-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9949b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9949b-123">INPUTS</span></span>

### <span data-ttu-id="9949b-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="9949b-124">None</span></span>

## <span data-ttu-id="9949b-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9949b-125">OUTPUTS</span></span>

### <span data-ttu-id="9949b-126">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="9949b-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="9949b-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="9949b-127">NOTES</span></span>

## <span data-ttu-id="9949b-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9949b-128">RELATED LINKS</span></span>
