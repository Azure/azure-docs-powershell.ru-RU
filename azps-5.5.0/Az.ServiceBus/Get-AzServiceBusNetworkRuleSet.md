---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNetworkRuleSet.md
ms.openlocfilehash: c9c5d3f9c8900ebfa1e11202f6105549c2180481
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242245"
---
# <span data-ttu-id="ac957-101">Get-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac957-101">Get-AzServiceBusNetworkRuleSet</span></span>

## <span data-ttu-id="ac957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac957-102">SYNOPSIS</span></span>
<span data-ttu-id="ac957-103">Получает сведения о NetworkruleSet NetworkruleSet концентратора событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="ac957-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ac957-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac957-104">SYNTAX</span></span>

### <span data-ttu-id="ac957-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac957-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac957-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ac957-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [[-ResourceGroupName] <String>] [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac957-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac957-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzServiceBusNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac957-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac957-108">DESCRIPTION</span></span>
<span data-ttu-id="ac957-109">Получает сведения о NetworkruleSet NetworkruleSet концентратора событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="ac957-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ac957-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac957-110">EXAMPLES</span></span>

### <span data-ttu-id="ac957-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac957-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="ac957-112">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="ac957-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="ac957-113">Получите сведения о NetworkruleSet NetworkruleSet пространства имен с помощью параметров ResourceGroup и Namespace.</span><span class="sxs-lookup"><span data-stu-id="ac957-113">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="ac957-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ac957-114">Example 2</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -Namespace ServiceBus-Namespace-1122
```
<span data-ttu-id="ac957-115">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="ac957-115">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-1122/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="ac957-116">Получите сведения о NetworkruleSet NetworkruleSet событий с помощью пространства имен, которая находится в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="ac957-116">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="ac957-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ac957-117">Example 3</span></span>
```powershell
PS C:\> Get-AzServiceBusNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389
```

<span data-ttu-id="ac957-118">Name : default DefaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span><span class="sxs-lookup"><span data-stu-id="ac957-118">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {1.1.1.1, Allow} VirtualNetworkRules : {/subscriptions/subscriptionId/resourcegroups/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/default, False}</span></span>

<span data-ttu-id="ac957-119">Получить сведения о NetworkruleSet событий NetworkruleSet пространства имен с помощью ИД ресурса из другого пространства имен</span><span class="sxs-lookup"><span data-stu-id="ac957-119">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="ac957-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac957-120">PARAMETERS</span></span>

### <span data-ttu-id="ac957-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac957-121">-DefaultProfile</span></span>
<span data-ttu-id="ac957-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac957-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac957-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ac957-123">-Namespace</span></span>
<span data-ttu-id="ac957-124">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="ac957-124">Namespace Name</span></span>

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

### <span data-ttu-id="ac957-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac957-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac957-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ac957-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ac957-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac957-127">-ResourceId</span></span>
<span data-ttu-id="ac957-128">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="ac957-128">Namespace Resource Id</span></span>

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

### <span data-ttu-id="ac957-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac957-129">CommonParameters</span></span>
<span data-ttu-id="ac957-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac957-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ac957-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac957-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac957-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac957-132">INPUTS</span></span>

### <span data-ttu-id="ac957-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ac957-133">System.String</span></span>

## <span data-ttu-id="ac957-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac957-134">OUTPUTS</span></span>

### <span data-ttu-id="ac957-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ac957-135">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ac957-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac957-136">NOTES</span></span>

## <span data-ttu-id="ac957-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac957-137">RELATED LINKS</span></span>