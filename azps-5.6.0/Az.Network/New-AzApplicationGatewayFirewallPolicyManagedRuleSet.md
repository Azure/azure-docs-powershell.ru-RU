---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: d8cb1e6f36433168d830c79c2bcbf8b5c259cf32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962691"
---
# <span data-ttu-id="a27d6-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a27d6-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="a27d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a27d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a27d6-103">Создает ManagedRuleSet для firewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="a27d6-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="a27d6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a27d6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a27d6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a27d6-105">DESCRIPTION</span></span>
<span data-ttu-id="a27d6-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleSet** создает управляемые правила для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a27d6-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="a27d6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a27d6-107">EXAMPLES</span></span>

### <span data-ttu-id="a27d6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a27d6-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="a27d6-109">Создает ManagedRuleSet с типом ruleSetType как $ruleSetType, ruleSetVersion как $ruleSetVersion и RuleGroupOverrides в качестве списка с целиком как $ruleGroupOverride 1, $ruleGroupOverride 2 Новый ManagedRuleSet назначен $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a27d6-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="a27d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a27d6-110">PARAMETERS</span></span>

### <span data-ttu-id="a27d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27d6-111">-DefaultProfile</span></span>
<span data-ttu-id="a27d6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a27d6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a27d6-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a27d6-113">-RuleGroupOverride</span></span>
<span data-ttu-id="a27d6-114">Переопределения группы правил.</span><span class="sxs-lookup"><span data-stu-id="a27d6-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a27d6-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="a27d6-115">-RuleSetType</span></span>
<span data-ttu-id="a27d6-116">Укажите Тип RuleSetType в managedRuleSet.</span><span class="sxs-lookup"><span data-stu-id="a27d6-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="a27d6-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="a27d6-117">-RuleSetVersion</span></span>
<span data-ttu-id="a27d6-118">Укажите RuleSetVersion в managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a27d6-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="a27d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27d6-119">CommonParameters</span></span>
<span data-ttu-id="a27d6-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a27d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27d6-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a27d6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27d6-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a27d6-122">INPUTS</span></span>

### <span data-ttu-id="a27d6-123">Нет</span><span class="sxs-lookup"><span data-stu-id="a27d6-123">None</span></span>

## <span data-ttu-id="a27d6-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a27d6-124">OUTPUTS</span></span>

### <span data-ttu-id="a27d6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a27d6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="a27d6-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a27d6-126">NOTES</span></span>

## <span data-ttu-id="a27d6-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a27d6-127">RELATED LINKS</span></span>
