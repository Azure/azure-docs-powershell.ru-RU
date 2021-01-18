---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504874"
---
# <span data-ttu-id="baad4-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="baad4-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="baad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baad4-102">SYNOPSIS</span></span>
<span data-ttu-id="baad4-103">Создайте объект исключения для управляемых наборов правил, групп или правил WAF.</span><span class="sxs-lookup"><span data-stu-id="baad4-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="baad4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="baad4-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baad4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baad4-105">DESCRIPTION</span></span>
<span data-ttu-id="baad4-106">Создайте объект исключения для управляемых наборов правил, групп или правил WAF.</span><span class="sxs-lookup"><span data-stu-id="baad4-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="baad4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="baad4-107">EXAMPLES</span></span>

### <span data-ttu-id="baad4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="baad4-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="baad4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baad4-109">PARAMETERS</span></span>

### <span data-ttu-id="baad4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baad4-110">-DefaultProfile</span></span>
<span data-ttu-id="baad4-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baad4-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baad4-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="baad4-112">-Operator</span></span>
<span data-ttu-id="baad4-113">Оператор, который используется при совпадении с селектором, EqualsAny означает отсутствие селектора (все переменные совпадения указанного типа)</span><span class="sxs-lookup"><span data-stu-id="baad4-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="baad4-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="baad4-114">-Selector</span></span>
<span data-ttu-id="baad4-115">Шаблон селектора для совпадения с использованием оператора (если оператор не равно "РавноAny")</span><span class="sxs-lookup"><span data-stu-id="baad4-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="baad4-116">-Variable</span><span class="sxs-lookup"><span data-stu-id="baad4-116">-Variable</span></span>
<span data-ttu-id="baad4-117">Переменная match.</span><span class="sxs-lookup"><span data-stu-id="baad4-117">Match variable.</span></span> <span data-ttu-id="baad4-118">Возможные значения: RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="baad4-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="baad4-119">Например, QueryStringArgNames — это исключение параметров GET, которые соответствуют выборке с заданным оператором.</span><span class="sxs-lookup"><span data-stu-id="baad4-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="baad4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baad4-120">CommonParameters</span></span>
<span data-ttu-id="baad4-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baad4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baad4-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="baad4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baad4-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baad4-123">INPUTS</span></span>

### <span data-ttu-id="baad4-124">Нет</span><span class="sxs-lookup"><span data-stu-id="baad4-124">None</span></span>

## <span data-ttu-id="baad4-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="baad4-125">OUTPUTS</span></span>

### <span data-ttu-id="baad4-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="baad4-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="baad4-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="baad4-127">NOTES</span></span>

## <span data-ttu-id="baad4-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baad4-128">RELATED LINKS</span></span>

<span data-ttu-id="baad4-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="baad4-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
