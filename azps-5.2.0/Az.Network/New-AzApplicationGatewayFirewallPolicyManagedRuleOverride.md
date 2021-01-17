---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397943"
---
# <span data-ttu-id="be854-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="be854-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="be854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be854-102">SYNOPSIS</span></span>
<span data-ttu-id="be854-103">Создает запись ManagedRuleOverride для записи RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="be854-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="be854-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be854-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be854-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be854-105">DESCRIPTION</span></span>
<span data-ttu-id="be854-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** создает запись ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="be854-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="be854-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be854-107">EXAMPLES</span></span>

### <span data-ttu-id="be854-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be854-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="be854-109">Создание записи ruleOverride с ruleId как $ruleId состоянием отключенным.</span><span class="sxs-lookup"><span data-stu-id="be854-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="be854-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be854-110">PARAMETERS</span></span>

### <span data-ttu-id="be854-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be854-111">-DefaultProfile</span></span>
<span data-ttu-id="be854-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be854-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be854-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="be854-113">-RuleId</span></span>
<span data-ttu-id="be854-114">Укажите RuleId в записи переопределения правила.</span><span class="sxs-lookup"><span data-stu-id="be854-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="be854-115">-State</span><span class="sxs-lookup"><span data-stu-id="be854-115">-State</span></span>
<span data-ttu-id="be854-116">Укажите RuleId в записи переопределения правила.</span><span class="sxs-lookup"><span data-stu-id="be854-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="be854-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be854-117">CommonParameters</span></span>
<span data-ttu-id="be854-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be854-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be854-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be854-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be854-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be854-120">INPUTS</span></span>

### <span data-ttu-id="be854-121">Нет</span><span class="sxs-lookup"><span data-stu-id="be854-121">None</span></span>

## <span data-ttu-id="be854-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be854-122">OUTPUTS</span></span>

### <span data-ttu-id="be854-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="be854-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="be854-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be854-124">NOTES</span></span>

## <span data-ttu-id="be854-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be854-125">RELATED LINKS</span></span>
