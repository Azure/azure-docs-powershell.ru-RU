---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402164"
---
# <span data-ttu-id="e7989-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e7989-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="e7989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7989-102">SYNOPSIS</span></span>
<span data-ttu-id="e7989-103">Создает ManagedRuleSet для firewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="e7989-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="e7989-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7989-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7989-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7989-105">DESCRIPTION</span></span>
<span data-ttu-id="e7989-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleSet** создает управляемые правила для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e7989-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="e7989-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7989-107">EXAMPLES</span></span>

### <span data-ttu-id="e7989-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7989-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="e7989-109">Создает ManagedRuleSet с типом ruleSetType $ruleSetType, ruleSetVersion как $ruleSetVersion и RuleGroupOverrides в качестве списка с целиком как $ruleGroupOverride 1, $ruleGroupOverride 2 Новый ManagedRuleSet назначен $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e7989-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="e7989-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7989-110">PARAMETERS</span></span>

### <span data-ttu-id="e7989-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7989-111">-DefaultProfile</span></span>
<span data-ttu-id="e7989-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7989-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7989-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e7989-113">-RuleGroupOverride</span></span>
<span data-ttu-id="e7989-114">Переопределения группы правил.</span><span class="sxs-lookup"><span data-stu-id="e7989-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="e7989-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="e7989-115">-RuleSetType</span></span>
<span data-ttu-id="e7989-116">Укажите Тип RuleSetType в managedRuleSet.</span><span class="sxs-lookup"><span data-stu-id="e7989-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="e7989-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="e7989-117">-RuleSetVersion</span></span>
<span data-ttu-id="e7989-118">Укажите RuleSetVersion в managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e7989-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="e7989-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7989-119">CommonParameters</span></span>
<span data-ttu-id="e7989-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7989-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7989-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7989-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7989-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7989-122">INPUTS</span></span>

### <span data-ttu-id="e7989-123">Нет</span><span class="sxs-lookup"><span data-stu-id="e7989-123">None</span></span>

## <span data-ttu-id="e7989-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7989-124">OUTPUTS</span></span>

### <span data-ttu-id="e7989-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="e7989-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="e7989-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7989-126">NOTES</span></span>

## <span data-ttu-id="e7989-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7989-127">RELATED LINKS</span></span>
