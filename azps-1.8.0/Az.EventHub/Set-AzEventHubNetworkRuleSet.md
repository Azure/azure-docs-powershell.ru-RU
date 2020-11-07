---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 72be362d513f447e32db0fe13b5e4b7b076ab947
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730808"
---
# <span data-ttu-id="5d5b9-101">Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d5b9-101">Set-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="5d5b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="5d5b9-103">Обновите NetwrokruleSet данного Namepsace в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-103">Update the NetwrokruleSet of the given Namepsace in the current Azure subscription.</span></span>

## <span data-ttu-id="5d5b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d5b9-104">SYNTAX</span></span>

### <span data-ttu-id="5d5b9-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d5b9-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNteworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d5b9-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5d5b9-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d5b9-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d5b9-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d5b9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d5b9-108">DESCRIPTION</span></span>
<span data-ttu-id="5d5b9-109">Обновите NetwrokruleSet данного Namepsace в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-109">Update the NetwrokruleSet of the given Namepsace in the current Azure subscription.</span></span>

## <span data-ttu-id="5d5b9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d5b9-110">EXAMPLES</span></span>

### <span data-ttu-id="5d5b9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d5b9-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace EventHub-Namespace1-1375 -IPRule $IpRules -VirtualNteworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="5d5b9-112">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="5d5b9-113">Обновление параметров NetworkRuleSet с помощью IPRule и-VirtualNteworkRule</span><span class="sxs-lookup"><span data-stu-id="5d5b9-113">Update the NetworkRuleSet using -IPRule and -VirtualNteworkRule parameters</span></span>

### <span data-ttu-id="5d5b9-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5d5b9-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="5d5b9-115">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="5d5b9-116">Обновление NetworkRuleSet с помощью-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d5b9-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="5d5b9-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5d5b9-117">Example 3</span></span>
```powershell
PS C:\> Set-AzEventHubNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375
```
<span data-ttu-id="5d5b9-118">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1122/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="5d5b9-119">Обновите NetworkRuleSet с помощью параметра-ResourceId для другого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="5d5b9-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d5b9-120">PARAMETERS</span></span>

### <span data-ttu-id="5d5b9-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="5d5b9-121">-DefaultAction</span></span>
<span data-ttu-id="5d5b9-122">Действие по умолчанию для NetwrokeuleSet</span><span class="sxs-lookup"><span data-stu-id="5d5b9-122">Default Action for NetwrokeuleSet</span></span>

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

### <span data-ttu-id="5d5b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d5b9-123">-DefaultProfile</span></span>
<span data-ttu-id="5d5b9-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d5b9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d5b9-125">-InputObject</span></span>
<span data-ttu-id="5d5b9-126">Объект конфигурации NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="5d5b9-126">NetworkruleSet Configuration Object</span></span>

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

### <span data-ttu-id="5d5b9-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="5d5b9-127">-IPRule</span></span>
<span data-ttu-id="5d5b9-128">Список IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="5d5b9-128">List of IPRuleSet</span></span>

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

### <span data-ttu-id="5d5b9-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d5b9-129">-Name</span></span>
<span data-ttu-id="5d5b9-130">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="5d5b9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d5b9-131">-ResourceGroupName</span></span>
<span data-ttu-id="5d5b9-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="5d5b9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d5b9-133">-ResourceId</span></span>
<span data-ttu-id="5d5b9-134">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="5d5b9-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="5d5b9-135">-VirtualNteworkRule</span><span class="sxs-lookup"><span data-stu-id="5d5b9-135">-VirtualNteworkRule</span></span>
<span data-ttu-id="5d5b9-136">Список VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="5d5b9-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d5b9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d5b9-137">-Confirm</span></span>
<span data-ttu-id="5d5b9-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d5b9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d5b9-139">-WhatIf</span></span>
<span data-ttu-id="5d5b9-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d5b9-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d5b9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d5b9-142">CommonParameters</span></span>
<span data-ttu-id="5d5b9-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5d5b9-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d5b9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d5b9-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d5b9-145">INPUTS</span></span>

### <span data-ttu-id="5d5b9-146">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5d5b9-146">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="5d5b9-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5d5b9-147">System.String</span></span>

## <span data-ttu-id="5d5b9-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d5b9-148">OUTPUTS</span></span>

### <span data-ttu-id="5d5b9-149">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="5d5b9-149">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="5d5b9-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d5b9-150">NOTES</span></span>

## <span data-ttu-id="5d5b9-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d5b9-151">RELATED LINKS</span></span>