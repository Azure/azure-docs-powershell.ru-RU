---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 45d7fdf6a276e98ce0aca2c2a0db6989e062e42c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074737"
---
# <span data-ttu-id="57849-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57849-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="57849-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57849-102">SYNOPSIS</span></span>
<span data-ttu-id="57849-103">Изменяет набор правил перезаписи для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="57849-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="57849-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57849-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57849-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57849-105">DESCRIPTION</span></span>
<span data-ttu-id="57849-106">Командлет **Set-AzApplicationGatewayRewriteRuleSet** изменяет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="57849-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="57849-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57849-107">EXAMPLES</span></span>

### <span data-ttu-id="57849-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57849-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="57849-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="57849-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="57849-110">Вторая команда изменяет параметр правила перезаписи для шлюза приложения, чтобы использовать правила повторной записи, указанные в переменной $rule.</span><span class="sxs-lookup"><span data-stu-id="57849-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="57849-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57849-111">PARAMETERS</span></span>

### <span data-ttu-id="57849-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57849-112">-ApplicationGateway</span></span>
<span data-ttu-id="57849-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57849-113">The applicationGateway</span></span>

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

### <span data-ttu-id="57849-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57849-114">-DefaultProfile</span></span>
<span data-ttu-id="57849-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57849-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57849-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="57849-116">-Name</span></span>
<span data-ttu-id="57849-117">Имя RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57849-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="57849-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="57849-118">-RewriteRule</span></span>
<span data-ttu-id="57849-119">Список правил для перезаписи</span><span class="sxs-lookup"><span data-stu-id="57849-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="57849-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57849-120">CommonParameters</span></span>
<span data-ttu-id="57849-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57849-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57849-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57849-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57849-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57849-123">INPUTS</span></span>

### <span data-ttu-id="57849-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57849-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57849-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57849-125">OUTPUTS</span></span>

### <span data-ttu-id="57849-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57849-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57849-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="57849-127">NOTES</span></span>

## <span data-ttu-id="57849-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57849-128">RELATED LINKS</span></span>

[<span data-ttu-id="57849-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57849-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="57849-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57849-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="57849-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57849-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="57849-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="57849-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="57849-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="57849-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="57849-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="57849-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="57849-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="57849-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
