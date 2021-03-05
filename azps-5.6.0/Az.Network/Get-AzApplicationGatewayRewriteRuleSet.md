---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 935e2df3de68d9ab8444cd1037d5c48951d6a335
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994073"
---
# <span data-ttu-id="0e61d-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e61d-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="0e61d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e61d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e61d-103">Возвращает набор правил переписыванием шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0e61d-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="0e61d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0e61d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e61d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e61d-105">DESCRIPTION</span></span>
<span data-ttu-id="0e61d-106">Возвращает набор правил переписыванием шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0e61d-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="0e61d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0e61d-107">EXAMPLES</span></span>

### <span data-ttu-id="0e61d-108">Пример 1. Получить набор правил для переописи</span><span class="sxs-lookup"><span data-stu-id="0e61d-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="0e61d-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0e61d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="0e61d-110">Вторая команда получает набор правил переписыванием с именем RuleSet01 из шлюза приложения, храняного в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="0e61d-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="0e61d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e61d-111">PARAMETERS</span></span>

### <span data-ttu-id="0e61d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e61d-112">-ApplicationGateway</span></span>
<span data-ttu-id="0e61d-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e61d-113">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e61d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e61d-114">-DefaultProfile</span></span>
<span data-ttu-id="0e61d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e61d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e61d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0e61d-116">-Name</span></span>
<span data-ttu-id="0e61d-117">Имя шлюза приложения RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e61d-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0e61d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e61d-118">CommonParameters</span></span>
<span data-ttu-id="0e61d-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e61d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e61d-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e61d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e61d-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e61d-121">INPUTS</span></span>

### <span data-ttu-id="0e61d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e61d-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e61d-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e61d-123">OUTPUTS</span></span>

### <span data-ttu-id="0e61d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e61d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="0e61d-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0e61d-125">NOTES</span></span>

## <span data-ttu-id="0e61d-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e61d-126">RELATED LINKS</span></span>

[<span data-ttu-id="0e61d-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e61d-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0e61d-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e61d-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0e61d-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e61d-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0e61d-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e61d-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="0e61d-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0e61d-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="0e61d-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0e61d-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="0e61d-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e61d-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
