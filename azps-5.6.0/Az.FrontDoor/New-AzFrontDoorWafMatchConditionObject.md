---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: e67841073d6c7342e0bb88c52809a9c45d92f82f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970840"
---
# <span data-ttu-id="5720b-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="5720b-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="5720b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5720b-102">SYNOPSIS</span></span>
<span data-ttu-id="5720b-103">Создание объекта MatchCondition для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="5720b-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="5720b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5720b-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5720b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5720b-105">DESCRIPTION</span></span>
<span data-ttu-id="5720b-106">Создание объекта MatchCondition для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="5720b-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="5720b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5720b-107">EXAMPLES</span></span>

### <span data-ttu-id="5720b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5720b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="5720b-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5720b-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="5720b-110">Создание объекта MatchCondition</span><span class="sxs-lookup"><span data-stu-id="5720b-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="5720b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5720b-111">PARAMETERS</span></span>

### <span data-ttu-id="5720b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5720b-112">-DefaultProfile</span></span>
<span data-ttu-id="5720b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5720b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5720b-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="5720b-114">-MatchValue</span></span>
<span data-ttu-id="5720b-115">Совпадает со значением.</span><span class="sxs-lookup"><span data-stu-id="5720b-115">Match value.</span></span>

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

### <span data-ttu-id="5720b-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="5720b-116">-MatchVariable</span></span>
<span data-ttu-id="5720b-117">Переменная match.</span><span class="sxs-lookup"><span data-stu-id="5720b-117">Match Variable.</span></span>
<span data-ttu-id="5720b-118">Возможные значения: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span><span class="sxs-lookup"><span data-stu-id="5720b-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="5720b-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="5720b-119">-NegateCondition</span></span>
<span data-ttu-id="5720b-120">В этой статье описывается, является ли это условием negate или значением по умолчанию не является ложь.</span><span class="sxs-lookup"><span data-stu-id="5720b-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="5720b-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="5720b-121">-OperatorProperty</span></span>
<span data-ttu-id="5720b-122">Оператор для совпадения.</span><span class="sxs-lookup"><span data-stu-id="5720b-122">Describes operator to be matched.</span></span>
<span data-ttu-id="5720b-123">Возможные значения: Any, 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span><span class="sxs-lookup"><span data-stu-id="5720b-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="5720b-124">-Selector</span><span class="sxs-lookup"><span data-stu-id="5720b-124">-Selector</span></span>
<span data-ttu-id="5720b-125">Имя селектора в RequestHeader или RequestBody для совпадения</span><span class="sxs-lookup"><span data-stu-id="5720b-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="5720b-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="5720b-126">-Transform</span></span>
<span data-ttu-id="5720b-127">Преобразования, которые нужно применить.</span><span class="sxs-lookup"><span data-stu-id="5720b-127">Transforms to apply.</span></span> <span data-ttu-id="5720b-128">Возможные значения: Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span><span class="sxs-lookup"><span data-stu-id="5720b-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="5720b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5720b-129">CommonParameters</span></span>
<span data-ttu-id="5720b-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5720b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5720b-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5720b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5720b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5720b-132">INPUTS</span></span>

### <span data-ttu-id="5720b-133">Нет</span><span class="sxs-lookup"><span data-stu-id="5720b-133">None</span></span>

## <span data-ttu-id="5720b-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5720b-134">OUTPUTS</span></span>

### <span data-ttu-id="5720b-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="5720b-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="5720b-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5720b-136">NOTES</span></span>

## <span data-ttu-id="5720b-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5720b-137">RELATED LINKS</span></span>

[<span data-ttu-id="5720b-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="5720b-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
