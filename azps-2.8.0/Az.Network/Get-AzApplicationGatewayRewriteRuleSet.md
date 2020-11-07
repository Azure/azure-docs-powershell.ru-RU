---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrewriteruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRewriteRuleSet.md
ms.openlocfilehash: 35338b5fa179e916bfb52f2529a12d5be1665e89
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902497"
---
# <span data-ttu-id="de697-101">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="de697-101">Get-AzApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="de697-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de697-102">SYNOPSIS</span></span>
<span data-ttu-id="de697-103">Возвращает набор правил перезаписи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="de697-103">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="de697-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de697-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRewriteRuleSet [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de697-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de697-105">DESCRIPTION</span></span>
<span data-ttu-id="de697-106">Возвращает набор правил перезаписи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="de697-106">Gets the rewrite rule set of an application gateway.</span></span>

## <span data-ttu-id="de697-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de697-107">EXAMPLES</span></span>

### <span data-ttu-id="de697-108">Пример 1: получение определенного набор правил для перезаписи</span><span class="sxs-lookup"><span data-stu-id="de697-108">Example 1 : Get a specific rewrite rule set</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRewriteRuleSet -Name "RuleSet01" -ApplicationGateway $AppGW
```

<span data-ttu-id="de697-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="de697-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="de697-110">Вторая команда получает наборы правил перезаписи с именем RuleSet01 из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="de697-110">The second command gets the rewrite rule set named RuleSet01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="de697-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de697-111">PARAMETERS</span></span>

### <span data-ttu-id="de697-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de697-112">-ApplicationGateway</span></span>
<span data-ttu-id="de697-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de697-113">The applicationGateway</span></span>

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

### <span data-ttu-id="de697-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de697-114">-DefaultProfile</span></span>
<span data-ttu-id="de697-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de697-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de697-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="de697-116">-Name</span></span>
<span data-ttu-id="de697-117">Имя RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="de697-117">The name of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="de697-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de697-118">CommonParameters</span></span>
<span data-ttu-id="de697-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de697-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de697-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de697-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de697-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de697-121">INPUTS</span></span>

### <span data-ttu-id="de697-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de697-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="de697-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de697-123">OUTPUTS</span></span>

### <span data-ttu-id="de697-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="de697-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet</span></span>

## <span data-ttu-id="de697-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="de697-125">NOTES</span></span>

## <span data-ttu-id="de697-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de697-126">RELATED LINKS</span></span>

[<span data-ttu-id="de697-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="de697-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="de697-128">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="de697-128">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="de697-129">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="de697-129">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="de697-130">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="de697-130">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="de697-131">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="de697-131">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="de697-132">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="de697-132">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="de697-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="de697-133">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
