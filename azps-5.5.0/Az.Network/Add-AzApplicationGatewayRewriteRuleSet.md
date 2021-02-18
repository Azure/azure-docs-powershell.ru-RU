---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241120"
---
# <span data-ttu-id="e8c96-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8c96-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="e8c96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8c96-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c96-103">Добавляет набор правил переписыванием в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="e8c96-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="e8c96-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e8c96-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8c96-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8c96-105">DESCRIPTION</span></span>
<span data-ttu-id="e8c96-106">Для шлюза приложения добавляется набор правил переописи **Add-AzApplicationGatewayRewriteRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="e8c96-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="e8c96-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e8c96-107">EXAMPLES</span></span>

### <span data-ttu-id="e8c96-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8c96-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="e8c96-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e8c96-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e8c96-110">Вторая команда добавляет набор правил переописи на шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="e8c96-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="e8c96-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8c96-111">PARAMETERS</span></span>

### <span data-ttu-id="e8c96-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8c96-112">-ApplicationGateway</span></span>
<span data-ttu-id="e8c96-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8c96-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e8c96-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c96-114">-DefaultProfile</span></span>
<span data-ttu-id="e8c96-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8c96-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8c96-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e8c96-116">-Name</span></span>
<span data-ttu-id="e8c96-117">Имя rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8c96-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="e8c96-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="e8c96-118">-RewriteRule</span></span>
<span data-ttu-id="e8c96-119">Список правил переписываний</span><span class="sxs-lookup"><span data-stu-id="e8c96-119">List of rewrite rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8c96-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c96-120">CommonParameters</span></span>
<span data-ttu-id="e8c96-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8c96-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c96-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8c96-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c96-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8c96-123">INPUTS</span></span>

### <span data-ttu-id="e8c96-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8c96-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8c96-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8c96-125">OUTPUTS</span></span>

### <span data-ttu-id="e8c96-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8c96-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8c96-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e8c96-127">NOTES</span></span>

## <span data-ttu-id="e8c96-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8c96-128">RELATED LINKS</span></span>

[<span data-ttu-id="e8c96-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8c96-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e8c96-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8c96-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e8c96-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8c96-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e8c96-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e8c96-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e8c96-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e8c96-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="e8c96-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e8c96-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="e8c96-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8c96-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
