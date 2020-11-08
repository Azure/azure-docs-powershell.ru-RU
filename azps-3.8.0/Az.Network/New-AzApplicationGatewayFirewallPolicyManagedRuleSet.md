---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074812"
---
# <span data-ttu-id="610b3-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="610b3-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="610b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="610b3-102">SYNOPSIS</span></span>
<span data-ttu-id="610b3-103">Создает ManagedRuleSet для firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="610b3-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="610b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="610b3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="610b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="610b3-105">DESCRIPTION</span></span>
<span data-ttu-id="610b3-106">**Новый параметр-AzApplicationGatewayFirewallPolicyManagedRuleSet** создает управляемые правила для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="610b3-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="610b3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="610b3-107">EXAMPLES</span></span>

### <span data-ttu-id="610b3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="610b3-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="610b3-109">Создает ManagedRuleSet с ruleSetType как $ruleSetType, ruleSetVersion как $ruleSetVersion и RuleGroupOverrides в виде списка с полным набором, как $ruleGroupOverride 1, $ruleGroupOverride 2, которым назначена новая ManagedRuleSet. $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="610b3-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="610b3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="610b3-110">PARAMETERS</span></span>

### <span data-ttu-id="610b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610b3-111">-DefaultProfile</span></span>
<span data-ttu-id="610b3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="610b3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="610b3-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="610b3-113">-RuleGroupOverride</span></span>
<span data-ttu-id="610b3-114">Переопределение группы правил.</span><span class="sxs-lookup"><span data-stu-id="610b3-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="610b3-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="610b3-115">-RuleSetType</span></span>
<span data-ttu-id="610b3-116">Указание RuleSetType в managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="610b3-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="610b3-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="610b3-117">-RuleSetVersion</span></span>
<span data-ttu-id="610b3-118">Указание RuleSetVersion в managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="610b3-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="610b3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610b3-119">CommonParameters</span></span>
<span data-ttu-id="610b3-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="610b3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610b3-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="610b3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610b3-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="610b3-122">INPUTS</span></span>

### <span data-ttu-id="610b3-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="610b3-123">None</span></span>

## <span data-ttu-id="610b3-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="610b3-124">OUTPUTS</span></span>

### <span data-ttu-id="610b3-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="610b3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="610b3-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="610b3-126">NOTES</span></span>

## <span data-ttu-id="610b3-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="610b3-127">RELATED LINKS</span></span>
