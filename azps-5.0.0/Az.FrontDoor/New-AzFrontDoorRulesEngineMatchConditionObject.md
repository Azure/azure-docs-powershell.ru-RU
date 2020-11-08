---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247411"
---
# <span data-ttu-id="406d0-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="406d0-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="406d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="406d0-102">SYNOPSIS</span></span>
<span data-ttu-id="406d0-103">Создайте объект PSRulesEngineMatchCondition для создания правила обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="406d0-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="406d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="406d0-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="406d0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="406d0-105">DESCRIPTION</span></span>
<span data-ttu-id="406d0-106">Создайте объект PSRulesEngineMatchCondition для создания правила обработчика правил.</span><span class="sxs-lookup"><span data-stu-id="406d0-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="406d0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="406d0-107">EXAMPLES</span></span>

### <span data-ttu-id="406d0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="406d0-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="406d0-109">Создайте новый объект PSRulesEngineMatchCondition.</span><span class="sxs-lookup"><span data-stu-id="406d0-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="406d0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="406d0-110">PARAMETERS</span></span>

### <span data-ttu-id="406d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406d0-111">-DefaultProfile</span></span>
<span data-ttu-id="406d0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="406d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="406d0-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="406d0-113">-MatchValue</span></span>
<span data-ttu-id="406d0-114">Сопоставленные значения с соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="406d0-114">Match values to match against.</span></span>
<span data-ttu-id="406d0-115">Оператор будет применен к каждому значению в этой статье с семантикой.</span><span class="sxs-lookup"><span data-stu-id="406d0-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="406d0-116">Если какой-либо из них соответствует переменной с указанным оператором, это условие соответствия считается совпадением.</span><span class="sxs-lookup"><span data-stu-id="406d0-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406d0-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="406d0-117">-MatchVariable</span></span>
<span data-ttu-id="406d0-118">Переменная Match.</span><span class="sxs-lookup"><span data-stu-id="406d0-118">Match Variable.</span></span>
<span data-ttu-id="406d0-119">Возможны значения для RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader</span><span class="sxs-lookup"><span data-stu-id="406d0-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406d0-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="406d0-120">-NegateCondition</span></span>
<span data-ttu-id="406d0-121">Описывает, является ли это условие противоположным.</span><span class="sxs-lookup"><span data-stu-id="406d0-121">Describes if this is negate condition or not</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406d0-122">-Operator</span><span class="sxs-lookup"><span data-stu-id="406d0-122">-Operator</span></span>
<span data-ttu-id="406d0-123">Описывает оператор, применяемый к условию соответствия.</span><span class="sxs-lookup"><span data-stu-id="406d0-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="406d0-124">Возможные значения: Any, IPMatch, геоmatching, Equals, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="406d0-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406d0-125">-Selector</span><span class="sxs-lookup"><span data-stu-id="406d0-125">-Selector</span></span>
<span data-ttu-id="406d0-126">Имя селектора в RequestHeader или RequestBody для сопоставления</span><span class="sxs-lookup"><span data-stu-id="406d0-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="406d0-127">-Transform</span><span class="sxs-lookup"><span data-stu-id="406d0-127">-Transform</span></span>
<span data-ttu-id="406d0-128">Список преобразований, которые применяются перед совпадением.</span><span class="sxs-lookup"><span data-stu-id="406d0-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="406d0-129">Возможные значения отдельных преобразований: строчные, прописные, Trim, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="406d0-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="406d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406d0-130">CommonParameters</span></span>
<span data-ttu-id="406d0-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="406d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406d0-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="406d0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406d0-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="406d0-133">INPUTS</span></span>

### <span data-ttu-id="406d0-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="406d0-134">None</span></span>

## <span data-ttu-id="406d0-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="406d0-135">OUTPUTS</span></span>

### <span data-ttu-id="406d0-136">Microsoft. Azure. Commands. FrontDoor. Models. PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="406d0-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="406d0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="406d0-137">NOTES</span></span>

## <span data-ttu-id="406d0-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="406d0-138">RELATED LINKS</span></span>
