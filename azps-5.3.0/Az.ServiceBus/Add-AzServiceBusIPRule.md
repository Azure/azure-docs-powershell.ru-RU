---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: 7eb4265042083135f8306f601e2a14818aaacb06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517506"
---
# <span data-ttu-id="e8cef-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="e8cef-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="e8cef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8cef-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cef-103">Добавление одного правила IP-адреса в NetworkRuleSet данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="e8cef-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="e8cef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e8cef-104">SYNTAX</span></span>

### <span data-ttu-id="e8cef-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8cef-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8cef-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8cef-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8cef-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8cef-107">DESCRIPTION</span></span>
<span data-ttu-id="e8cef-108">Добавление одного правила IP-адреса в NetworkRuleSet данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="e8cef-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="e8cef-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e8cef-109">EXAMPLES</span></span>

### <span data-ttu-id="e8cef-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8cef-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="e8cef-111">Name : defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="e8cef-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="e8cef-112">добавьте IPRule с IpMask "11.22.33.44" и action Allow на заданное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="e8cef-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="e8cef-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e8cef-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="e8cef-114">Name : defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="e8cef-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="e8cef-115">добавьте IPRule с IpMask "11.22.33.44" и action Allow на заданное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="e8cef-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="e8cef-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8cef-116">PARAMETERS</span></span>

### <span data-ttu-id="e8cef-117">-Action</span><span class="sxs-lookup"><span data-stu-id="e8cef-117">-Action</span></span>
<span data-ttu-id="e8cef-118">Действие фильтра IP-адресов</span><span class="sxs-lookup"><span data-stu-id="e8cef-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cef-119">-DefaultProfile</span></span>
<span data-ttu-id="e8cef-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8cef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8cef-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="e8cef-121">-IpMask</span></span>
<span data-ttu-id="e8cef-122">ИД ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="e8cef-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cef-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="e8cef-123">-IpRuleObject</span></span>
<span data-ttu-id="e8cef-124">Объект конфигурации IPRule, который нужно добавить</span><span class="sxs-lookup"><span data-stu-id="e8cef-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8cef-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e8cef-125">-Name</span></span>
<span data-ttu-id="e8cef-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="e8cef-126">Namespace Name</span></span>

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

### <span data-ttu-id="e8cef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8cef-127">-ResourceGroupName</span></span>
<span data-ttu-id="e8cef-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e8cef-128">Resource Group Name</span></span>

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

### <span data-ttu-id="e8cef-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8cef-129">-Confirm</span></span>
<span data-ttu-id="e8cef-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8cef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8cef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8cef-131">-WhatIf</span></span>
<span data-ttu-id="e8cef-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8cef-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8cef-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e8cef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8cef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cef-134">CommonParameters</span></span>
<span data-ttu-id="e8cef-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8cef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e8cef-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8cef-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cef-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8cef-137">INPUTS</span></span>

### <span data-ttu-id="e8cef-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e8cef-138">System.String</span></span>

### <span data-ttu-id="e8cef-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="e8cef-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="e8cef-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8cef-140">OUTPUTS</span></span>

### <span data-ttu-id="e8cef-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="e8cef-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="e8cef-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e8cef-142">NOTES</span></span>

## <span data-ttu-id="e8cef-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8cef-143">RELATED LINKS</span></span>