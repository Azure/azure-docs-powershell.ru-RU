---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 096fb182ae330750eeb23e365bc929edb17b21f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007747"
---
# <span data-ttu-id="dbb39-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="dbb39-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="dbb39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbb39-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb39-103">Создание условия для пользовательского правила</span><span class="sxs-lookup"><span data-stu-id="dbb39-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="dbb39-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dbb39-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbb39-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbb39-105">DESCRIPTION</span></span>
<span data-ttu-id="dbb39-106">**New-AzApplicationGatewayFirewallCondition** создает условие совпадения для настраиваемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="dbb39-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="dbb39-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dbb39-107">EXAMPLES</span></span>

### <span data-ttu-id="dbb39-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dbb39-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="dbb39-109">Команда создает новое условие совпадения с использованием переменной совпадения, определенной в $variable, оператором является "Содержит" и условие отрицания — false, Transfroms (нижний регистр и обрезка), значение совпадения — abc и cde.</span><span class="sxs-lookup"><span data-stu-id="dbb39-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="dbb39-110">Новое условие совпадения будет сохранено в $condition.</span><span class="sxs-lookup"><span data-stu-id="dbb39-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="dbb39-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbb39-111">PARAMETERS</span></span>

### <span data-ttu-id="dbb39-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb39-112">-DefaultProfile</span></span>
<span data-ttu-id="dbb39-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbb39-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbb39-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="dbb39-114">-MatchValue</span></span>
<span data-ttu-id="dbb39-115">"Совпадение".</span><span class="sxs-lookup"><span data-stu-id="dbb39-115">Match value.</span></span>

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

### <span data-ttu-id="dbb39-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="dbb39-116">-MatchVariable</span></span>
<span data-ttu-id="dbb39-117">Список переменных совпадения.</span><span class="sxs-lookup"><span data-stu-id="dbb39-117">List of match variables.</span></span>

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

### <span data-ttu-id="dbb39-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="dbb39-118">-NegationCondition</span></span>
<span data-ttu-id="dbb39-119">В этой статье описывается, является ли это условием negate.</span><span class="sxs-lookup"><span data-stu-id="dbb39-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="dbb39-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="dbb39-120">-Operator</span></span>
<span data-ttu-id="dbb39-121">Оператор для совпадения.</span><span class="sxs-lookup"><span data-stu-id="dbb39-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="dbb39-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="dbb39-122">-Transform</span></span>
<span data-ttu-id="dbb39-123">Список преобразований.</span><span class="sxs-lookup"><span data-stu-id="dbb39-123">List of transforms.</span></span>

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

### <span data-ttu-id="dbb39-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb39-124">CommonParameters</span></span>
<span data-ttu-id="dbb39-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbb39-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb39-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbb39-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb39-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbb39-127">INPUTS</span></span>

### <span data-ttu-id="dbb39-128">Нет</span><span class="sxs-lookup"><span data-stu-id="dbb39-128">None</span></span>

## <span data-ttu-id="dbb39-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbb39-129">OUTPUTS</span></span>

### <span data-ttu-id="dbb39-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="dbb39-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="dbb39-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dbb39-131">NOTES</span></span>

## <span data-ttu-id="dbb39-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbb39-132">RELATED LINKS</span></span>
