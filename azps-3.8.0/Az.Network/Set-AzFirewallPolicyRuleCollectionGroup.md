---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8e1260a636a1be5a42888fcc6cc12cb8b228859c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066979"
---
# <span data-ttu-id="7d65d-101">Set-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="7d65d-101">Set-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="7d65d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d65d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d65d-103">Сохранение измененной группы набора правил политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="7d65d-103">saves a modified azure firewall policy rule collection group</span></span>

## <span data-ttu-id="7d65d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d65d-104">SYNTAX</span></span>

### <span data-ttu-id="7d65d-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d65d-105">SetByNameParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String> -FirewallPolicyName <String>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d65d-106">SetByParentInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d65d-106">SetByParentInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -Name <String> -FirewallPolicyObject <PSAzureFirewallPolicy>
 -Priority <UInt32> -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d65d-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d65d-107">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -InputObject <PSAzureFirewallPolicyRuleCollectionGroupWrapper>
 [-Priority <UInt32>] [-RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d65d-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d65d-108">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d65d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d65d-109">DESCRIPTION</span></span>
<span data-ttu-id="7d65d-110">Командлет **Set-AzFirewallPolicyRuleCollectionGroup** обновляет группы коллекций правил в политике брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7d65d-110">The **Set-AzFirewallPolicyRuleCollectionGroup** cmdlet updates a rule collection groups in an Azure Firewall Policy.</span></span>

## <span data-ttu-id="7d65d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d65d-111">EXAMPLES</span></span>

### <span data-ttu-id="7d65d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d65d-112">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="7d65d-113">Этот пример обновляет группу коллекции правил в политике брандмауэра $fp</span><span class="sxs-lookup"><span data-stu-id="7d65d-113">This example updates a rule collection group in the firewall policy $fp</span></span>

## <span data-ttu-id="7d65d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d65d-114">PARAMETERS</span></span>

### <span data-ttu-id="7d65d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d65d-115">-DefaultProfile</span></span>
<span data-ttu-id="7d65d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d65d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d65d-117">-FirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="7d65d-117">-FirewallPolicyName</span></span>
<span data-ttu-id="7d65d-118">Имя политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="7d65d-118">The name of the firewall policy</span></span>

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

### <span data-ttu-id="7d65d-119">-FirewallPolicyObject</span><span class="sxs-lookup"><span data-stu-id="7d65d-119">-FirewallPolicyObject</span></span>
<span data-ttu-id="7d65d-120">Политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="7d65d-120">Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByParentInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d65d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d65d-121">-InputObject</span></span>
<span data-ttu-id="7d65d-122">Список правил</span><span class="sxs-lookup"><span data-stu-id="7d65d-122">The list of rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroupWrapper
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d65d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d65d-123">-Name</span></span>
<span data-ttu-id="7d65d-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="7d65d-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByParentInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d65d-125">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="7d65d-125">-Priority</span></span>
<span data-ttu-id="7d65d-126">Приоритет группы правил</span><span class="sxs-lookup"><span data-stu-id="7d65d-126">The priority of the rule group</span></span>

```yaml
Type: System.UInt32
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d65d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d65d-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d65d-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d65d-128">The resource group name.</span></span>

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

### <span data-ttu-id="7d65d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d65d-129">-ResourceId</span></span>
<span data-ttu-id="7d65d-130">Идентификатор ресурса группы набора правил</span><span class="sxs-lookup"><span data-stu-id="7d65d-130">The resource Id of the Rule collection groupy</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d65d-131">-RuleCollection</span><span class="sxs-lookup"><span data-stu-id="7d65d-131">-RuleCollection</span></span>
<span data-ttu-id="7d65d-132">Список коллекций правил</span><span class="sxs-lookup"><span data-stu-id="7d65d-132">The list of rule collections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByNameParameterSet, SetByParentInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d65d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d65d-133">-Confirm</span></span>
<span data-ttu-id="7d65d-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d65d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d65d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d65d-135">-WhatIf</span></span>
<span data-ttu-id="7d65d-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d65d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d65d-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d65d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d65d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d65d-138">CommonParameters</span></span>
<span data-ttu-id="7d65d-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d65d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d65d-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d65d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d65d-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d65d-141">INPUTS</span></span>

### <span data-ttu-id="7d65d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7d65d-142">System.String</span></span>

### <span data-ttu-id="7d65d-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7d65d-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="7d65d-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d65d-144">OUTPUTS</span></span>

### <span data-ttu-id="7d65d-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="7d65d-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="7d65d-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d65d-146">NOTES</span></span>

## <span data-ttu-id="7d65d-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d65d-147">RELATED LINKS</span></span>
