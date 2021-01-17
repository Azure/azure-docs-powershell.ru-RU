---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416007"
---
# <span data-ttu-id="6a5c3-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="6a5c3-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="6a5c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5c3-103">Создайте объект исключения для управляемых наборов правил, групп или правил WAF.</span><span class="sxs-lookup"><span data-stu-id="6a5c3-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="6a5c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a5c3-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a5c3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a5c3-105">DESCRIPTION</span></span>
<span data-ttu-id="6a5c3-106">Создайте объект исключения для управляемых наборов правил, групп или правил WAF.</span><span class="sxs-lookup"><span data-stu-id="6a5c3-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="6a5c3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a5c3-107">EXAMPLES</span></span>

### <span data-ttu-id="6a5c3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a5c3-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="6a5c3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a5c3-109">PARAMETERS</span></span>

### <span data-ttu-id="6a5c3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5c3-110">-DefaultProfile</span></span>
<span data-ttu-id="6a5c3-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a5c3-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a5c3-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="6a5c3-112">-Operator</span></span>
<span data-ttu-id="6a5c3-113">Оператор, который используется при совпадении с селектором, EqualsAny означает отсутствие селектора (все переменные совпадения указанного типа)</span><span class="sxs-lookup"><span data-stu-id="6a5c3-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="6a5c3-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="6a5c3-114">-Selector</span></span>
<span data-ttu-id="6a5c3-115">Шаблон селектора для совпадения с использованием оператора (если оператор не равно "РавноAny")</span><span class="sxs-lookup"><span data-stu-id="6a5c3-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a5c3-116">-Variable</span><span class="sxs-lookup"><span data-stu-id="6a5c3-116">-Variable</span></span>
<span data-ttu-id="6a5c3-117">Переменная match.</span><span class="sxs-lookup"><span data-stu-id="6a5c3-117">Match variable.</span></span> <span data-ttu-id="6a5c3-118">Возможные значения: RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="6a5c3-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="6a5c3-119">Например, QueryStringArgNames — это исключение параметров GET, которые соответствуют выборке с заданным оператором.</span><span class="sxs-lookup"><span data-stu-id="6a5c3-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="6a5c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5c3-120">CommonParameters</span></span>
<span data-ttu-id="6a5c3-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a5c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5c3-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a5c3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5c3-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a5c3-123">INPUTS</span></span>

### <span data-ttu-id="6a5c3-124">Нет</span><span class="sxs-lookup"><span data-stu-id="6a5c3-124">None</span></span>

## <span data-ttu-id="6a5c3-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a5c3-125">OUTPUTS</span></span>

### <span data-ttu-id="6a5c3-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="6a5c3-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="6a5c3-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a5c3-127">NOTES</span></span>

## <span data-ttu-id="6a5c3-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a5c3-128">RELATED LINKS</span></span>

<span data-ttu-id="6a5c3-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="6a5c3-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
