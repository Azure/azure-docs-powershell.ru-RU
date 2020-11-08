---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: 0340cbf8c71b0ab117f1ff967ec7c3bb3e32b8f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245451"
---
# <span data-ttu-id="d8011-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="d8011-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="d8011-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8011-102">SYNOPSIS</span></span>
<span data-ttu-id="d8011-103">Создание объекта MatchCondition для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="d8011-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="d8011-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8011-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8011-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8011-105">DESCRIPTION</span></span>
<span data-ttu-id="d8011-106">Создание объекта MatchCondition для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="d8011-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="d8011-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8011-107">EXAMPLES</span></span>

### <span data-ttu-id="d8011-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8011-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="d8011-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d8011-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="d8011-110">Создание объекта MatchCondition</span><span class="sxs-lookup"><span data-stu-id="d8011-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="d8011-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8011-111">PARAMETERS</span></span>

### <span data-ttu-id="d8011-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8011-112">-DefaultProfile</span></span>
<span data-ttu-id="d8011-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8011-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8011-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="d8011-114">-MatchValue</span></span>
<span data-ttu-id="d8011-115">Значение match.</span><span class="sxs-lookup"><span data-stu-id="d8011-115">Match value.</span></span>

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

### <span data-ttu-id="d8011-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="d8011-116">-MatchVariable</span></span>
<span data-ttu-id="d8011-117">Переменная Match.</span><span class="sxs-lookup"><span data-stu-id="d8011-117">Match Variable.</span></span>
<span data-ttu-id="d8011-118">Возможные значения: "RemoteAddr", "RequestMethod", "QueryString", "i args", "RequestUri", "RequestHeader", "RequestBody" и "SocketAddr"</span><span class="sxs-lookup"><span data-stu-id="d8011-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody', 'SocketAddr'</span></span>

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

### <span data-ttu-id="d8011-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="d8011-119">-NegateCondition</span></span>
<span data-ttu-id="d8011-120">Описывает, является ли это условием отрицания или значение по умолчанию — false</span><span class="sxs-lookup"><span data-stu-id="d8011-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="d8011-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="d8011-121">-OperatorProperty</span></span>
<span data-ttu-id="d8011-122">Описывает оператор, с которым должен выполняться поиск.</span><span class="sxs-lookup"><span data-stu-id="d8011-122">Describes operator to be matched.</span></span>
<span data-ttu-id="d8011-123">Возможные значения: "Any", "IPMatch", "геоmatch", "равно", "содержит", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "BeginsWith", "EndsWith" и "регулярное выражение"</span><span class="sxs-lookup"><span data-stu-id="d8011-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="d8011-124">-Selector</span><span class="sxs-lookup"><span data-stu-id="d8011-124">-Selector</span></span>
<span data-ttu-id="d8011-125">Имя селектора в RequestHeader или RequestBody для сопоставления</span><span class="sxs-lookup"><span data-stu-id="d8011-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="d8011-126">-Transform</span><span class="sxs-lookup"><span data-stu-id="d8011-126">-Transform</span></span>
<span data-ttu-id="d8011-127">Преобразования для применения.</span><span class="sxs-lookup"><span data-stu-id="d8011-127">Transforms to apply.</span></span> <span data-ttu-id="d8011-128">Возможные значения: "строчные", "прописные", "обрезать", "UrlDecode", "UrlEncode", "RemoveNulls".</span><span class="sxs-lookup"><span data-stu-id="d8011-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

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

### <span data-ttu-id="d8011-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8011-129">CommonParameters</span></span>
<span data-ttu-id="d8011-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8011-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8011-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8011-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8011-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8011-132">INPUTS</span></span>

### <span data-ttu-id="d8011-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="d8011-133">None</span></span>

## <span data-ttu-id="d8011-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8011-134">OUTPUTS</span></span>

### <span data-ttu-id="d8011-135">Microsoft. Azure. Commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="d8011-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="d8011-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8011-136">NOTES</span></span>

## <span data-ttu-id="d8011-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8011-137">RELATED LINKS</span></span>

[<span data-ttu-id="d8011-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="d8011-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
