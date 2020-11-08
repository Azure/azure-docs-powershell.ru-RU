---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 6e45f0bc0eaab8316d0534e1f73a1543175e1144
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073786"
---
# <span data-ttu-id="3d570-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d570-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="3d570-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d570-102">SYNOPSIS</span></span>
<span data-ttu-id="3d570-103">Добавляет правило перезаписи, установленное для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3d570-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="3d570-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d570-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d570-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d570-105">DESCRIPTION</span></span>
<span data-ttu-id="3d570-106">Командлет **Add-AzApplicationGatewayRewriteRuleSet** добавляет правило перезаписи, установленное для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3d570-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="3d570-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d570-107">EXAMPLES</span></span>

### <span data-ttu-id="3d570-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d570-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="3d570-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3d570-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3d570-110">Вторая команда добавляет правило перезаписи, установленное для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3d570-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="3d570-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d570-111">PARAMETERS</span></span>

### <span data-ttu-id="3d570-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d570-112">-ApplicationGateway</span></span>
<span data-ttu-id="3d570-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d570-113">The applicationGateway</span></span>

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

### <span data-ttu-id="3d570-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d570-114">-DefaultProfile</span></span>
<span data-ttu-id="3d570-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d570-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d570-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d570-116">-Name</span></span>
<span data-ttu-id="3d570-117">Имя RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d570-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="3d570-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="3d570-118">-RewriteRule</span></span>
<span data-ttu-id="3d570-119">Список правил для перезаписи</span><span class="sxs-lookup"><span data-stu-id="3d570-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="3d570-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d570-120">CommonParameters</span></span>
<span data-ttu-id="3d570-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d570-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d570-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d570-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d570-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d570-123">INPUTS</span></span>

### <span data-ttu-id="3d570-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d570-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d570-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d570-125">OUTPUTS</span></span>

### <span data-ttu-id="3d570-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d570-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d570-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d570-127">NOTES</span></span>

## <span data-ttu-id="3d570-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d570-128">RELATED LINKS</span></span>

[<span data-ttu-id="3d570-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d570-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3d570-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d570-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3d570-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d570-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3d570-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d570-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3d570-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3d570-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="3d570-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3d570-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="3d570-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d570-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
