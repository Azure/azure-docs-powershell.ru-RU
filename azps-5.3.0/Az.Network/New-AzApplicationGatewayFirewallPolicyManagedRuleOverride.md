---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425415"
---
# <span data-ttu-id="a55f9-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a55f9-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="a55f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a55f9-102">SYNOPSIS</span></span>
<span data-ttu-id="a55f9-103">Создает запись ManagedRuleOverride для записи RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="a55f9-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="a55f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a55f9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a55f9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a55f9-105">DESCRIPTION</span></span>
<span data-ttu-id="a55f9-106">Запись ruleOverride создается с помощью **new-AzApplicationGatewayFirewallPolicyManagedRuleOverride.**</span><span class="sxs-lookup"><span data-stu-id="a55f9-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="a55f9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a55f9-107">EXAMPLES</span></span>

### <span data-ttu-id="a55f9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a55f9-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="a55f9-109">Создание записи ruleOverride с ruleId как $ruleId состоянием отключенным.</span><span class="sxs-lookup"><span data-stu-id="a55f9-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="a55f9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a55f9-110">PARAMETERS</span></span>

### <span data-ttu-id="a55f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55f9-111">-DefaultProfile</span></span>
<span data-ttu-id="a55f9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a55f9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a55f9-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="a55f9-113">-RuleId</span></span>
<span data-ttu-id="a55f9-114">Укажите RuleId в записи переопределения правила.</span><span class="sxs-lookup"><span data-stu-id="a55f9-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="a55f9-115">-State</span><span class="sxs-lookup"><span data-stu-id="a55f9-115">-State</span></span>
<span data-ttu-id="a55f9-116">Укажите RuleId в записи переопределения правила.</span><span class="sxs-lookup"><span data-stu-id="a55f9-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="a55f9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55f9-117">CommonParameters</span></span>
<span data-ttu-id="a55f9-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a55f9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55f9-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a55f9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55f9-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a55f9-120">INPUTS</span></span>

### <span data-ttu-id="a55f9-121">Нет</span><span class="sxs-lookup"><span data-stu-id="a55f9-121">None</span></span>

## <span data-ttu-id="a55f9-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a55f9-122">OUTPUTS</span></span>

### <span data-ttu-id="a55f9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a55f9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="a55f9-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a55f9-124">NOTES</span></span>

## <span data-ttu-id="a55f9-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a55f9-125">RELATED LINKS</span></span>
