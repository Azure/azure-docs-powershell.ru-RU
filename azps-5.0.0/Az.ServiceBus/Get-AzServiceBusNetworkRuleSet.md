---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246545"
---
# <span data-ttu-id="c8aeb-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c8aeb-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="c8aeb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="c8aeb-103">Получает сведения о NetworkruleSetх концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="c8aeb-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="c8aeb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8aeb-104">SYNTAX</span></span>

### <span data-ttu-id="c8aeb-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8aeb-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8aeb-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c8aeb-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8aeb-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8aeb-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8aeb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8aeb-108">DESCRIPTION</span></span>
<span data-ttu-id="c8aeb-109">Получает сведения о NetworkruleSetх концентраторов событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="c8aeb-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="c8aeb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8aeb-110">EXAMPLES</span></span>

### <span data-ttu-id="c8aeb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8aeb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="c8aeb-112">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default;</span><span class="sxs-lookup"><span data-stu-id="c8aeb-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="c8aeb-113">Получение подробных сведений о концентраторах событий NetworkruleSet пространства имен с помощью параметров ResourceGroup и пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c8aeb-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="c8aeb-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c8aeb-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="c8aeb-115">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default;</span><span class="sxs-lookup"><span data-stu-id="c8aeb-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="c8aeb-116">Получение подробных сведений о концентраторах событий NetworkruleSet пространства имен с помощью пространства имен, которое находится в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="c8aeb-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="c8aeb-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c8aeb-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="c8aeb-118">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {1.1.1.1, Allow} VirtualNetworkRules: {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default;</span><span class="sxs-lookup"><span data-stu-id="c8aeb-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="c8aeb-119">Получение подробных сведений о концентраторах событий NetworkruleSet пространства имен с помощью идентификатора ресурса другого пространства имен</span><span class="sxs-lookup"><span data-stu-id="c8aeb-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="c8aeb-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8aeb-120">PARAMETERS</span></span>

### <span data-ttu-id="c8aeb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8aeb-121">-DefaultProfile</span></span>
<span data-ttu-id="c8aeb-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8aeb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8aeb-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c8aeb-123">-Namespace</span></span>
<span data-ttu-id="c8aeb-124">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="c8aeb-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8aeb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8aeb-125">-ResourceGroupName</span></span>
<span data-ttu-id="c8aeb-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c8aeb-126">Resource Group Name</span></span>

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

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8aeb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8aeb-127">-ResourceId</span></span>
<span data-ttu-id="c8aeb-128">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="c8aeb-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="c8aeb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8aeb-129">CommonParameters</span></span>
<span data-ttu-id="c8aeb-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8aeb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c8aeb-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8aeb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8aeb-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8aeb-132">INPUTS</span></span>

### <span data-ttu-id="c8aeb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c8aeb-133">System.String</span></span>

## <span data-ttu-id="c8aeb-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8aeb-134">OUTPUTS</span></span>

### <span data-ttu-id="c8aeb-135">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="c8aeb-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="c8aeb-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8aeb-136">NOTES</span></span>

## <span data-ttu-id="c8aeb-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8aeb-137">RELATED LINKS</span></span>