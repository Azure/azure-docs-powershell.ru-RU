---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900601"
---
# <span data-ttu-id="0a43f-101">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0a43f-101">New-AzFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="0a43f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a43f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a43f-103">Создание объекта MatchCondition для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="0a43f-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="0a43f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a43f-104">SYNTAX</span></span>

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a43f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a43f-105">DESCRIPTION</span></span>
<span data-ttu-id="0a43f-106">Создание объекта MatchCondition для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="0a43f-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="0a43f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a43f-107">EXAMPLES</span></span>

### <span data-ttu-id="0a43f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a43f-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

<span data-ttu-id="0a43f-109">Создание объекта MatchCondition</span><span class="sxs-lookup"><span data-stu-id="0a43f-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="0a43f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a43f-110">PARAMETERS</span></span>

### <span data-ttu-id="0a43f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a43f-111">-DefaultProfile</span></span>
<span data-ttu-id="0a43f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a43f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a43f-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="0a43f-113">-MatchValue</span></span>
<span data-ttu-id="0a43f-114">Значение match.</span><span class="sxs-lookup"><span data-stu-id="0a43f-114">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a43f-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="0a43f-115">-MatchVariable</span></span>
<span data-ttu-id="0a43f-116">Переменная Match.</span><span class="sxs-lookup"><span data-stu-id="0a43f-116">Match Variable.</span></span>
<span data-ttu-id="0a43f-117">Возможные значения: "RemoteAddr", "RequestMethod", "QueryString", "i args", "RequestUri", "RequestHeader", "RequestBody"</span><span class="sxs-lookup"><span data-stu-id="0a43f-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a43f-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="0a43f-118">-NegateCondition</span></span>
<span data-ttu-id="0a43f-119">Описывает, является ли это условием отрицания или значение по умолчанию — false</span><span class="sxs-lookup"><span data-stu-id="0a43f-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="0a43f-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="0a43f-120">-OperatorProperty</span></span>
<span data-ttu-id="0a43f-121">Описывает оператор, с которым должен выполняться поиск.</span><span class="sxs-lookup"><span data-stu-id="0a43f-121">Describes operator to be matched.</span></span>
<span data-ttu-id="0a43f-122">Возможные значения: "Any", "IPMatch", "геоmatch", "равно", "содержит", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "BeginsWith", "EndsWith"</span><span class="sxs-lookup"><span data-stu-id="0a43f-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a43f-123">-Selector</span><span class="sxs-lookup"><span data-stu-id="0a43f-123">-Selector</span></span>
<span data-ttu-id="0a43f-124">Имя селектора в RequestHeader или RequestBody для сопоставления</span><span class="sxs-lookup"><span data-stu-id="0a43f-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="0a43f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a43f-125">CommonParameters</span></span>
<span data-ttu-id="0a43f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a43f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a43f-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a43f-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a43f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a43f-128">INPUTS</span></span>

### <span data-ttu-id="0a43f-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="0a43f-129">None</span></span>

## <span data-ttu-id="0a43f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a43f-130">OUTPUTS</span></span>

### <span data-ttu-id="0a43f-131">Microsoft. Azure. Commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="0a43f-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="0a43f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a43f-132">NOTES</span></span>

## <span data-ttu-id="0a43f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a43f-133">RELATED LINKS</span></span>

[<span data-ttu-id="0a43f-134">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="0a43f-134">New-AzFrontDoorCustomRuleObject</span></span>](./New-AzFrontDoorCustomRuleObject.md)
