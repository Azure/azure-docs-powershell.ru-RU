---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518041"
---
# <span data-ttu-id="01b21-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01b21-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="01b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b21-102">SYNOPSIS</span></span>
<span data-ttu-id="01b21-103">Изменяет набор правил переописи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="01b21-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="01b21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01b21-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01b21-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01b21-105">DESCRIPTION</span></span>
<span data-ttu-id="01b21-106">**Cmdlet Set-AzApplicationGatewayRewriteRuleSet** изменяет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="01b21-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="01b21-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01b21-107">EXAMPLES</span></span>

### <span data-ttu-id="01b21-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01b21-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="01b21-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="01b21-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="01b21-110">Вторая команда изменяет правило переописи, заданное шлюзом приложения, для использования правил переописи, указанных в переменной $rule.</span><span class="sxs-lookup"><span data-stu-id="01b21-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="01b21-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01b21-111">PARAMETERS</span></span>

### <span data-ttu-id="01b21-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01b21-112">-ApplicationGateway</span></span>
<span data-ttu-id="01b21-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01b21-113">The applicationGateway</span></span>

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

### <span data-ttu-id="01b21-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b21-114">-DefaultProfile</span></span>
<span data-ttu-id="01b21-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01b21-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01b21-116">-Name</span><span class="sxs-lookup"><span data-stu-id="01b21-116">-Name</span></span>
<span data-ttu-id="01b21-117">Имя rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01b21-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="01b21-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="01b21-118">-RewriteRule</span></span>
<span data-ttu-id="01b21-119">Список правил переписываний</span><span class="sxs-lookup"><span data-stu-id="01b21-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="01b21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b21-120">CommonParameters</span></span>
<span data-ttu-id="01b21-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b21-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01b21-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b21-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01b21-123">INPUTS</span></span>

### <span data-ttu-id="01b21-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01b21-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="01b21-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01b21-125">OUTPUTS</span></span>

### <span data-ttu-id="01b21-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01b21-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="01b21-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01b21-127">NOTES</span></span>

## <span data-ttu-id="01b21-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01b21-128">RELATED LINKS</span></span>

[<span data-ttu-id="01b21-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01b21-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="01b21-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01b21-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="01b21-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01b21-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="01b21-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="01b21-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="01b21-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="01b21-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="01b21-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="01b21-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="01b21-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="01b21-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
