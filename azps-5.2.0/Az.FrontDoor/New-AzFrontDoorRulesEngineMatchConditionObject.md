---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328653"
---
# <span data-ttu-id="f1a22-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="f1a22-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="f1a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1a22-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a22-103">Создайте объект PSRulesEngineMatchCondition для создания правила обрезки правил.</span><span class="sxs-lookup"><span data-stu-id="f1a22-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="f1a22-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1a22-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1a22-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1a22-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a22-106">Создайте объект PSRulesEngineMatchCondition для создания правила обрезки правил.</span><span class="sxs-lookup"><span data-stu-id="f1a22-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="f1a22-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1a22-107">EXAMPLES</span></span>

### <span data-ttu-id="f1a22-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1a22-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="f1a22-109">Новый объект PSRulesEngineMatchCondition.</span><span class="sxs-lookup"><span data-stu-id="f1a22-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="f1a22-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1a22-110">PARAMETERS</span></span>

### <span data-ttu-id="f1a22-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a22-111">-DefaultProfile</span></span>
<span data-ttu-id="f1a22-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1a22-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1a22-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="f1a22-113">-MatchValue</span></span>
<span data-ttu-id="f1a22-114">Совпадают значения.</span><span class="sxs-lookup"><span data-stu-id="f1a22-114">Match values to match against.</span></span>
<span data-ttu-id="f1a22-115">Оператор будет применяться к каждому значению в этом окте с помощью семантики ИЛИ.</span><span class="sxs-lookup"><span data-stu-id="f1a22-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="f1a22-116">Если любая из них совпадает с переменной с заданным оператором, это условие считается совпадением.</span><span class="sxs-lookup"><span data-stu-id="f1a22-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

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

### <span data-ttu-id="f1a22-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="f1a22-117">-MatchVariable</span></span>
<span data-ttu-id="f1a22-118">Переменная match.</span><span class="sxs-lookup"><span data-stu-id="f1a22-118">Match Variable.</span></span>
<span data-ttu-id="f1a22-119">Возможные значения: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfimeExtension, RequestHeader, RequestBody, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="f1a22-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

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

### <span data-ttu-id="f1a22-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="f1a22-120">-NegateCondition</span></span>
<span data-ttu-id="f1a22-121">В этой статье описано, является ли это условием negate или нет.</span><span class="sxs-lookup"><span data-stu-id="f1a22-121">Describes if this is negate condition or not</span></span>

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

### <span data-ttu-id="f1a22-122">-Operator</span><span class="sxs-lookup"><span data-stu-id="f1a22-122">-Operator</span></span>
<span data-ttu-id="f1a22-123">Оператор, который нужно применить к условию совпадения.</span><span class="sxs-lookup"><span data-stu-id="f1a22-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="f1a22-124">Возможные значения: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span><span class="sxs-lookup"><span data-stu-id="f1a22-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

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

### <span data-ttu-id="f1a22-125">-Selector</span><span class="sxs-lookup"><span data-stu-id="f1a22-125">-Selector</span></span>
<span data-ttu-id="f1a22-126">Имя селектора в RequestHeader или RequestBody для совпадения</span><span class="sxs-lookup"><span data-stu-id="f1a22-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="f1a22-127">-Transform</span><span class="sxs-lookup"><span data-stu-id="f1a22-127">-Transform</span></span>
<span data-ttu-id="f1a22-128">Список преобразований, которые применяются перед соответствием.</span><span class="sxs-lookup"><span data-stu-id="f1a22-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="f1a22-129">Возможные значения индивидуальных преобразований: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="f1a22-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

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

### <span data-ttu-id="f1a22-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a22-130">CommonParameters</span></span>
<span data-ttu-id="f1a22-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a22-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a22-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1a22-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a22-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1a22-133">INPUTS</span></span>

### <span data-ttu-id="f1a22-134">Нет</span><span class="sxs-lookup"><span data-stu-id="f1a22-134">None</span></span>

## <span data-ttu-id="f1a22-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1a22-135">OUTPUTS</span></span>

### <span data-ttu-id="f1a22-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="f1a22-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="f1a22-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1a22-137">NOTES</span></span>

## <span data-ttu-id="f1a22-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1a22-138">RELATED LINKS</span></span>
