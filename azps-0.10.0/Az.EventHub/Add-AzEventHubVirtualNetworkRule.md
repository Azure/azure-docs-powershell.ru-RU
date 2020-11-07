---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 37f13534095341895a4fc3b4c1c9feb9e5e911be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910411"
---
# <span data-ttu-id="aff39-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aff39-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="aff39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aff39-102">SYNOPSIS</span></span>
<span data-ttu-id="aff39-103">Добавление одного VirtualNetworkRule к NetworkRuleSet для указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="aff39-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="aff39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aff39-104">SYNTAX</span></span>

### <span data-ttu-id="aff39-105">VirtualNetworkRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aff39-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aff39-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aff39-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aff39-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aff39-107">DESCRIPTION</span></span>
<span data-ttu-id="aff39-108">Добавление одного VirtualNetworkRule к NetworkRuleSet для указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="aff39-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="aff39-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aff39-109">EXAMPLES</span></span>

### <span data-ttu-id="aff39-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aff39-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="aff39-111">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="aff39-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="aff39-112">Добавляет заданную подсеть и IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) в NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="aff39-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="aff39-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aff39-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="aff39-114">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules: {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, false}</span><span class="sxs-lookup"><span data-stu-id="aff39-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="aff39-115">Добавляет $virtualruleset 1 в NetworkRuleSet для указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="aff39-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="aff39-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aff39-116">PARAMETERS</span></span>

### <span data-ttu-id="aff39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff39-117">-DefaultProfile</span></span>
<span data-ttu-id="aff39-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aff39-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aff39-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="aff39-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="aff39-120">КОД ARM для подсети</span><span class="sxs-lookup"><span data-stu-id="aff39-120">ARM ID of Subnet</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff39-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aff39-121">-Name</span></span>
<span data-ttu-id="aff39-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="aff39-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff39-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff39-123">-ResourceGroupName</span></span>
<span data-ttu-id="aff39-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="aff39-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff39-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="aff39-125">-SubnetId</span></span>
<span data-ttu-id="aff39-126">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="aff39-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff39-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="aff39-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="aff39-128">Объект конфигурации VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aff39-128">VirtualNetworkRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aff39-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aff39-129">-Confirm</span></span>
<span data-ttu-id="aff39-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aff39-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aff39-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aff39-131">-WhatIf</span></span>
<span data-ttu-id="aff39-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aff39-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aff39-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aff39-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aff39-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff39-134">CommonParameters</span></span>
<span data-ttu-id="aff39-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aff39-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aff39-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff39-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff39-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aff39-137">INPUTS</span></span>

### <span data-ttu-id="aff39-138">System. String</span><span class="sxs-lookup"><span data-stu-id="aff39-138">System.String</span></span>

### <span data-ttu-id="aff39-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aff39-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="aff39-140">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="aff39-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="aff39-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aff39-141">OUTPUTS</span></span>

### <span data-ttu-id="aff39-142">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="aff39-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="aff39-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="aff39-143">NOTES</span></span>

## <span data-ttu-id="aff39-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aff39-144">RELATED LINKS</span></span>
