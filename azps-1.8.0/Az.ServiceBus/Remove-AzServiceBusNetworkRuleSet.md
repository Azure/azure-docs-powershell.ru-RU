---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: df8e85505a7aa62b883ecdc0536f9b3cd1352109
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729162"
---
# <span data-ttu-id="42825-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="42825-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="42825-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42825-102">SYNOPSIS</span></span>
<span data-ttu-id="42825-103">Удаляет NetwrokRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="42825-103">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="42825-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42825-104">SYNTAX</span></span>

### <span data-ttu-id="42825-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42825-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42825-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="42825-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42825-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42825-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42825-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42825-108">DESCRIPTION</span></span>
<span data-ttu-id="42825-109">Удаляет NetwrokRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="42825-109">Removes the NetwrokRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="42825-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42825-110">EXAMPLES</span></span>

### <span data-ttu-id="42825-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42825-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="42825-112">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="42825-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="42825-113">Удаляет NetwrokRuleSet для заданных "ServiceBus-Namespace1-1375" namesapce</span><span class="sxs-lookup"><span data-stu-id="42825-113">Deletes the NetwrokRuleSet for the Given "ServiceBus-Namespace1-1375" namesapce</span></span> 

### <span data-ttu-id="42825-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="42825-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="42825-115">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="42825-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="42825-116">Удаление NetwrokRuleSet с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="42825-116">Deletes the NetwrokRuleSet using InputObject</span></span> 

### <span data-ttu-id="42825-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="42825-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="42825-118">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="42825-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="42825-119">Удаляет NetwrokRuleSet, использующий ResourceId из Namepsace</span><span class="sxs-lookup"><span data-stu-id="42825-119">Deletes the NetwrokRuleSet using ResourceId of the Namepsace</span></span>


## <span data-ttu-id="42825-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42825-120">PARAMETERS</span></span>

### <span data-ttu-id="42825-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42825-121">-AsJob</span></span>
<span data-ttu-id="42825-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="42825-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42825-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42825-123">-DefaultProfile</span></span>
<span data-ttu-id="42825-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42825-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42825-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42825-125">-InputObject</span></span>
<span data-ttu-id="42825-126">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="42825-126">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42825-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42825-127">-Name</span></span>
<span data-ttu-id="42825-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="42825-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42825-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42825-129">-PassThru</span></span>
<span data-ttu-id="42825-130">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="42825-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42825-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42825-131">-ResourceGroupName</span></span>
<span data-ttu-id="42825-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="42825-132">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42825-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42825-133">-ResourceId</span></span>
<span data-ttu-id="42825-134">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="42825-134">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42825-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42825-135">-Confirm</span></span>
<span data-ttu-id="42825-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42825-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42825-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42825-137">-WhatIf</span></span>
<span data-ttu-id="42825-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42825-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42825-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42825-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42825-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42825-140">CommonParameters</span></span>
<span data-ttu-id="42825-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42825-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="42825-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42825-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42825-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42825-143">INPUTS</span></span>

### <span data-ttu-id="42825-144">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="42825-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="42825-145">System. String</span><span class="sxs-lookup"><span data-stu-id="42825-145">System.String</span></span>

## <span data-ttu-id="42825-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42825-146">OUTPUTS</span></span>

### <span data-ttu-id="42825-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42825-147">System.Boolean</span></span>

## <span data-ttu-id="42825-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="42825-148">NOTES</span></span>

## <span data-ttu-id="42825-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42825-149">RELATED LINKS</span></span>
