---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244522"
---
# <span data-ttu-id="0104f-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="0104f-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="0104f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0104f-102">SYNOPSIS</span></span>
<span data-ttu-id="0104f-103">Создайте объект исключения управляемого правила для наборов управляемых правил WAF, групп или правил.</span><span class="sxs-lookup"><span data-stu-id="0104f-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="0104f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0104f-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0104f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0104f-105">DESCRIPTION</span></span>
<span data-ttu-id="0104f-106">Создайте объект исключения управляемого правила для наборов управляемых правил WAF, групп или правил.</span><span class="sxs-lookup"><span data-stu-id="0104f-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="0104f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0104f-107">EXAMPLES</span></span>

### <span data-ttu-id="0104f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0104f-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="0104f-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0104f-109">PARAMETERS</span></span>

### <span data-ttu-id="0104f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0104f-110">-DefaultProfile</span></span>
<span data-ttu-id="0104f-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0104f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0104f-112">-Operator</span><span class="sxs-lookup"><span data-stu-id="0104f-112">-Operator</span></span>
<span data-ttu-id="0104f-113">Оператор, который будет использоваться при сопоставлении Selector, EqualsAny означает, что селектор (все переменные соответствия указанному типу) не выбраны.</span><span class="sxs-lookup"><span data-stu-id="0104f-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

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

### <span data-ttu-id="0104f-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="0104f-114">-Selector</span></span>
<span data-ttu-id="0104f-115">Шаблон Selector для поиска соответствия с помощью оператора (если оператор не является EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="0104f-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="0104f-116">-Variable</span><span class="sxs-lookup"><span data-stu-id="0104f-116">-Variable</span></span>
<span data-ttu-id="0104f-117">Переменная Match.</span><span class="sxs-lookup"><span data-stu-id="0104f-117">Match variable.</span></span> <span data-ttu-id="0104f-118">Возможные значения: RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="0104f-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="0104f-119">Например, QueryStringArgNames является исключением параметров GET, отвечающих селектору с помощью заданного оператора.</span><span class="sxs-lookup"><span data-stu-id="0104f-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

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

### <span data-ttu-id="0104f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0104f-120">CommonParameters</span></span>
<span data-ttu-id="0104f-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0104f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0104f-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0104f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0104f-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0104f-123">INPUTS</span></span>

### <span data-ttu-id="0104f-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="0104f-124">None</span></span>

## <span data-ttu-id="0104f-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0104f-125">OUTPUTS</span></span>

### <span data-ttu-id="0104f-126">Microsoft. Azure. Commands. FrontDoor. Models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="0104f-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="0104f-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="0104f-127">NOTES</span></span>

## <span data-ttu-id="0104f-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0104f-128">RELATED LINKS</span></span>

<span data-ttu-id="0104f-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="0104f-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
