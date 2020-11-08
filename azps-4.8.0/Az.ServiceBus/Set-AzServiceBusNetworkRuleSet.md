---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 87f735a098057beb67b76fd4a0f763732c2e816a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077607"
---
# <span data-ttu-id="2ba3c-101">Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ba3c-101">Set-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="2ba3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ba3c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba3c-103">Обновите NetworkruleSet указанного пространства имен в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-103">Update the NetworkruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="2ba3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ba3c-104">SYNTAX</span></span>

### <span data-ttu-id="2ba3c-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ba3c-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-DefaultAction <String>]
 [-IPRule] <PSNWRuleSetIpRulesAttributes[]> [-VirtualNetworkRule] <PSNWRuleSetVirtualNetworkRulesAttributes[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba3c-106">NetwrokruleSetInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ba3c-106">NetwrokruleSetInputObjectSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSNetworkRuleSetAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ba3c-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ba3c-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Set-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba3c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ba3c-108">DESCRIPTION</span></span>
<span data-ttu-id="2ba3c-109">Обновите NetwrokruleSet указанного пространства имен в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-109">Update the NetwrokruleSet of the given Namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="2ba3c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ba3c-110">EXAMPLES</span></span>

### <span data-ttu-id="2ba3c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ba3c-111">Example 1</span></span> 
```powershell
PS C:\> $IpRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "4.4.4.4";Action = "Allow"},[Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes] @{IpMask = "3.3.3.3";Action = "Allow"})
PS C:\> $VirtualNetworkRules = @([Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes]@{Subnet=@{Id="/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default"};IgnoreMissingVnetServiceEndpoint=$True})
PS C:\>  Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -IPRule $IpRules -VirtualNetworkRule $VirtualNetworkRules -DefaultAction "Allow" -Debug

```

<span data-ttu-id="2ba3c-112">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/Default.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="2ba3c-113">Обновление параметров NetworkRuleSet с помощью IPRule и-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2ba3c-113">Update the NetworkRuleSet using -IPRule and -VirtualNetworkRule parameters</span></span>

### <span data-ttu-id="2ba3c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2ba3c-114">Example 2</span></span>
```powershell
PS C:\> $getresult = Get-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -InputObject $getresult
```

<span data-ttu-id="2ba3c-115">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/Default.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="2ba3c-116">Обновление NetworkRuleSet с помощью-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ba3c-116">Update the NetworkRuleSet using -InputObject</span></span>


### <span data-ttu-id="2ba3c-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2ba3c-117">Example 3</span></span>
```powershell
PS C:\> Set-AzServiceBusNetworkRuleSet -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-1375 -ResourceId /subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```

<span data-ttu-id="2ba3c-118">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules: {/Subscriptions/SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/Default.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {4.4.4.4, Allow, 3.3.3.3, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, True}</span></span>

<span data-ttu-id="2ba3c-119">Обновите NetworkRuleSet с помощью параметра-ResourceId для другого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-119">Update the NetworkRuleSet using -ResourceId of the other namespace.</span></span>

## <span data-ttu-id="2ba3c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ba3c-120">PARAMETERS</span></span>

### <span data-ttu-id="2ba3c-121">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="2ba3c-121">-DefaultAction</span></span>
<span data-ttu-id="2ba3c-122">Действие по умолчанию для NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ba3c-122">Default Action for NetworkRuleSet</span></span>

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

### <span data-ttu-id="2ba3c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba3c-123">-DefaultProfile</span></span>
<span data-ttu-id="2ba3c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ba3c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ba3c-125">-InputObject</span></span>
<span data-ttu-id="2ba3c-126">Объект конфигурации NetworkruleSet</span><span class="sxs-lookup"><span data-stu-id="2ba3c-126">NetworkruleSet Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes
Parameter Sets: NetwrokruleSetInputObjectSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ba3c-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="2ba3c-127">-IPRule</span></span>
<span data-ttu-id="2ba3c-128">Список IPRuleSet</span><span class="sxs-lookup"><span data-stu-id="2ba3c-128">List of IPRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba3c-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ba3c-129">-Name</span></span>
<span data-ttu-id="2ba3c-130">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-130">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="2ba3c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ba3c-131">-ResourceGroupName</span></span>
<span data-ttu-id="2ba3c-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="2ba3c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ba3c-133">-ResourceId</span></span>
<span data-ttu-id="2ba3c-134">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="2ba3c-134">Resource ID of Namespace</span></span>

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

### <span data-ttu-id="2ba3c-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2ba3c-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="2ba3c-136">Список VirtualNetworkRules</span><span class="sxs-lookup"><span data-stu-id="2ba3c-136">List of VirtualNetworkRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes[]
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: VirtualNteworkRule

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba3c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ba3c-137">-Confirm</span></span>
<span data-ttu-id="2ba3c-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba3c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba3c-139">-WhatIf</span></span>
<span data-ttu-id="2ba3c-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ba3c-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba3c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba3c-142">CommonParameters</span></span>
<span data-ttu-id="2ba3c-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ba3c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2ba3c-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ba3c-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba3c-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ba3c-145">INPUTS</span></span>

### <span data-ttu-id="2ba3c-146">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="2ba3c-146">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

### <span data-ttu-id="2ba3c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2ba3c-147">System.String</span></span>

## <span data-ttu-id="2ba3c-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ba3c-148">OUTPUTS</span></span>

### <span data-ttu-id="2ba3c-149">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="2ba3c-149">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="2ba3c-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ba3c-150">NOTES</span></span>

## <span data-ttu-id="2ba3c-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ba3c-151">RELATED LINKS</span></span>