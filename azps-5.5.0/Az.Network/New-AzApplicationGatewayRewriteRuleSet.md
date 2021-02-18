---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: b2fc00bf62b1ed147e1c7c32aa30731222a28bea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240880"
---
# <span data-ttu-id="f5b47-101">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5b47-101">New-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="f5b47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5b47-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b47-103">Создает правило маршрутки запросов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f5b47-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="f5b47-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5b47-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleSet -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5b47-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5b47-105">DESCRIPTION</span></span>
<span data-ttu-id="f5b47-106">Для шлюза приложения Azure создается набор правил переописи для нового **azApplicationGatewayRewriteRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="f5b47-106">**The New-AzApplicationGatewayRewriteRuleSet** cmdlet creates a rewrite rule set for an Azure application gateway.</span></span>

## <span data-ttu-id="f5b47-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5b47-107">EXAMPLES</span></span>

### <span data-ttu-id="f5b47-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5b47-108">Example 1</span></span>
```powershell
PS C:\> $ruleset = New-AzApplicationGatewayRewriteRuleSet -Name ruleset1 -RewriteRule $rule
```

<span data-ttu-id="f5b47-109">Эта команда создает набор правил переописи с именем ruleset1 и сохраняет результат в переменной с $ruleset.</span><span class="sxs-lookup"><span data-stu-id="f5b47-109">This command creates a rewrite rule set named ruleset1 and stores the result in the variable named $ruleset.</span></span>

## <span data-ttu-id="f5b47-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5b47-110">PARAMETERS</span></span>

### <span data-ttu-id="f5b47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b47-111">-DefaultProfile</span></span>
<span data-ttu-id="f5b47-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5b47-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5b47-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f5b47-113">-Name</span></span>
<span data-ttu-id="f5b47-114">Имя rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5b47-114">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="f5b47-115">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="f5b47-115">-RewriteRule</span></span>
<span data-ttu-id="f5b47-116">Список правил переписываний</span><span class="sxs-lookup"><span data-stu-id="f5b47-116">List of rewrite rules</span></span>

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

### <span data-ttu-id="f5b47-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b47-117">CommonParameters</span></span>
<span data-ttu-id="f5b47-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5b47-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b47-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b47-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b47-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5b47-120">INPUTS</span></span>

### <span data-ttu-id="f5b47-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f5b47-121">None</span></span>

## <span data-ttu-id="f5b47-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5b47-122">OUTPUTS</span></span>

### <span data-ttu-id="f5b47-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5b47-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="f5b47-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5b47-124">NOTES</span></span>

## <span data-ttu-id="f5b47-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5b47-125">RELATED LINKS</span></span>

[<span data-ttu-id="f5b47-126">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5b47-126">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f5b47-127">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5b47-127">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f5b47-128">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5b47-128">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f5b47-129">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f5b47-129">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f5b47-130">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f5b47-130">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="f5b47-131">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f5b47-131">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="f5b47-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5b47-132">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
