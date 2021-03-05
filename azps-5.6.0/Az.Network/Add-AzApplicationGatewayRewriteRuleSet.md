---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: d657c769a32d7c042a12a56571343885c526eea7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982499"
---
# <span data-ttu-id="421d8-101">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="421d8-101">Add-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="421d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="421d8-102">SYNOPSIS</span></span>
<span data-ttu-id="421d8-103">Добавляет набор правил переписыванием в шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="421d8-103">Adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="421d8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="421d8-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="421d8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="421d8-105">DESCRIPTION</span></span>
<span data-ttu-id="421d8-106">Для шлюза приложения добавляется набор правил переописи **Add-AzApplicationGatewayRewriteRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="421d8-106">The **Add-AzApplicationGatewayRewriteRuleSet** cmdlet adds a rewrite rule set to an application gateway.</span></span>

## <span data-ttu-id="421d8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="421d8-107">EXAMPLES</span></span>

### <span data-ttu-id="421d8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="421d8-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="421d8-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="421d8-109">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="421d8-110">Вторая команда добавляет набор правил переописи на шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="421d8-110">The second command adds the rewrite rule set to the application gateway.</span></span>

## <span data-ttu-id="421d8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="421d8-111">PARAMETERS</span></span>

### <span data-ttu-id="421d8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="421d8-112">-ApplicationGateway</span></span>
<span data-ttu-id="421d8-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="421d8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="421d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="421d8-114">-DefaultProfile</span></span>
<span data-ttu-id="421d8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="421d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="421d8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="421d8-116">-Name</span></span>
<span data-ttu-id="421d8-117">Имя rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="421d8-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="421d8-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="421d8-118">-RewriteRule</span></span>
<span data-ttu-id="421d8-119">Список правил переписываний</span><span class="sxs-lookup"><span data-stu-id="421d8-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="421d8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="421d8-120">CommonParameters</span></span>
<span data-ttu-id="421d8-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="421d8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="421d8-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="421d8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="421d8-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="421d8-123">INPUTS</span></span>

### <span data-ttu-id="421d8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="421d8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="421d8-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="421d8-125">OUTPUTS</span></span>

### <span data-ttu-id="421d8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="421d8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="421d8-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="421d8-127">NOTES</span></span>

## <span data-ttu-id="421d8-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="421d8-128">RELATED LINKS</span></span>

[<span data-ttu-id="421d8-129">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="421d8-129">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="421d8-130">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="421d8-130">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="421d8-131">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="421d8-131">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="421d8-132">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="421d8-132">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="421d8-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="421d8-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="421d8-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="421d8-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="421d8-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="421d8-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
