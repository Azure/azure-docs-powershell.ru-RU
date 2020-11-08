---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: dc3019154d4041396d46f3c9f6dbdbdd3deb22a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236965"
---
# <span data-ttu-id="5ede8-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ede8-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="5ede8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ede8-102">SYNOPSIS</span></span>
<span data-ttu-id="5ede8-103">Возвращает набор правил перезаписи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="5ede8-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="5ede8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ede8-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ede8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ede8-105">DESCRIPTION</span></span>
<span data-ttu-id="5ede8-106">Возвращает набор правил перезаписи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="5ede8-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="5ede8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ede8-107">EXAMPLES</span></span>

### <span data-ttu-id="5ede8-108">Пример 1: получение определенного набор правил для перезаписи</span><span class="sxs-lookup"><span data-stu-id="5ede8-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="5ede8-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5ede8-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5ede8-110">Вторая команда получает наборы правил перезаписи с именем RuleSet01 из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5ede8-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="5ede8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ede8-111">PARAMETERS</span></span>

### <span data-ttu-id="5ede8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ede8-112">-ApplicationGateway</span></span>
<span data-ttu-id="5ede8-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ede8-113">The applicationGateway</span></span>

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

### <span data-ttu-id="5ede8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ede8-114">-DefaultProfile</span></span>
<span data-ttu-id="5ede8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ede8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ede8-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5ede8-116">-Name</span></span>
<span data-ttu-id="5ede8-117">Имя RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="5ede8-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="5ede8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ede8-118">CommonParameters</span></span>
<span data-ttu-id="5ede8-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ede8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ede8-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ede8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ede8-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ede8-121">INPUTS</span></span>

### <span data-ttu-id="5ede8-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ede8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ede8-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ede8-123">OUTPUTS</span></span>

### <span data-ttu-id="5ede8-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ede8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="5ede8-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ede8-125">NOTES</span></span>

## <span data-ttu-id="5ede8-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ede8-126">RELATED LINKS</span></span>

[<span data-ttu-id="5ede8-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ede8-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5ede8-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ede8-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5ede8-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ede8-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5ede8-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ede8-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="5ede8-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="5ede8-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="5ede8-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="5ede8-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="5ede8-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ede8-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)