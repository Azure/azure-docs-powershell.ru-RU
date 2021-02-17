---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 01f1dc89257088c053cdd6003384c31c708d6b04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236625"
---
# <span data-ttu-id="3d0cd-101">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d0cd-101">Remove-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="3d0cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="3d0cd-103">Удаляет набор правил переописи из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3d0cd-103">Removes a rewrite rule set from an application gateway.</span></span>

## <span data-ttu-id="3d0cd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3d0cd-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRewriteRuleSet -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d0cd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d0cd-105">DESCRIPTION</span></span>
<span data-ttu-id="3d0cd-106">Для удаления набора правил перезаписи из шлюза приложения Azure удаляется набор правил **Remove-AzApplicationGatewayRewriteRuleSet.**</span><span class="sxs-lookup"><span data-stu-id="3d0cd-106">The **Remove-AzApplicationGatewayRewriteRuleSet** cmdlet removes a rewrite rule set from an Azure application gateway.</span></span>

## <span data-ttu-id="3d0cd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3d0cd-107">EXAMPLES</span></span>

### <span data-ttu-id="3d0cd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d0cd-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "RuleSet02"
```

<span data-ttu-id="3d0cd-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3d0cd-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3d0cd-110">Вторая команда удаляет набор правил переописи с именем RuleSet02 из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3d0cd-110">The second command removes the rewrite rule set named RuleSet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3d0cd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d0cd-111">PARAMETERS</span></span>

### <span data-ttu-id="3d0cd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d0cd-112">-ApplicationGateway</span></span>
<span data-ttu-id="3d0cd-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d0cd-113">The applicationGateway</span></span>

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

### <span data-ttu-id="3d0cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d0cd-114">-DefaultProfile</span></span>
<span data-ttu-id="3d0cd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d0cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d0cd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3d0cd-116">-Name</span></span>
<span data-ttu-id="3d0cd-117">Имя шлюза приложения RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d0cd-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="3d0cd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d0cd-118">CommonParameters</span></span>
<span data-ttu-id="3d0cd-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d0cd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d0cd-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d0cd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d0cd-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d0cd-121">INPUTS</span></span>

### <span data-ttu-id="3d0cd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d0cd-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d0cd-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d0cd-123">OUTPUTS</span></span>

### <span data-ttu-id="3d0cd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d0cd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d0cd-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3d0cd-125">NOTES</span></span>

## <span data-ttu-id="3d0cd-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d0cd-126">RELATED LINKS</span></span>

[<span data-ttu-id="3d0cd-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d0cd-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3d0cd-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d0cd-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3d0cd-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d0cd-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3d0cd-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3d0cd-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3d0cd-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3d0cd-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="3d0cd-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3d0cd-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="3d0cd-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d0cd-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
