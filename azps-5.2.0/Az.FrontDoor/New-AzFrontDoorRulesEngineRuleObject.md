---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328652"
---
# <span data-ttu-id="7f5ee-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="7f5ee-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="7f5ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f5ee-102">SYNOPSIS</span></span>
<span data-ttu-id="7f5ee-103">Создайте объект PSRulesEngineRule для создания обн. правил.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="7f5ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f5ee-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f5ee-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f5ee-105">DESCRIPTION</span></span>
<span data-ttu-id="7f5ee-106">Создайте объект PSRulesEngineRule для создания обн. правил.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="7f5ee-107">Используйте cmdlet "New-AzFrontDoorRulesEngineActionObject" для создания объекта PSRulesEngineAction, который передается в параметр "-Action".</span><span class="sxs-lookup"><span data-stu-id="7f5ee-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="7f5ee-108">Используйте командлет "New-AzFrontDoorRulesEngineMatchConditionObject" для создания объекта PSRulesEngineMatchCondition, который будет передаваться в параметр "-MatchCondition".</span><span class="sxs-lookup"><span data-stu-id="7f5ee-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="7f5ee-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f5ee-109">EXAMPLES</span></span>

### <span data-ttu-id="7f5ee-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7f5ee-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="7f5ee-111">Создайте новый объект PSRulesEngineRule и продемонстрируйте, как увидеть подполя.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="7f5ee-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7f5ee-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="7f5ee-113">Ожидается вывод при передаче недопустимого значения приоритета.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="7f5ee-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f5ee-114">PARAMETERS</span></span>

### <span data-ttu-id="7f5ee-115">-Action</span><span class="sxs-lookup"><span data-stu-id="7f5ee-115">-Action</span></span>
<span data-ttu-id="7f5ee-116">Действия, выполняемые с запросом и ответом, если выполняются все условия совпадения.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f5ee-117">-DefaultProfile</span></span>
<span data-ttu-id="7f5ee-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f5ee-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="7f5ee-119">-MatchCondition</span></span>
<span data-ttu-id="7f5ee-120">Список условий совпадений, которые должны выполняться для действий этого правила.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="7f5ee-121">Отсутствие условий совпадения означает, что действия будут всегда запускаться.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5ee-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="7f5ee-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="7f5ee-123">Если это правило соответствует, должно ли обл. правила продолжать использовать оставшиеся правила или остановиться.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="7f5ee-124">Возможные значения: "Продолжить" и "Остановить".</span><span class="sxs-lookup"><span data-stu-id="7f5ee-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="7f5ee-125">Если нет, по умолчанию для продолжения.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5ee-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7f5ee-126">-Name</span></span>
<span data-ttu-id="7f5ee-127">Имя, на которое ссылаются данное правило.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="7f5ee-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="7f5ee-128">-Priority</span></span>
<span data-ttu-id="7f5ee-129">Приоритет, присвоенный этому правилу.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="7f5ee-130">Не может быть отрицательным.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-130">Cannot be negative.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f5ee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f5ee-131">CommonParameters</span></span>
<span data-ttu-id="7f5ee-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f5ee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f5ee-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f5ee-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f5ee-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f5ee-134">INPUTS</span></span>

### <span data-ttu-id="7f5ee-135">Нет</span><span class="sxs-lookup"><span data-stu-id="7f5ee-135">None</span></span>

## <span data-ttu-id="7f5ee-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f5ee-136">OUTPUTS</span></span>

### <span data-ttu-id="7f5ee-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="7f5ee-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="7f5ee-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f5ee-138">NOTES</span></span>

## <span data-ttu-id="7f5ee-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f5ee-139">RELATED LINKS</span></span>
