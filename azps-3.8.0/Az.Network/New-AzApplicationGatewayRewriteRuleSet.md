---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074774"
---
# <span data-ttu-id="e0594-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0594-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="e0594-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0594-102">SYNOPSIS</span></span>
<span data-ttu-id="e0594-103">Создание правила маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e0594-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="e0594-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0594-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0594-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0594-105">DESCRIPTION</span></span>
<span data-ttu-id="e0594-106">Командлет **New-AzApplicationGatewayRewriteRuleSet** создает набор правил перезаписи для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="e0594-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="e0594-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0594-107">EXAMPLES</span></span>

### <span data-ttu-id="e0594-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0594-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="e0594-109">Эта команда создает набор правил перезаписи с именем ruleset1 и сохраняет результат в переменной с именем $ruleset.</span><span class="sxs-lookup"><span data-stu-id="e0594-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="e0594-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0594-110">PARAMETERS</span></span>

### <span data-ttu-id="e0594-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0594-111">-DefaultProfile</span></span>
<span data-ttu-id="e0594-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0594-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0594-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0594-113">-Name</span></span>
<span data-ttu-id="e0594-114">Имя RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0594-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="e0594-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="e0594-115">-RewriteRule</span></span>
<span data-ttu-id="e0594-116">Список правил для перезаписи</span><span class="sxs-lookup"><span data-stu-id="e0594-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="e0594-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0594-117">CommonParameters</span></span>
<span data-ttu-id="e0594-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0594-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0594-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0594-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0594-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0594-120">INPUTS</span></span>

### <span data-ttu-id="e0594-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="e0594-121">None</span></span>

## <span data-ttu-id="e0594-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0594-122">OUTPUTS</span></span>

### <span data-ttu-id="e0594-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0594-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="e0594-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0594-124">NOTES</span></span>

## <span data-ttu-id="e0594-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0594-125">RELATED LINKS</span></span>

[<span data-ttu-id="e0594-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0594-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e0594-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0594-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e0594-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0594-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e0594-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e0594-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="e0594-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e0594-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="e0594-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e0594-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="e0594-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0594-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
