---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 934c69071e90ebb1a38bf4e1fda5e631364ab87b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003464"
---
# <span data-ttu-id="8714e-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8714e-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="8714e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8714e-102">SYNOPSIS</span></span>
<span data-ttu-id="8714e-103">Изменяет набор правил переписыванием для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8714e-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="8714e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8714e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8714e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8714e-105">DESCRIPTION</span></span>
<span data-ttu-id="8714e-106">**Cmdlet Set-AzApplicationGatewayRewriteRuleSet** изменяет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="8714e-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="8714e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8714e-107">EXAMPLES</span></span>

### <span data-ttu-id="8714e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8714e-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="8714e-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8714e-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8714e-110">Вторая команда изменяет правило переописи, заданное шлюзом приложения, для использования правил переописи, указанных в $rule переменной.</span><span class="sxs-lookup"><span data-stu-id="8714e-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="8714e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8714e-111">PARAMETERS</span></span>

### <span data-ttu-id="8714e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8714e-112">-ApplicationGateway</span></span>
<span data-ttu-id="8714e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8714e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8714e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8714e-114">-DefaultProfile</span></span>
<span data-ttu-id="8714e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8714e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8714e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8714e-116">-Name</span></span>
<span data-ttu-id="8714e-117">Имя rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8714e-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="8714e-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="8714e-118">-RewriteRule</span></span>
<span data-ttu-id="8714e-119">Список правил переписываний</span><span class="sxs-lookup"><span data-stu-id="8714e-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="8714e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8714e-120">CommonParameters</span></span>
<span data-ttu-id="8714e-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8714e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8714e-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8714e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8714e-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8714e-123">INPUTS</span></span>

### <span data-ttu-id="8714e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8714e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8714e-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8714e-125">OUTPUTS</span></span>

### <span data-ttu-id="8714e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8714e-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8714e-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8714e-127">NOTES</span></span>

## <span data-ttu-id="8714e-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8714e-128">RELATED LINKS</span></span>

[<span data-ttu-id="8714e-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8714e-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8714e-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8714e-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8714e-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8714e-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8714e-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8714e-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="8714e-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="8714e-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="8714e-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="8714e-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="8714e-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="8714e-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
