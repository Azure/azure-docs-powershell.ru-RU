---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 3587005559849072d973242eb6af221c0b8b0557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730040"
---
# <span data-ttu-id="f639f-101">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f639f-101">Set-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="f639f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f639f-102">SYNOPSIS</span></span>
<span data-ttu-id="f639f-103">Изменяет набор правил перезаписи для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f639f-103">Modifies a rewrite rule set for an application gateway.</span></span>

## <span data-ttu-id="f639f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f639f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RewriteRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f639f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f639f-105">DESCRIPTION</span></span>
<span data-ttu-id="f639f-106">Командлет **Set-AzApplicationGatewayRewriteRuleSet** изменяет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="f639f-106">The **Set-AzApplicationGatewayRewriteRuleSet** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="f639f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f639f-107">EXAMPLES</span></span>

### <span data-ttu-id="f639f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f639f-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRewriteRuleSet -ApplicationGateway $AppGw -Name "ruleset1" -RewriteRule $rule
```

<span data-ttu-id="f639f-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f639f-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f639f-110">Вторая команда изменяет параметр правила перезаписи для шлюза приложения, чтобы использовать правила повторной записи, указанные в переменной $rule.</span><span class="sxs-lookup"><span data-stu-id="f639f-110">The second command modifies the rewrite rule set for the application gateway to use rewrite rules specified in the $rule variable.</span></span>

## <span data-ttu-id="f639f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f639f-111">PARAMETERS</span></span>

### <span data-ttu-id="f639f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f639f-112">-ApplicationGateway</span></span>
<span data-ttu-id="f639f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f639f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f639f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f639f-114">-DefaultProfile</span></span>
<span data-ttu-id="f639f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f639f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f639f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f639f-116">-Name</span></span>
<span data-ttu-id="f639f-117">Имя RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f639f-117">The name of the RewriteRuleSet</span></span>

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

### <span data-ttu-id="f639f-118">-RewriteRule</span><span class="sxs-lookup"><span data-stu-id="f639f-118">-RewriteRule</span></span>
<span data-ttu-id="f639f-119">Список правил для перезаписи</span><span class="sxs-lookup"><span data-stu-id="f639f-119">List of rewrite rules</span></span>

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

### <span data-ttu-id="f639f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f639f-120">CommonParameters</span></span>
<span data-ttu-id="f639f-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f639f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f639f-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f639f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f639f-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f639f-123">INPUTS</span></span>

### <span data-ttu-id="f639f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f639f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f639f-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f639f-125">OUTPUTS</span></span>

### <span data-ttu-id="f639f-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f639f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f639f-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f639f-127">NOTES</span></span>

## <span data-ttu-id="f639f-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f639f-128">RELATED LINKS</span></span>

[<span data-ttu-id="f639f-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f639f-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f639f-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f639f-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f639f-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f639f-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f639f-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f639f-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f639f-133">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f639f-133">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="f639f-134">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f639f-134">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="f639f-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f639f-135">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
