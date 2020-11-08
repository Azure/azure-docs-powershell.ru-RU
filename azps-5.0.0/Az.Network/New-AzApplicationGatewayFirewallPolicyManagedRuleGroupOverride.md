---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246199"
---
# <span data-ttu-id="d33f1-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d33f1-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="d33f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d33f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d33f1-103">Создает запись RuleGroupOverride в ManagedRuleSets для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d33f1-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="d33f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d33f1-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d33f1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d33f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d33f1-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** создает запись RuleGroupOverride в managedRuleSet для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d33f1-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="d33f1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d33f1-107">EXAMPLES</span></span>

### <span data-ttu-id="d33f1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d33f1-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="d33f1-109">Создает запись RuleGroupOverride с именем группы в качестве $ruleName, а правила — $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="d33f1-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="d33f1-110">Назначает тот же самый $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="d33f1-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="d33f1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d33f1-111">PARAMETERS</span></span>

### <span data-ttu-id="d33f1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d33f1-112">-DefaultProfile</span></span>
<span data-ttu-id="d33f1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d33f1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d33f1-114">-Правило</span><span class="sxs-lookup"><span data-stu-id="d33f1-114">-Rule</span></span>
<span data-ttu-id="d33f1-115">Список правил.</span><span class="sxs-lookup"><span data-stu-id="d33f1-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d33f1-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="d33f1-116">-RuleGroupName</span></span>
<span data-ttu-id="d33f1-117">Укажите ruleGroupName в записи переопределения RuleGroup.</span><span class="sxs-lookup"><span data-stu-id="d33f1-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="d33f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d33f1-118">CommonParameters</span></span>
<span data-ttu-id="d33f1-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d33f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d33f1-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d33f1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d33f1-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d33f1-121">INPUTS</span></span>

### <span data-ttu-id="d33f1-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="d33f1-122">None</span></span>

## <span data-ttu-id="d33f1-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d33f1-123">OUTPUTS</span></span>

### <span data-ttu-id="d33f1-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d33f1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="d33f1-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="d33f1-125">NOTES</span></span>

## <span data-ttu-id="d33f1-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d33f1-126">RELATED LINKS</span></span>
