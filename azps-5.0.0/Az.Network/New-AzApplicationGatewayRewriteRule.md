---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318029"
---
# <span data-ttu-id="f3118-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f3118-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="f3118-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3118-102">SYNOPSIS</span></span>
<span data-ttu-id="f3118-103">Создание правила перезаписи для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f3118-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="f3118-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3118-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3118-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3118-105">DESCRIPTION</span></span>
<span data-ttu-id="f3118-106">Командлет **New-AzApplicationGatewayRewriteRule** создает правило повторной записи для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="f3118-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="f3118-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3118-107">EXAMPLES</span></span>

### <span data-ttu-id="f3118-108">Пример 1: Создание правила повторной записи для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="f3118-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="f3118-109">Эта команда создает правило перезаписи с именем rule1 и сохраняет результат в переменной с именем $rule.</span><span class="sxs-lookup"><span data-stu-id="f3118-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="f3118-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3118-110">PARAMETERS</span></span>

### <span data-ttu-id="f3118-111">-В качестве действия</span><span class="sxs-lookup"><span data-stu-id="f3118-111">-ActionSet</span></span>
<span data-ttu-id="f3118-112">Набор макрокоманд для правила перезаписи</span><span class="sxs-lookup"><span data-stu-id="f3118-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="f3118-113">-Условие</span><span class="sxs-lookup"><span data-stu-id="f3118-113">-Condition</span></span>
<span data-ttu-id="f3118-114">Условие для правила перезаписи для выполнения</span><span class="sxs-lookup"><span data-stu-id="f3118-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="f3118-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3118-115">-DefaultProfile</span></span>
<span data-ttu-id="f3118-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3118-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3118-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3118-117">-Name</span></span>
<span data-ttu-id="f3118-118">Имя RewriteRule</span><span class="sxs-lookup"><span data-stu-id="f3118-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="f3118-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="f3118-119">-RuleSequence</span></span>
<span data-ttu-id="f3118-120">Порядок правил для этого правила перезаписи в наборе правил перезаписи</span><span class="sxs-lookup"><span data-stu-id="f3118-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="f3118-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3118-121">CommonParameters</span></span>
<span data-ttu-id="f3118-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3118-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3118-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3118-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3118-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3118-124">INPUTS</span></span>

### <span data-ttu-id="f3118-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="f3118-125">None</span></span>

## <span data-ttu-id="f3118-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3118-126">OUTPUTS</span></span>

### <span data-ttu-id="f3118-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="f3118-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="f3118-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3118-128">NOTES</span></span>

## <span data-ttu-id="f3118-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3118-129">RELATED LINKS</span></span>

[<span data-ttu-id="f3118-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3118-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f3118-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3118-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f3118-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3118-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f3118-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3118-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f3118-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3118-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="f3118-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="f3118-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="f3118-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3118-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
