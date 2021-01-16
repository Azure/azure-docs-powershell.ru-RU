---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRule.md
ms.openlocfilehash: 5eaa5cdc8b00fa13d9fc0c06821b664f1afc2a65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421847"
---
# <span data-ttu-id="d3053-101">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d3053-101">New-AzApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="d3053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3053-102">SYNOPSIS</span></span>
<span data-ttu-id="d3053-103">Создает правило переписывание для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d3053-103">Creates a rewrite rule for an application gateway.</span></span>

## <span data-ttu-id="d3053-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3053-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRule -Name <String> -ActionSet <PSApplicationGatewayRewriteRuleActionSet>
 [-RuleSequence <Int32>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3053-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3053-105">DESCRIPTION</span></span>
<span data-ttu-id="d3053-106">Для шлюза приложения Azure создается правило переописи для шлюза приложения **New-AzApplicationGatewayRewriteRule.**</span><span class="sxs-lookup"><span data-stu-id="d3053-106">**The New-AzApplicationGatewayRewriteRule** cmdlet creates a rewrite rule for an Azure application gateway.</span></span>

## <span data-ttu-id="d3053-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3053-107">EXAMPLES</span></span>

### <span data-ttu-id="d3053-108">Пример 1. Создание правила переописи шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="d3053-108">Example 1 : Create a rewrite rule for an application gateway</span></span>
```powershell
PS C:\> $rule = New-AzApplicationGatewayRewriteRule -Name rule1 -ActionSet $action -RuleSequence 101 -Condition $condition
```

<span data-ttu-id="d3053-109">Эта команда создает правило переописи с именем "правило1" и сохраняет результат в переменной с именем $rule.</span><span class="sxs-lookup"><span data-stu-id="d3053-109">This command creates a rewrite rule named rule1 and stores the result in the variable named $rule.</span></span>

## <span data-ttu-id="d3053-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3053-110">PARAMETERS</span></span>

### <span data-ttu-id="d3053-111">-ActionSet</span><span class="sxs-lookup"><span data-stu-id="d3053-111">-ActionSet</span></span>
<span data-ttu-id="d3053-112">Набор действий для правила переписывание</span><span class="sxs-lookup"><span data-stu-id="d3053-112">ActionSet of the rewrite rule</span></span>

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

### <span data-ttu-id="d3053-113">-Условие</span><span class="sxs-lookup"><span data-stu-id="d3053-113">-Condition</span></span>
<span data-ttu-id="d3053-114">Условие для выполнения правила переописи</span><span class="sxs-lookup"><span data-stu-id="d3053-114">Condition for the rewrite rule to execute</span></span>

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

### <span data-ttu-id="d3053-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3053-115">-DefaultProfile</span></span>
<span data-ttu-id="d3053-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3053-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3053-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d3053-117">-Name</span></span>
<span data-ttu-id="d3053-118">Имя rewriteRule</span><span class="sxs-lookup"><span data-stu-id="d3053-118">The name of the RewriteRule</span></span>

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

### <span data-ttu-id="d3053-119">-RuleSequence</span><span class="sxs-lookup"><span data-stu-id="d3053-119">-RuleSequence</span></span>
<span data-ttu-id="d3053-120">Порядок правил для этого правила переописи в наборе правил переписывание</span><span class="sxs-lookup"><span data-stu-id="d3053-120">The rule ordering of this rewrite rule in the rewrite rule set</span></span>

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

### <span data-ttu-id="d3053-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3053-121">CommonParameters</span></span>
<span data-ttu-id="d3053-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3053-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3053-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3053-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3053-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3053-124">INPUTS</span></span>

### <span data-ttu-id="d3053-125">Нет</span><span class="sxs-lookup"><span data-stu-id="d3053-125">None</span></span>

## <span data-ttu-id="d3053-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3053-126">OUTPUTS</span></span>

### <span data-ttu-id="d3053-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d3053-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRule</span></span>

## <span data-ttu-id="d3053-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3053-128">NOTES</span></span>

## <span data-ttu-id="d3053-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3053-129">RELATED LINKS</span></span>

[<span data-ttu-id="d3053-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3053-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3053-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3053-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3053-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3053-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3053-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3053-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3053-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3053-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d3053-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d3053-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)

[<span data-ttu-id="d3053-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3053-136">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>](./New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md)
