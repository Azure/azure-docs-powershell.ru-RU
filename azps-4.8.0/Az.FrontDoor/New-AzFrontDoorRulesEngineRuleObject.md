---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077755"
---
# <span data-ttu-id="81968-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="81968-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="81968-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81968-102">SYNOPSIS</span></span>
<span data-ttu-id="81968-103">Создайте объект PSRulesEngineRule для создания обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="81968-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="81968-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81968-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81968-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81968-105">DESCRIPTION</span></span>
<span data-ttu-id="81968-106">Создайте объект PSRulesEngineRule для создания обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="81968-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="81968-107">Используйте командлет "New-AzFrontDoorRulesEngineActionObject", чтобы создать объект PSRulesEngineAction для передачи в параметр "-Action".</span><span class="sxs-lookup"><span data-stu-id="81968-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="81968-108">Используйте командлет "New-AzFrontDoorRulesEngineMatchConditionObject", чтобы создать объект PSRulesEngineMatchCondition для передачи в параметр "-MatchCondition".</span><span class="sxs-lookup"><span data-stu-id="81968-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="81968-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81968-109">EXAMPLES</span></span>

### <span data-ttu-id="81968-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="81968-110">Example 1</span></span>
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

<span data-ttu-id="81968-111">Создайте новый объект PSRulesEngineRule и покажите, как просмотреть подполя.</span><span class="sxs-lookup"><span data-stu-id="81968-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="81968-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="81968-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="81968-113">Ожидать вывода при передаче недопустимых значений приоритета.</span><span class="sxs-lookup"><span data-stu-id="81968-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="81968-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81968-114">PARAMETERS</span></span>

### <span data-ttu-id="81968-115">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="81968-115">-Action</span></span>
<span data-ttu-id="81968-116">Действия, которые необходимо выполнить для запроса и ответа, если все условия соответствия выполняются.</span><span class="sxs-lookup"><span data-stu-id="81968-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

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

### <span data-ttu-id="81968-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81968-117">-DefaultProfile</span></span>
<span data-ttu-id="81968-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81968-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81968-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="81968-119">-MatchCondition</span></span>
<span data-ttu-id="81968-120">Список условий соответствия, которые должны соблюдаться в соответствии с действиями, которые необходимо выполнить для этого правила.</span><span class="sxs-lookup"><span data-stu-id="81968-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="81968-121">Отсутствие соответствия условиям означает, что действия будут всегда выполняться.</span><span class="sxs-lookup"><span data-stu-id="81968-121">Having no match conditions means the actions will always run.</span></span>

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

### <span data-ttu-id="81968-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="81968-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="81968-123">Если это правило является соответствием, необходимо, чтобы обработчик правил продолжал выполнение оставшихся правил или остановиться.</span><span class="sxs-lookup"><span data-stu-id="81968-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="81968-124">Возможные значения: продолжение и остановка.</span><span class="sxs-lookup"><span data-stu-id="81968-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="81968-125">Если этот режим отсутствует, по умолчанию используется значение продолжить.</span><span class="sxs-lookup"><span data-stu-id="81968-125">If not present, defaults to Continue.</span></span>

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

### <span data-ttu-id="81968-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81968-126">-Name</span></span>
<span data-ttu-id="81968-127">Имя, которое будет содержаться в этом конкретном правиле.</span><span class="sxs-lookup"><span data-stu-id="81968-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="81968-128">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="81968-128">-Priority</span></span>
<span data-ttu-id="81968-129">Приоритет, назначенный этому правилу.</span><span class="sxs-lookup"><span data-stu-id="81968-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="81968-130">Не может быть отрицательным.</span><span class="sxs-lookup"><span data-stu-id="81968-130">Cannot be negative.</span></span>

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

### <span data-ttu-id="81968-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81968-131">CommonParameters</span></span>
<span data-ttu-id="81968-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81968-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81968-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81968-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81968-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81968-134">INPUTS</span></span>

### <span data-ttu-id="81968-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="81968-135">None</span></span>

## <span data-ttu-id="81968-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81968-136">OUTPUTS</span></span>

### <span data-ttu-id="81968-137">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="81968-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="81968-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="81968-138">NOTES</span></span>

## <span data-ttu-id="81968-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81968-139">RELATED LINKS</span></span>
