---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506484"
---
# <span data-ttu-id="29b56-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="29b56-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="29b56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29b56-102">SYNOPSIS</span></span>
<span data-ttu-id="29b56-103">Создание условия для пользовательского правила</span><span class="sxs-lookup"><span data-stu-id="29b56-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="29b56-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="29b56-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29b56-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29b56-105">DESCRIPTION</span></span>
<span data-ttu-id="29b56-106">**New-AzApplicationGatewayFirewallCondition** создает условие совпадения для настраиваемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="29b56-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="29b56-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="29b56-107">EXAMPLES</span></span>

### <span data-ttu-id="29b56-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29b56-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="29b56-109">Команда создает новое условие совпадения с использованием переменной совпадения, определенной в $variable, оператором является "Содержит" и условие отрицания — ложь, транспромы, включая нижний регистр и усеченный регистр, значение совпадения — "абв" и "cde".</span><span class="sxs-lookup"><span data-stu-id="29b56-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="29b56-110">Новое условие совпадения будет сохранено в $condition.</span><span class="sxs-lookup"><span data-stu-id="29b56-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="29b56-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29b56-111">PARAMETERS</span></span>

### <span data-ttu-id="29b56-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b56-112">-DefaultProfile</span></span>
<span data-ttu-id="29b56-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29b56-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29b56-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="29b56-114">-MatchValue</span></span>
<span data-ttu-id="29b56-115">"Совпадение".</span><span class="sxs-lookup"><span data-stu-id="29b56-115">Match value.</span></span>

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

### <span data-ttu-id="29b56-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="29b56-116">-MatchVariable</span></span>
<span data-ttu-id="29b56-117">Список переменных совпадения.</span><span class="sxs-lookup"><span data-stu-id="29b56-117">List of match variables.</span></span>

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

### <span data-ttu-id="29b56-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="29b56-118">-NegationCondition</span></span>
<span data-ttu-id="29b56-119">В этой статье описывается, является ли это условием negate.</span><span class="sxs-lookup"><span data-stu-id="29b56-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="29b56-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="29b56-120">-Operator</span></span>
<span data-ttu-id="29b56-121">Оператор для совпадения.</span><span class="sxs-lookup"><span data-stu-id="29b56-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="29b56-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="29b56-122">-Transform</span></span>
<span data-ttu-id="29b56-123">Список преобразований.</span><span class="sxs-lookup"><span data-stu-id="29b56-123">List of transforms.</span></span>

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

### <span data-ttu-id="29b56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b56-124">CommonParameters</span></span>
<span data-ttu-id="29b56-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29b56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b56-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b56-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b56-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29b56-127">INPUTS</span></span>

### <span data-ttu-id="29b56-128">Нет</span><span class="sxs-lookup"><span data-stu-id="29b56-128">None</span></span>

## <span data-ttu-id="29b56-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29b56-129">OUTPUTS</span></span>

### <span data-ttu-id="29b56-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="29b56-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="29b56-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="29b56-131">NOTES</span></span>

## <span data-ttu-id="29b56-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29b56-132">RELATED LINKS</span></span>
