---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397948"
---
# <span data-ttu-id="28a55-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="28a55-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="28a55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a55-102">SYNOPSIS</span></span>
<span data-ttu-id="28a55-103">Создайте ManagedRules для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="28a55-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="28a55-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28a55-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="28a55-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28a55-105">DESCRIPTION</span></span>
<span data-ttu-id="28a55-106">**New-AzApplicationGatewayFirewallPolicyManagedRule** создает управляемые правила для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="28a55-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="28a55-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28a55-107">EXAMPLES</span></span>

### <span data-ttu-id="28a55-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28a55-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="28a55-109">Команда создает список управляемых правил ManagedRuleSet со списком $managedRuleSet и списком исключений с записями $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="28a55-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="28a55-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28a55-110">PARAMETERS</span></span>

### <span data-ttu-id="28a55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a55-111">-DefaultProfile</span></span>
<span data-ttu-id="28a55-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28a55-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a55-113">-Исключение</span><span class="sxs-lookup"><span data-stu-id="28a55-113">-Exclusion</span></span>
<span data-ttu-id="28a55-114">Список исключений.</span><span class="sxs-lookup"><span data-stu-id="28a55-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a55-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="28a55-115">-ManagedRuleSet</span></span>
<span data-ttu-id="28a55-116">Список управляемых правил.</span><span class="sxs-lookup"><span data-stu-id="28a55-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a55-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a55-117">CommonParameters</span></span>
<span data-ttu-id="28a55-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a55-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a55-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28a55-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a55-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28a55-120">INPUTS</span></span>

### <span data-ttu-id="28a55-121">Нет</span><span class="sxs-lookup"><span data-stu-id="28a55-121">None</span></span>

## <span data-ttu-id="28a55-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28a55-122">OUTPUTS</span></span>

### <span data-ttu-id="28a55-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="28a55-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="28a55-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28a55-124">NOTES</span></span>

## <span data-ttu-id="28a55-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28a55-125">RELATED LINKS</span></span>
