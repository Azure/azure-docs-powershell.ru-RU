---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407383"
---
# <span data-ttu-id="635a7-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="635a7-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="635a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="635a7-102">SYNOPSIS</span></span>
<span data-ttu-id="635a7-103">Обновив NetworkruleSet данного пространства имен в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="635a7-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="635a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="635a7-104">SYNTAX</span></span>

### <span data-ttu-id="635a7-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="635a7-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635a7-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="635a7-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="635a7-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="635a7-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="635a7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="635a7-108">DESCRIPTION</span></span>
<span data-ttu-id="635a7-109">Обновив NetworkruleSet данного пространства имен в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="635a7-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="635a7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="635a7-110">EXAMPLES</span></span>

### <span data-ttu-id="635a7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="635a7-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="635a7-112">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="635a7-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="635a7-113">Обновление NetworkRuleSet с помощью параметров -IPRule и -VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="635a7-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="635a7-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="635a7-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="635a7-115">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="635a7-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="635a7-116">Обновление NetworkRuleSet с помощью -InputObject</span><span class="sxs-lookup"><span data-stu-id="635a7-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="635a7-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="635a7-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="635a7-118">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span><span class="sxs-lookup"><span data-stu-id="635a7-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="635a7-119">Обновите NetworkRuleSet, используя -ResourceId другого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="635a7-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="635a7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="635a7-120">PARAMETERS</span></span>

### <span data-ttu-id="635a7-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="635a7-121">-DefaultAction</span></span>
<span data-ttu-id="635a7-122">Действие по умолчанию для NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="635a7-122">Default Action for NetworkRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635a7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="635a7-123">-DefaultProfile</span></span>
<span data-ttu-id="635a7-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="635a7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="635a7-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="635a7-125">-InputObject</span></span>
<span data-ttu-id="635a7-126">Объект Конфигурации NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="635a7-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="635a7-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="635a7-127">-IPRule</span></span>
<span data-ttu-id="635a7-128">Список IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="635a7-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635a7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="635a7-129">-Name</span></span>
<span data-ttu-id="635a7-130">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="635a7-130">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635a7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="635a7-131">-ResourceGroupName</span></span>
<span data-ttu-id="635a7-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="635a7-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635a7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="635a7-133">-ResourceId</span></span>
<span data-ttu-id="635a7-134">ИД ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="635a7-134">Resource ID of Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="635a7-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="635a7-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="635a7-136">Указывает на то, включена ли trustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="635a7-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635a7-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="635a7-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="635a7-138">Список VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="635a7-138">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635a7-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="635a7-139">-Confirm</span></span>
<span data-ttu-id="635a7-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="635a7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="635a7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="635a7-141">-WhatIf</span></span>
<span data-ttu-id="635a7-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="635a7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="635a7-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="635a7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="635a7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635a7-144">CommonParameters</span></span>
<span data-ttu-id="635a7-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="635a7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="635a7-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="635a7-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635a7-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="635a7-147">INPUTS</span></span>

### <span data-ttu-id="635a7-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="635a7-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="635a7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="635a7-149">System.String</span></span>

## <span data-ttu-id="635a7-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="635a7-150">OUTPUTS</span></span>

### <span data-ttu-id="635a7-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="635a7-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="635a7-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="635a7-152">NOTES</span></span>

## <span data-ttu-id="635a7-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="635a7-153">RELATED LINKS</span></span>