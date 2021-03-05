---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: 31c12fd53c8aa6c886ab5e26a8c35996045335e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992645"
---
# <span data-ttu-id="bd9ab-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="bd9ab-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="bd9ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9ab-103">Создает запись ManagedRuleOverride для записи RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="bd9ab-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="bd9ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd9ab-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd9ab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd9ab-105">DESCRIPTION</span></span>
<span data-ttu-id="bd9ab-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** создает запись ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="bd9ab-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="bd9ab-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd9ab-107">EXAMPLES</span></span>

### <span data-ttu-id="bd9ab-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd9ab-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="bd9ab-109">Создает запись ruleOverride с ruleId как $ruleId состоянием отключенным.</span><span class="sxs-lookup"><span data-stu-id="bd9ab-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="bd9ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd9ab-110">PARAMETERS</span></span>

### <span data-ttu-id="bd9ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9ab-111">-DefaultProfile</span></span>
<span data-ttu-id="bd9ab-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd9ab-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="bd9ab-113">-RuleId</span></span>
<span data-ttu-id="bd9ab-114">Укажите RuleId в записи переопределения правила.</span><span class="sxs-lookup"><span data-stu-id="bd9ab-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="bd9ab-115">-State</span><span class="sxs-lookup"><span data-stu-id="bd9ab-115">-State</span></span>
<span data-ttu-id="bd9ab-116">Укажите RuleId в записи переопределения правила.</span><span class="sxs-lookup"><span data-stu-id="bd9ab-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd9ab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9ab-117">CommonParameters</span></span>
<span data-ttu-id="bd9ab-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd9ab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9ab-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd9ab-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9ab-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd9ab-120">INPUTS</span></span>

### <span data-ttu-id="bd9ab-121">Нет</span><span class="sxs-lookup"><span data-stu-id="bd9ab-121">None</span></span>

## <span data-ttu-id="bd9ab-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd9ab-122">OUTPUTS</span></span>

### <span data-ttu-id="bd9ab-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="bd9ab-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="bd9ab-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd9ab-124">NOTES</span></span>

## <span data-ttu-id="bd9ab-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd9ab-125">RELATED LINKS</span></span>
