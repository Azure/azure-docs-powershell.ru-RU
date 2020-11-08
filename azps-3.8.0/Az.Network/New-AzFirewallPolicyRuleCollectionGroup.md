---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 1aeb93085fdf8fa362e38843deacdef6e07929d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066282"
---
# <span data-ttu-id="4d8b9-101">New-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="4d8b9-101">New-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="4d8b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d8b9-103">Создание группы набора правил политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="4d8b9-103">Create a new Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="4d8b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d8b9-104">SYNTAX</span></span>

### <span data-ttu-id="4d8b9-105">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d8b9-105">SetByInputObjectParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d8b9-106">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d8b9-106">SetByNameParameterSet</span></span>
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d8b9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d8b9-107">DESCRIPTION</span></span>
<span data-ttu-id="4d8b9-108">Командлет **New-AzFirewallPolicyRuleCollectionGroup** создает группу семейства правил в политике брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-108">The **New-AzFirewallPolicyRuleCollectionGroup** cmdlet creates a rule collection group in a Azure Firewall Policy.</span></span>

## <span data-ttu-id="4d8b9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d8b9-109">EXAMPLES</span></span>

### <span data-ttu-id="4d8b9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4d8b9-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="4d8b9-111">В этом примере группа "семейство правил" создается в политике брандмауэра $fp</span><span class="sxs-lookup"><span data-stu-id="4d8b9-111">This example creates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="4d8b9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d8b9-112">PARAMETERS</span></span>

### <span data-ttu-id="4d8b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d8b9-113">-DefaultProfile</span></span>
<span data-ttu-id="4d8b9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d8b9-115">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="4d8b9-115">-FirewallPolicyName</span></span>
<span data-ttu-id="4d8b9-116">Имя политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="4d8b9-116">The name of the firewall policy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8b9-117">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="4d8b9-117">-FirewallPolicyObject</span></span>
<span data-ttu-id="4d8b9-118">Политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-118">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8b9-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4d8b9-119">-Name</span></span>
<span data-ttu-id="4d8b9-120">Имя группы правил</span><span class="sxs-lookup"><span data-stu-id="4d8b9-120">The name of the Rule Group</span></span>

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

### <span data-ttu-id="4d8b9-121">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="4d8b9-121">-Priority</span></span>
<span data-ttu-id="4d8b9-122">Приоритет группы правил</span><span class="sxs-lookup"><span data-stu-id="4d8b9-122">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d8b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d8b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="4d8b9-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8b9-125">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="4d8b9-125">-RuleCollection</span></span>
<span data-ttu-id="4d8b9-126">Список правил</span><span class="sxs-lookup"><span data-stu-id="4d8b9-126">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d8b9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d8b9-127">-Confirm</span></span>
<span data-ttu-id="4d8b9-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d8b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d8b9-129">-WhatIf</span></span>
<span data-ttu-id="4d8b9-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d8b9-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d8b9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d8b9-132">CommonParameters</span></span>
<span data-ttu-id="4d8b9-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d8b9-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d8b9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d8b9-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d8b9-135">INPUTS</span></span>

### <span data-ttu-id="4d8b9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4d8b9-136">System.String</span></span>

### <span data-ttu-id="4d8b9-137">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4d8b9-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="4d8b9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d8b9-138">OUTPUTS</span></span>

### <span data-ttu-id="4d8b9-139">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="4d8b9-139">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="4d8b9-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d8b9-140">NOTES</span></span>

## <span data-ttu-id="4d8b9-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d8b9-141">RELATED LINKS</span></span>
