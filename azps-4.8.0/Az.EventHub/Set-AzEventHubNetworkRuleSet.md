---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 6f769613516dbd1f94400832bd8fac0045fec198
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078280"
---
# <span data-ttu-id="6f251-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f251-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="6f251-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f251-102">SYNOPSIS</span></span>
<span data-ttu-id="6f251-103">Обновите NetworkruleSet указанного пространства имен в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6f251-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="6f251-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f251-104">SYNTAX</span></span>

### <span data-ttu-id="6f251-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f251-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-TrustedServiceAccessEnabled] [-IPRule] <PSNWRuleSetIpRulesAttributes[]>
 [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f251-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f251-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f251-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f251-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f251-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f251-108">DESCRIPTION</span></span>
<span data-ttu-id="6f251-109">Обновите NetworkruleSet указанного пространства имен в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6f251-109">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="6f251-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f251-110">EXAMPLES</span></span>

### <span data-ttu-id="6f251-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f251-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="6f251-112">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="6f251-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="6f251-113">Обновление параметров NetworkRuleSet с помощью IPRule и-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6f251-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="6f251-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6f251-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="6f251-115">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="6f251-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="6f251-116">Обновление NetworkRuleSet с помощью-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f251-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="6f251-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6f251-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="6f251-118">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="6f251-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="6f251-119">Обновите NetworkRuleSet с помощью параметра-ResourceId для другого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6f251-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="6f251-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f251-120">PARAMETERS</span></span>

### <span data-ttu-id="6f251-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="6f251-121">-DefaultAction</span></span>
<span data-ttu-id="6f251-122">Действие по умолчанию для NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f251-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="6f251-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f251-123">-DefaultProfile</span></span>
<span data-ttu-id="6f251-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f251-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f251-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f251-125">-InputObject</span></span>
<span data-ttu-id="6f251-126">Объект конфигурации NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="6f251-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="6f251-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="6f251-127">-IPRule</span></span>
<span data-ttu-id="6f251-128">Список IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="6f251-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="6f251-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f251-129">-Name</span></span>
<span data-ttu-id="6f251-130">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="6f251-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="6f251-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f251-131">-ResourceGroupName</span></span>
<span data-ttu-id="6f251-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f251-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="6f251-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f251-133">-ResourceId</span></span>
<span data-ttu-id="6f251-134">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="6f251-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="6f251-135">-TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="6f251-135">-TrustedServiceAccessEnabled</span></span>
<span data-ttu-id="6f251-136">Указывает, включена ли TrustedServiceAccessEnabled</span><span class="sxs-lookup"><span data-stu-id="6f251-136">Indicates whether TrustedServiceAccessEnabled is enabled</span></span>

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

### <span data-ttu-id="6f251-137">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6f251-137">-VirtualNetworkRule</span></span>
<span data-ttu-id="6f251-138">Список VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="6f251-138">List of VirtualNetworkRules</span></span>

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

### <span data-ttu-id="6f251-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f251-139">-Confirm</span></span>
<span data-ttu-id="6f251-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f251-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f251-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f251-141">-WhatIf</span></span>
<span data-ttu-id="6f251-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f251-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f251-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f251-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f251-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f251-144">CommonParameters</span></span>
<span data-ttu-id="6f251-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f251-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6f251-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f251-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f251-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f251-147">INPUTS</span></span>

### <span data-ttu-id="6f251-148">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="6f251-148">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="6f251-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6f251-149">System.String</span></span>

## <span data-ttu-id="6f251-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f251-150">OUTPUTS</span></span>

### <span data-ttu-id="6f251-151">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="6f251-151">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="6f251-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f251-152">NOTES</span></span>

## <span data-ttu-id="6f251-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f251-153">RELATED LINKS</span></span>