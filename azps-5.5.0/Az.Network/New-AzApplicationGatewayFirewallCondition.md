---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallCondition.md
ms.openlocfilehash: 64157cd137e9f3b784404dccee6513b6fe023d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213865"
---
# <span data-ttu-id="ef557-101">New-AzApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="ef557-101">New-AzApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="ef557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef557-102">SYNOPSIS</span></span>
<span data-ttu-id="ef557-103">Создание условия для пользовательского правила</span><span class="sxs-lookup"><span data-stu-id="ef557-103">Creates a match condition for custom rule</span></span>

## <span data-ttu-id="ef557-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef557-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallCondition -MatchVariable <PSApplicationGatewayFirewallMatchVariable[]>
 -Operator <String> [-NegationCondition <Boolean>] -MatchValue <String[]> [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef557-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef557-105">DESCRIPTION</span></span>
<span data-ttu-id="ef557-106">**New-AzApplicationGatewayFirewallCondition** создает условие совпадения для настраиваемого правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ef557-106">The **New-AzApplicationGatewayFirewallCondition** creates a match condition for firewall custom rule.</span></span>

## <span data-ttu-id="ef557-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef557-107">EXAMPLES</span></span>

### <span data-ttu-id="ef557-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef557-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallCondition -MatchVariable $variable -Operator Contains -NegationCondition false -Transforms Lowercase, Trim -MatchValue abc, cde
```

<span data-ttu-id="ef557-109">Команда создает новое условие совпадения с использованием переменной совпадения, определенной в $variable, оператором является "Содержит" и условие отрицания — false, Transfroms (нижний регистр и усеченный регистр), значение совпадения — abc и cde.</span><span class="sxs-lookup"><span data-stu-id="ef557-109">The command creates a new match condition using the match variable defined in the $variable, the operator is Contains and negation condition is false, Transfroms including lowercase and trim, the match value is abc and cde.</span></span> <span data-ttu-id="ef557-110">Новое условие совпадения будет сохранено в $condition.</span><span class="sxs-lookup"><span data-stu-id="ef557-110">The new match condition is saved in $condition.</span></span>

## <span data-ttu-id="ef557-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef557-111">PARAMETERS</span></span>

### <span data-ttu-id="ef557-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef557-112">-DefaultProfile</span></span>
<span data-ttu-id="ef557-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef557-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef557-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="ef557-114">-MatchValue</span></span>
<span data-ttu-id="ef557-115">Совпадает со значением.</span><span class="sxs-lookup"><span data-stu-id="ef557-115">Match value.</span></span>

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

### <span data-ttu-id="ef557-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="ef557-116">-MatchVariable</span></span>
<span data-ttu-id="ef557-117">Список переменных совпадения.</span><span class="sxs-lookup"><span data-stu-id="ef557-117">List of match variables.</span></span>

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

### <span data-ttu-id="ef557-118">-NegationCondition</span><span class="sxs-lookup"><span data-stu-id="ef557-118">-NegationCondition</span></span>
<span data-ttu-id="ef557-119">В этой статье описывается, является ли это условием negate.</span><span class="sxs-lookup"><span data-stu-id="ef557-119">Describes if this is negate condition or not.</span></span>

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

### <span data-ttu-id="ef557-120">-Operator</span><span class="sxs-lookup"><span data-stu-id="ef557-120">-Operator</span></span>
<span data-ttu-id="ef557-121">Оператор для совпадения.</span><span class="sxs-lookup"><span data-stu-id="ef557-121">Describes operator to be matched.</span></span>

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

### <span data-ttu-id="ef557-122">-Transform</span><span class="sxs-lookup"><span data-stu-id="ef557-122">-Transform</span></span>
<span data-ttu-id="ef557-123">Список преобразований.</span><span class="sxs-lookup"><span data-stu-id="ef557-123">List of transforms.</span></span>

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

### <span data-ttu-id="ef557-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef557-124">CommonParameters</span></span>
<span data-ttu-id="ef557-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef557-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef557-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef557-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef557-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef557-127">INPUTS</span></span>

### <span data-ttu-id="ef557-128">Нет</span><span class="sxs-lookup"><span data-stu-id="ef557-128">None</span></span>

## <span data-ttu-id="ef557-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef557-129">OUTPUTS</span></span>

### <span data-ttu-id="ef557-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span><span class="sxs-lookup"><span data-stu-id="ef557-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCondition</span></span>

## <span data-ttu-id="ef557-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef557-131">NOTES</span></span>

## <span data-ttu-id="ef557-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef557-132">RELATED LINKS</span></span>
