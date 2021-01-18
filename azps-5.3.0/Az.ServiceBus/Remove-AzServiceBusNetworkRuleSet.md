---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 6c803f399bf88c6e4887441ec9f9bd50c058361b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517393"
---
# <span data-ttu-id="8916c-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8916c-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="8916c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8916c-102">SYNOPSIS</span></span>
<span data-ttu-id="8916c-103">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8916c-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="8916c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8916c-104">SYNTAX</span></span>

### <span data-ttu-id="8916c-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8916c-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8916c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8916c-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8916c-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8916c-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8916c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8916c-108">DESCRIPTION</span></span>
<span data-ttu-id="8916c-109">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8916c-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="8916c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8916c-110">EXAMPLES</span></span>

### <span data-ttu-id="8916c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8916c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="8916c-112">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="8916c-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="8916c-113">Удаляет NetworkRuleSet для заданного пространства имен ServiceBus-Namespace1-1375.</span><span class="sxs-lookup"><span data-stu-id="8916c-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="8916c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8916c-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="8916c-115">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="8916c-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="8916c-116">Удаление NetworkRuleSet с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="8916c-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="8916c-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8916c-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="8916c-118">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="8916c-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="8916c-119">Удаление NetworkRuleSet с помощью ResourceId пространства имен</span><span class="sxs-lookup"><span data-stu-id="8916c-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="8916c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8916c-120">PARAMETERS</span></span>

### <span data-ttu-id="8916c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8916c-121">-AsJob</span></span>
<span data-ttu-id="8916c-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8916c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8916c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8916c-123">-DefaultProfile</span></span>
<span data-ttu-id="8916c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8916c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8916c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8916c-125">-InputObject</span></span>
<span data-ttu-id="8916c-126">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="8916c-126">Namespace Object</span></span>

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

### <span data-ttu-id="8916c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8916c-127">-Name</span></span>
<span data-ttu-id="8916c-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="8916c-128">Namespace Name</span></span>

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

### <span data-ttu-id="8916c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8916c-129">-PassThru</span></span>
<span data-ttu-id="8916c-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8916c-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8916c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8916c-131">-ResourceGroupName</span></span>
<span data-ttu-id="8916c-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8916c-132">Resource Group Name</span></span>

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

### <span data-ttu-id="8916c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8916c-133">-ResourceId</span></span>
<span data-ttu-id="8916c-134">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="8916c-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="8916c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8916c-135">-Confirm</span></span>
<span data-ttu-id="8916c-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8916c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8916c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8916c-137">-WhatIf</span></span>
<span data-ttu-id="8916c-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8916c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8916c-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8916c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8916c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8916c-140">CommonParameters</span></span>
<span data-ttu-id="8916c-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8916c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8916c-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8916c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8916c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8916c-143">INPUTS</span></span>

### <span data-ttu-id="8916c-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="8916c-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="8916c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8916c-145">System.String</span></span>

## <span data-ttu-id="8916c-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8916c-146">OUTPUTS</span></span>

### <span data-ttu-id="8916c-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8916c-147">System.Boolean</span></span>

## <span data-ttu-id="8916c-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8916c-148">NOTES</span></span>

## <span data-ttu-id="8916c-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8916c-149">RELATED LINKS</span></span>
