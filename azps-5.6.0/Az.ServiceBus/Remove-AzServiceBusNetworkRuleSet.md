---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: 339569d3415edadbf284f904358f889e7210267a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015987"
---
# <span data-ttu-id="39b8f-101">Remove-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="39b8f-101">Remove-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="39b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="39b8f-103">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="39b8f-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="39b8f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39b8f-104">SYNTAX</span></span>

### <span data-ttu-id="39b8f-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39b8f-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39b8f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="39b8f-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39b8f-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39b8f-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39b8f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39b8f-108">DESCRIPTION</span></span>
<span data-ttu-id="39b8f-109">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="39b8f-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="39b8f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39b8f-110">EXAMPLES</span></span>

### <span data-ttu-id="39b8f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39b8f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace1-1375
```

<span data-ttu-id="39b8f-112">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="39b8f-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1375/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="39b8f-113">Удаляет NetworkRuleSet для заданного пространства имен ServiceBus-Namespace1-1375.</span><span class="sxs-lookup"><span data-stu-id="39b8f-113">Deletes the NetworkRuleSet for the Given "ServiceBus-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="39b8f-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="39b8f-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -InputObject $result1375
```
<span data-ttu-id="39b8f-115">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="39b8f-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="39b8f-116">Удаление NetworkRuleSet с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="39b8f-116">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="39b8f-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="39b8f-117">Example 3</span></span>
```powershell
PS C:\> Remove-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace1-1375
```
<span data-ttu-id="39b8f-118">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="39b8f-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="39b8f-119">Удаляет NetworkRuleSet с помощью ResourceId пространства имен.</span><span class="sxs-lookup"><span data-stu-id="39b8f-119">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="39b8f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39b8f-120">PARAMETERS</span></span>

### <span data-ttu-id="39b8f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39b8f-121">-AsJob</span></span>
<span data-ttu-id="39b8f-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="39b8f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39b8f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b8f-123">-DefaultProfile</span></span>
<span data-ttu-id="39b8f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39b8f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39b8f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39b8f-125">-InputObject</span></span>
<span data-ttu-id="39b8f-126">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="39b8f-126">Namespace Object</span></span>

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

### <span data-ttu-id="39b8f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="39b8f-127">-Name</span></span>
<span data-ttu-id="39b8f-128">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="39b8f-128">Namespace Name</span></span>

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

### <span data-ttu-id="39b8f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39b8f-129">-PassThru</span></span>
<span data-ttu-id="39b8f-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="39b8f-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="39b8f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39b8f-131">-ResourceGroupName</span></span>
<span data-ttu-id="39b8f-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="39b8f-132">Resource Group Name</span></span>

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

### <span data-ttu-id="39b8f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39b8f-133">-ResourceId</span></span>
<span data-ttu-id="39b8f-134">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="39b8f-134">Namespace Resource Id</span></span>

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

### <span data-ttu-id="39b8f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39b8f-135">-Confirm</span></span>
<span data-ttu-id="39b8f-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39b8f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39b8f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39b8f-137">-WhatIf</span></span>
<span data-ttu-id="39b8f-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39b8f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39b8f-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="39b8f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39b8f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b8f-140">CommonParameters</span></span>
<span data-ttu-id="39b8f-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39b8f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="39b8f-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39b8f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b8f-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39b8f-143">INPUTS</span></span>

### <span data-ttu-id="39b8f-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="39b8f-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="39b8f-145">System.String</span><span class="sxs-lookup"><span data-stu-id="39b8f-145">System.String</span></span>

## <span data-ttu-id="39b8f-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39b8f-146">OUTPUTS</span></span>

### <span data-ttu-id="39b8f-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39b8f-147">System.Boolean</span></span>

## <span data-ttu-id="39b8f-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39b8f-148">NOTES</span></span>

## <span data-ttu-id="39b8f-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39b8f-149">RELATED LINKS</span></span>
