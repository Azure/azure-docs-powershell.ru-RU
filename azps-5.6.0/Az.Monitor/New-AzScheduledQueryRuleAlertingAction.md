---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryrulealertingaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAlertingAction.md
ms.openlocfilehash: 0394aa7c2db880bbb10c8d68c9d502560c1035bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961811"
---
# <span data-ttu-id="7f836-101">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7f836-101">New-AzScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="7f836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f836-102">SYNOPSIS</span></span>
<span data-ttu-id="7f836-103">Создание объекта с оповещением типа</span><span class="sxs-lookup"><span data-stu-id="7f836-103">Creates an object of type Alerting Action</span></span>

## <span data-ttu-id="7f836-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f836-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAlertingAction [-AznsAction <PSScheduledQueryRuleAznsAction>] -Severity <String>
 [-ThrottlingInMinutes <Int32>] -Trigger <PSScheduledQueryRuleTriggerCondition>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f836-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f836-105">DESCRIPTION</span></span>
<span data-ttu-id="7f836-106">Создает объект с действием "Оповещать этот объект", который передается команде, создав правило оповещения журнала.</span><span class="sxs-lookup"><span data-stu-id="7f836-106">Creates an object of type Alerting Action This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="7f836-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f836-107">EXAMPLES</span></span>

### <span data-ttu-id="7f836-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f836-108">Example 1</span></span>
```powershell
PS C:\> $alertingAction = New-AzScheduledQueryRuleAlertingAction -AznsAction $aznsActionGroup -Severity "1" -Trigger $triggerCondition
```

## <span data-ttu-id="7f836-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f836-109">PARAMETERS</span></span>

### <span data-ttu-id="7f836-110">-AznsAction</span><span class="sxs-lookup"><span data-stu-id="7f836-110">-AznsAction</span></span>
<span data-ttu-id="7f836-111">Сведения о действиях AzNS</span><span class="sxs-lookup"><span data-stu-id="7f836-111">The AzNS action details</span></span>

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

### <span data-ttu-id="7f836-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f836-112">-DefaultProfile</span></span>
<span data-ttu-id="7f836-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f836-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f836-114">-Severity</span><span class="sxs-lookup"><span data-stu-id="7f836-114">-Severity</span></span>
<span data-ttu-id="7f836-115">Серьезность этого оповещения</span><span class="sxs-lookup"><span data-stu-id="7f836-115">The severity for this alert</span></span>

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

### <span data-ttu-id="7f836-116">-ThrottlingInMinutes</span><span class="sxs-lookup"><span data-stu-id="7f836-116">-ThrottlingInMinutes</span></span>
<span data-ttu-id="7f836-117">Длительность в минутах, для которых нужно регулирование оповещений</span><span class="sxs-lookup"><span data-stu-id="7f836-117">The duration in minutes for which alert should be throttled</span></span>

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

### <span data-ttu-id="7f836-118">-Trigger</span><span class="sxs-lookup"><span data-stu-id="7f836-118">-Trigger</span></span>
<span data-ttu-id="7f836-119">Условие триггера оповещения</span><span class="sxs-lookup"><span data-stu-id="7f836-119">The alert trigger condition</span></span>

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

### <span data-ttu-id="7f836-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f836-120">CommonParameters</span></span>
<span data-ttu-id="7f836-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f836-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f836-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f836-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f836-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f836-123">INPUTS</span></span>

### <span data-ttu-id="7f836-124">Нет</span><span class="sxs-lookup"><span data-stu-id="7f836-124">None</span></span>

## <span data-ttu-id="7f836-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f836-125">OUTPUTS</span></span>

### <span data-ttu-id="7f836-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7f836-126">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="7f836-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f836-127">NOTES</span></span>

## <span data-ttu-id="7f836-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f836-128">RELATED LINKS</span></span>
