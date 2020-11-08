---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079478"
---
# <span data-ttu-id="7f2d0-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7f2d0-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="7f2d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2d0-103">Создание правила перезаписи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="7f2d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f2d0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f2d0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f2d0-105">DESCRIPTION</span></span>
<span data-ttu-id="7f2d0-106">Командлет **New-AzApplicationGatewayRewriteRule** создает правило повторной записи для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="7f2d0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f2d0-107">EXAMPLES</span></span>

### <span data-ttu-id="7f2d0-108">Пример 1: Создание правила повторной записи для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="7f2d0-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="7f2d0-109">Эта команда создает правило перезаписи с именем rule1 и сохраняет результат в переменной с именем $rule.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="7f2d0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f2d0-110">PARAMETERS</span></span>

### <span data-ttu-id="7f2d0-111">-В качестве действия</span><span class="sxs-lookup"><span data-stu-id="7f2d0-111">-ActionSet</span></span>
<span data-ttu-id="7f2d0-112">Набор макрокоманд для правила перезаписи</span><span class="sxs-lookup"><span data-stu-id="7f2d0-112">ActionSet of the rewrite rule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleActionSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2d0-113">-Условие</span><span class="sxs-lookup"><span data-stu-id="7f2d0-113">-Condition</span></span>
<span data-ttu-id="7f2d0-114">Условие для правила перезаписи для выполнения</span><span class="sxs-lookup"><span data-stu-id="7f2d0-114">Condition for the rewrite rule to execute</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2d0-115">-DefaultProfile</span></span>
<span data-ttu-id="7f2d0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f2d0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f2d0-117">-Name</span></span>
<span data-ttu-id="7f2d0-118">Имя RewriteRule</span><span class="sxs-lookup"><span data-stu-id="7f2d0-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="7f2d0-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="7f2d0-119">-RuleSequence</span></span>
<span data-ttu-id="7f2d0-120">Порядок правил для этого правила перезаписи в наборе правил перезаписи</span><span class="sxs-lookup"><span data-stu-id="7f2d0-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2d0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2d0-121">CommonParameters</span></span>
<span data-ttu-id="7f2d0-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f2d0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2d0-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f2d0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2d0-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f2d0-124">INPUTS</span></span>

### <span data-ttu-id="7f2d0-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="7f2d0-125">None</span></span>

## <span data-ttu-id="7f2d0-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f2d0-126">OUTPUTS</span></span>

### <span data-ttu-id="7f2d0-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7f2d0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="7f2d0-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f2d0-128">NOTES</span></span>

## <span data-ttu-id="7f2d0-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f2d0-129">RELATED LINKS</span></span>

[<span data-ttu-id="7f2d0-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f2d0-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f2d0-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f2d0-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f2d0-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f2d0-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f2d0-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f2d0-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f2d0-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7f2d0-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="7f2d0-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7f2d0-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="7f2d0-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f2d0-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
