---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: aec627fdc8889d6bcfc4fb8e7762eb3be7bf0432
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902250"
---
# <span data-ttu-id="7b5f2-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="7b5f2-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="7b5f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b5f2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5f2-103">Создание условия соответствия для настраиваемого правила</span><span class="sxs-lookup"><span data-stu-id="7b5f2-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="7b5f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b5f2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b5f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b5f2-105">DESCRIPTION</span></span>
<span data-ttu-id="7b5f2-106">Параметр **New-AzApplicationGatewayFirewallCondition** создает условие соответствия для настраиваемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="7b5f2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b5f2-107">EXAMPLES</span></span>

### <span data-ttu-id="7b5f2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b5f2-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallConditon -MatchVariables $variable -Operator Contains -NegationConditon false -Transforms Lowercase, Trim -MatchValues abc, cde
```

<span data-ttu-id="7b5f2-109">Команда создает новое условие соответствия, используя переменную Match, определенную в $variable, оператор содержит условие отрицания, имеет значение ложь, передается в том числе строчными и усеченными значениями Match.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="7b5f2-110">Новое условие соответствия сохраняется в $condition.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="7b5f2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b5f2-111">PARAMETERS</span></span>

### <span data-ttu-id="7b5f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5f2-112">-DefaultProfile</span></span>
<span data-ttu-id="7b5f2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b5f2-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="7b5f2-114">-MatchValue</span></span>
<span data-ttu-id="7b5f2-115">Значение match.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-115">Match value.</span></span>

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

### <span data-ttu-id="7b5f2-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="7b5f2-116">-MatchVariable</span></span>
<span data-ttu-id="7b5f2-117">Список переменных соответствия.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-117">List of match variables.</span></span>

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

### <span data-ttu-id="7b5f2-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="7b5f2-118">-NegationCondition</span></span>
<span data-ttu-id="7b5f2-119">Описывает, является ли это условие противоположным.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="7b5f2-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="7b5f2-120">-Operator</span></span>
<span data-ttu-id="7b5f2-121">Описывает оператор, с которым должен выполняться поиск.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="7b5f2-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="7b5f2-122">-Transform</span></span>
<span data-ttu-id="7b5f2-123">Список преобразований.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-123">List of transforms.</span></span>

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

### <span data-ttu-id="7b5f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5f2-124">CommonParameters</span></span>
<span data-ttu-id="7b5f2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b5f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5f2-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b5f2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5f2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b5f2-127">INPUTS</span></span>

### <span data-ttu-id="7b5f2-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="7b5f2-128">None</span></span>

## <span data-ttu-id="7b5f2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b5f2-129">OUTPUTS</span></span>

### <span data-ttu-id="7b5f2-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="7b5f2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="7b5f2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b5f2-131">NOTES</span></span>

## <span data-ttu-id="7b5f2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b5f2-132">RELATED LINKS</span></span>
