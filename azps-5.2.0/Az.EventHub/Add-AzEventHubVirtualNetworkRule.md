---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 627519cd4325e7fb9677c358146f2f8a9081151a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417972"
---
# <span data-ttu-id="ef8b2-101">Add-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ef8b2-101">Add-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="ef8b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef8b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ef8b2-103">Добавление одного экземпляра VirtualNetworkRule в NetworkRuleSet для данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="ef8b2-103">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="ef8b2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef8b2-104">SYNTAX</span></span>

### <span data-ttu-id="ef8b2-105">VirtualNetworkRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef8b2-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef8b2-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef8b2-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef8b2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef8b2-107">DESCRIPTION</span></span>
<span data-ttu-id="ef8b2-108">Добавление одного экземпляра VirtualNetworkRule в NetworkRuleSet для данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="ef8b2-108">Add a single VirtualNetworkRule to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="ef8b2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef8b2-109">EXAMPLES</span></span>

### <span data-ttu-id="ef8b2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef8b2-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01" -IgnoreMissingVnetServiceEndpoint
```

<span data-ttu-id="ef8b2-111">Name : defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="ef8b2-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="ef8b2-112">Добавляет подсеть и IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) в NetworkRuleSet для данного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ef8b2-112">Adds the given Subnet and IgnoreMissingVnetServiceEndpoint (VirtualNetworkRule) to NetworkRuleSet for the given Namespace</span></span>

### <span data-ttu-id="ef8b2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ef8b2-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="ef8b2-114">Name : defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type : Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="ef8b2-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-1122/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules : {/subscriptions/SubscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="ef8b2-115">Добавляет $virtualruleset 1 в NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ef8b2-115">Adds the $virtualruleset1 to NetworkRuleSet for the given Namespace</span></span>

## <span data-ttu-id="ef8b2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef8b2-116">PARAMETERS</span></span>

### <span data-ttu-id="ef8b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef8b2-117">-DefaultProfile</span></span>
<span data-ttu-id="ef8b2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef8b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef8b2-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef8b2-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="ef8b2-120">ARM ИД подсети</span><span class="sxs-lookup"><span data-stu-id="ef8b2-120">ARM ID of Subnet</span></span>

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

### <span data-ttu-id="ef8b2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ef8b2-121">-Name</span></span>
<span data-ttu-id="ef8b2-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ef8b2-122">Namespace Name</span></span>

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

### <span data-ttu-id="ef8b2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef8b2-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef8b2-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ef8b2-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ef8b2-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ef8b2-125">-SubnetId</span></span>
<span data-ttu-id="ef8b2-126">ИД ресурсов подсети</span><span class="sxs-lookup"><span data-stu-id="ef8b2-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="ef8b2-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ef8b2-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="ef8b2-128">Объект конфигурации VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ef8b2-128">VirtualNetworkRule Configuration Object</span></span>

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

### <span data-ttu-id="ef8b2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef8b2-129">-Confirm</span></span>
<span data-ttu-id="ef8b2-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ef8b2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef8b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef8b2-131">-WhatIf</span></span>
<span data-ttu-id="ef8b2-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef8b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef8b2-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ef8b2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef8b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef8b2-134">CommonParameters</span></span>
<span data-ttu-id="ef8b2-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef8b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ef8b2-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef8b2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef8b2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef8b2-137">INPUTS</span></span>

### <span data-ttu-id="ef8b2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ef8b2-138">System.String</span></span>

### <span data-ttu-id="ef8b2-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ef8b2-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ef8b2-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="ef8b2-140">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="ef8b2-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef8b2-141">OUTPUTS</span></span>

### <span data-ttu-id="ef8b2-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ef8b2-142">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ef8b2-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef8b2-143">NOTES</span></span>

## <span data-ttu-id="ef8b2-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef8b2-144">RELATED LINKS</span></span>
