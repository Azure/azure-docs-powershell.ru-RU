---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213817"
---
# <span data-ttu-id="0b36c-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0b36c-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="0b36c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b36c-102">SYNOPSIS</span></span>
<span data-ttu-id="0b36c-103">Создает запись RuleGroupOverride в ManagedRuleSets для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="0b36c-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="0b36c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0b36c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b36c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b36c-105">DESCRIPTION</span></span>
<span data-ttu-id="0b36c-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** создает запись ruleGroupOverride в managedRuleSet для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="0b36c-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="0b36c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0b36c-107">EXAMPLES</span></span>

### <span data-ttu-id="0b36c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b36c-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="0b36c-109">Создание записи RuleGroupOverride с именем группы в $ruleName и правилами $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="0b36c-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="0b36c-110">Назначает то же самое $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="0b36c-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="0b36c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b36c-111">PARAMETERS</span></span>

### <span data-ttu-id="0b36c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b36c-112">-DefaultProfile</span></span>
<span data-ttu-id="0b36c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b36c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b36c-114">-Правило</span><span class="sxs-lookup"><span data-stu-id="0b36c-114">-Rule</span></span>
<span data-ttu-id="0b36c-115">Список правил.</span><span class="sxs-lookup"><span data-stu-id="0b36c-115">List of Rules.</span></span>

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

### <span data-ttu-id="0b36c-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="0b36c-116">-RuleGroupName</span></span>
<span data-ttu-id="0b36c-117">Укажите имягруппы правил в переопределеемом записи RuleGroup.</span><span class="sxs-lookup"><span data-stu-id="0b36c-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="0b36c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b36c-118">CommonParameters</span></span>
<span data-ttu-id="0b36c-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b36c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b36c-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b36c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b36c-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b36c-121">INPUTS</span></span>

### <span data-ttu-id="0b36c-122">Нет</span><span class="sxs-lookup"><span data-stu-id="0b36c-122">None</span></span>

## <span data-ttu-id="0b36c-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0b36c-123">OUTPUTS</span></span>

### <span data-ttu-id="0b36c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0b36c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="0b36c-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0b36c-125">NOTES</span></span>

## <span data-ttu-id="0b36c-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b36c-126">RELATED LINKS</span></span>
