---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243028"
---
# <span data-ttu-id="33bdd-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="33bdd-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="33bdd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="33bdd-103">Создание условия соответствия для настраиваемого правила</span><span class="sxs-lookup"><span data-stu-id="33bdd-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="33bdd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33bdd-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33bdd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="33bdd-106">Параметр **New-AzApplicationGatewayFirewallCondition** создает условие соответствия для настраиваемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="33bdd-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="33bdd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="33bdd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="33bdd-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="33bdd-109">Команда создает новое условие соответствия, используя переменную Match, определенную в $variable, оператор содержит условие отрицания, имеет значение ложь, передается в том числе строчными и усеченными значениями Match.</span><span class="sxs-lookup"><span data-stu-id="33bdd-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="33bdd-110">Новое условие соответствия сохраняется в $condition.</span><span class="sxs-lookup"><span data-stu-id="33bdd-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="33bdd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33bdd-111">PARAMETERS</span></span>

### <span data-ttu-id="33bdd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33bdd-112">-DefaultProfile</span></span>
<span data-ttu-id="33bdd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33bdd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33bdd-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="33bdd-114">-MatchValue</span></span>
<span data-ttu-id="33bdd-115">Значение match.</span><span class="sxs-lookup"><span data-stu-id="33bdd-115">Match value.</span></span>

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

### <span data-ttu-id="33bdd-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="33bdd-116">-MatchVariable</span></span>
<span data-ttu-id="33bdd-117">Список переменных соответствия.</span><span class="sxs-lookup"><span data-stu-id="33bdd-117">List of match variables.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33bdd-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="33bdd-118">-NegationCondition</span></span>
<span data-ttu-id="33bdd-119">Описывает, является ли это условие противоположным.</span><span class="sxs-lookup"><span data-stu-id="33bdd-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="33bdd-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="33bdd-120">-Operator</span></span>
<span data-ttu-id="33bdd-121">Описывает оператор, с которым должен выполняться поиск.</span><span class="sxs-lookup"><span data-stu-id="33bdd-121">Describes operator to be matched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith, Regex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33bdd-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="33bdd-122">-Transform</span></span>
<span data-ttu-id="33bdd-123">Список преобразований.</span><span class="sxs-lookup"><span data-stu-id="33bdd-123">List of transforms.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Trim, UrlDecode, UrlEncode, RemoveNulls, HtmlEntityDecode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33bdd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33bdd-124">CommonParameters</span></span>
<span data-ttu-id="33bdd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33bdd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33bdd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33bdd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33bdd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33bdd-127">INPUTS</span></span>

### <span data-ttu-id="33bdd-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="33bdd-128">None</span></span>

## <span data-ttu-id="33bdd-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33bdd-129">OUTPUTS</span></span>

### <span data-ttu-id="33bdd-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="33bdd-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="33bdd-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="33bdd-131">NOTES</span></span>

## <span data-ttu-id="33bdd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33bdd-132">RELATED LINKS</span></span>