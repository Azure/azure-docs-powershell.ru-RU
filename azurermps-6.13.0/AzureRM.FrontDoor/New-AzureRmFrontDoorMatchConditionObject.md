---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732929"
---
# <span data-ttu-id="25c98-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="25c98-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="25c98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25c98-102">SYNOPSIS</span></span>
<span data-ttu-id="25c98-103">Создание объекта MatchCondition для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="25c98-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25c98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25c98-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25c98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25c98-105">DESCRIPTION</span></span>
<span data-ttu-id="25c98-106">Создание объекта MatchCondition для создания политики WAF</span><span class="sxs-lookup"><span data-stu-id="25c98-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="25c98-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25c98-107">EXAMPLES</span></span>

### <span data-ttu-id="25c98-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="25c98-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="25c98-109">Создание объекта MatchCondition</span><span class="sxs-lookup"><span data-stu-id="25c98-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="25c98-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25c98-110">PARAMETERS</span></span>

### <span data-ttu-id="25c98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c98-111">-DefaultProfile</span></span>
<span data-ttu-id="25c98-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25c98-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25c98-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="25c98-113">-MatchValue</span></span>
<span data-ttu-id="25c98-114">Значение match.</span><span class="sxs-lookup"><span data-stu-id="25c98-114">Match value.</span></span>

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

### <span data-ttu-id="25c98-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="25c98-115">-MatchVariable</span></span>
<span data-ttu-id="25c98-116">Переменная Match.</span><span class="sxs-lookup"><span data-stu-id="25c98-116">Match Variable.</span></span>
<span data-ttu-id="25c98-117">Возможные значения: "RemoteAddr", "RequestMethod", "QueryString", "i args", "RequestUri", "RequestHeader", "RequestBody"</span><span class="sxs-lookup"><span data-stu-id="25c98-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="25c98-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="25c98-118">-NegateCondition</span></span>
<span data-ttu-id="25c98-119">Описывает, является ли это условием отрицания или значение по умолчанию — false</span><span class="sxs-lookup"><span data-stu-id="25c98-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="25c98-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="25c98-120">-OperatorProperty</span></span>
<span data-ttu-id="25c98-121">Описывает оператор, с которым должен выполняться поиск.</span><span class="sxs-lookup"><span data-stu-id="25c98-121">Describes operator to be matched.</span></span>
<span data-ttu-id="25c98-122">Возможные значения: "Any", "IPMatch", "геоmatch", "равно", "содержит", "LessThan", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "BeginsWith", "EndsWith"</span><span class="sxs-lookup"><span data-stu-id="25c98-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

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

### <span data-ttu-id="25c98-123">-Selector</span><span class="sxs-lookup"><span data-stu-id="25c98-123">-Selector</span></span>
<span data-ttu-id="25c98-124">Имя селектора в RequestHeader или RequestBody для сопоставления</span><span class="sxs-lookup"><span data-stu-id="25c98-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="25c98-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c98-125">CommonParameters</span></span>
<span data-ttu-id="25c98-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25c98-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c98-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25c98-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c98-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25c98-128">INPUTS</span></span>

### <span data-ttu-id="25c98-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="25c98-129">None</span></span>

## <span data-ttu-id="25c98-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25c98-130">OUTPUTS</span></span>

### <span data-ttu-id="25c98-131">Microsoft. Azure. Commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="25c98-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="25c98-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="25c98-132">NOTES</span></span>

## <span data-ttu-id="25c98-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25c98-133">RELATED LINKS</span></span>

[<span data-ttu-id="25c98-134">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="25c98-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
