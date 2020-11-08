---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079480"
---
# <span data-ttu-id="bce6f-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="bce6f-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="bce6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bce6f-102">SYNOPSIS</span></span>
<span data-ttu-id="bce6f-103">Создание записи managedRuleOverride для записи RuleGroupOverrideGroup.</span><span class="sxs-lookup"><span data-stu-id="bce6f-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="bce6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bce6f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bce6f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bce6f-105">DESCRIPTION</span></span>
<span data-ttu-id="bce6f-106">**New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** создает запись ruleOverride.</span><span class="sxs-lookup"><span data-stu-id="bce6f-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="bce6f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bce6f-107">EXAMPLES</span></span>

### <span data-ttu-id="bce6f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bce6f-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="bce6f-109">Создает запись ruleOverride с RuleId как $ruleId и состоянием "отключено".</span><span class="sxs-lookup"><span data-stu-id="bce6f-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="bce6f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bce6f-110">PARAMETERS</span></span>

### <span data-ttu-id="bce6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce6f-111">-DefaultProfile</span></span>
<span data-ttu-id="bce6f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bce6f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce6f-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="bce6f-113">-RuleId</span></span>
<span data-ttu-id="bce6f-114">Укажите RuleId в записи правила переопределения.</span><span class="sxs-lookup"><span data-stu-id="bce6f-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="bce6f-115">-State</span><span class="sxs-lookup"><span data-stu-id="bce6f-115">-State</span></span>
<span data-ttu-id="bce6f-116">Укажите RuleId в записи правила переопределения.</span><span class="sxs-lookup"><span data-stu-id="bce6f-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="bce6f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce6f-117">CommonParameters</span></span>
<span data-ttu-id="bce6f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bce6f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce6f-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bce6f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce6f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bce6f-120">INPUTS</span></span>

### <span data-ttu-id="bce6f-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="bce6f-121">None</span></span>

## <span data-ttu-id="bce6f-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bce6f-122">OUTPUTS</span></span>

### <span data-ttu-id="bce6f-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="bce6f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="bce6f-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="bce6f-124">NOTES</span></span>

## <span data-ttu-id="bce6f-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bce6f-125">RELATED LINKS</span></span>
