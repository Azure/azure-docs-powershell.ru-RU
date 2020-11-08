---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074816"
---
# <span data-ttu-id="459e9-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="459e9-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="459e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="459e9-102">SYNOPSIS</span></span>
<span data-ttu-id="459e9-103">Создайте ManagedRules для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="459e9-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="459e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="459e9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="459e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="459e9-105">DESCRIPTION</span></span>
<span data-ttu-id="459e9-106">**Новый параметр-AzApplicationGatewayFirewallPolicyManagedRule** создает управляемые правила для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="459e9-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="459e9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="459e9-107">EXAMPLES</span></span>

### <span data-ttu-id="459e9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="459e9-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="459e9-109">Команда создает управляемые правила список ManagedRuleSet с $managedRuleSet и список исключений с записями $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="459e9-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="459e9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="459e9-110">PARAMETERS</span></span>

### <span data-ttu-id="459e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="459e9-111">-DefaultProfile</span></span>
<span data-ttu-id="459e9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="459e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="459e9-113">-Исключение</span><span class="sxs-lookup"><span data-stu-id="459e9-113">-Exclusion</span></span>
<span data-ttu-id="459e9-114">Список записей исключений.</span><span class="sxs-lookup"><span data-stu-id="459e9-114">List of Exclusion Entry.</span></span>

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

### <span data-ttu-id="459e9-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="459e9-115">-ManagedRuleSet</span></span>
<span data-ttu-id="459e9-116">Список управляемых наборов правил.</span><span class="sxs-lookup"><span data-stu-id="459e9-116">List of Managed ruleSets.</span></span>

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

### <span data-ttu-id="459e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="459e9-117">CommonParameters</span></span>
<span data-ttu-id="459e9-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="459e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="459e9-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="459e9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="459e9-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="459e9-120">INPUTS</span></span>

### <span data-ttu-id="459e9-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="459e9-121">None</span></span>

## <span data-ttu-id="459e9-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="459e9-122">OUTPUTS</span></span>

### <span data-ttu-id="459e9-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="459e9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="459e9-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="459e9-124">NOTES</span></span>

## <span data-ttu-id="459e9-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="459e9-125">RELATED LINKS</span></span>
