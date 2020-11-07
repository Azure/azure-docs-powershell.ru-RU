---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 7d7403fff78d04153f1c088cbdf41f61677e2e7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730200"
---
# <span data-ttu-id="b1d59-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1d59-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="b1d59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1d59-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d59-103">Удаляет набор правил перезаписи из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b1d59-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="b1d59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1d59-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1d59-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1d59-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d59-106">Командлет **rewrite-AzApplicationGatewayRewriteRuleSet** удаляет набор правил перезаписи из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b1d59-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="b1d59-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1d59-107">EXAMPLES</span></span>

### <span data-ttu-id="b1d59-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1d59-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="b1d59-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b1d59-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b1d59-110">Вторая команда удаляет из шлюза приложений, сохраненного в $AppGw, наборы правил перезаписи с именем RuleSet02.</span><span class="sxs-lookup"><span data-stu-id="b1d59-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b1d59-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1d59-111">PARAMETERS</span></span>

### <span data-ttu-id="b1d59-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1d59-112">-ApplicationGateway</span></span>
<span data-ttu-id="b1d59-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1d59-113">The applicationGateway</span></span>

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

### <span data-ttu-id="b1d59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d59-114">-DefaultProfile</span></span>
<span data-ttu-id="b1d59-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1d59-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1d59-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b1d59-116">-Name</span></span>
<span data-ttu-id="b1d59-117">Имя RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b1d59-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b1d59-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d59-118">CommonParameters</span></span>
<span data-ttu-id="b1d59-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1d59-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d59-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d59-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d59-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1d59-121">INPUTS</span></span>

### <span data-ttu-id="b1d59-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1d59-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1d59-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1d59-123">OUTPUTS</span></span>

### <span data-ttu-id="b1d59-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1d59-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1d59-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1d59-125">NOTES</span></span>

## <span data-ttu-id="b1d59-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1d59-126">RELATED LINKS</span></span>

[<span data-ttu-id="b1d59-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1d59-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b1d59-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1d59-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b1d59-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1d59-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b1d59-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b1d59-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="b1d59-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="b1d59-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="b1d59-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="b1d59-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="b1d59-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="b1d59-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
