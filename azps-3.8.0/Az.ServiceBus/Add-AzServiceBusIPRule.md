---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: 7eb4265042083135f8306f601e2a14818aaacb06
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073758"
---
# <span data-ttu-id="2bcae-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="2bcae-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="2bcae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2bcae-102">SYNOPSIS</span></span>
<span data-ttu-id="2bcae-103">Добавление отдельного правила IP-адреса в NetworkRuleSet указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="2bcae-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="2bcae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2bcae-104">SYNTAX</span></span>

### <span data-ttu-id="2bcae-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2bcae-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bcae-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bcae-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2bcae-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bcae-107">DESCRIPTION</span></span>
<span data-ttu-id="2bcae-108">Добавление отдельного правила IP-адреса в NetworkRuleSet указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="2bcae-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="2bcae-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2bcae-109">EXAMPLES</span></span>

### <span data-ttu-id="2bcae-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2bcae-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="2bcae-111">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="2bcae-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="2bcae-112">Добавьте IPRule с IpMask "11.22.33.44" и действие разрешено решение заданное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="2bcae-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="2bcae-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2bcae-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="2bcae-114">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="2bcae-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="2bcae-115">Добавьте IPRule с IpMask "11.22.33.44" и действие разрешено решение заданное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="2bcae-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="2bcae-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2bcae-116">PARAMETERS</span></span>

### <span data-ttu-id="2bcae-117">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="2bcae-117">-Action</span></span>
<span data-ttu-id="2bcae-118">Действие фильтра IP</span><span class="sxs-lookup"><span data-stu-id="2bcae-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="2bcae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bcae-119">-DefaultProfile</span></span>
<span data-ttu-id="2bcae-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bcae-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="2bcae-121">-IpMask</span></span>
<span data-ttu-id="2bcae-122">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="2bcae-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="2bcae-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="2bcae-123">-IpRuleObject</span></span>
<span data-ttu-id="2bcae-124">Объект конфигурации IPRule, который нужно добавить</span><span class="sxs-lookup"><span data-stu-id="2bcae-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="2bcae-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2bcae-125">-Name</span></span>
<span data-ttu-id="2bcae-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="2bcae-126">Namespace Name</span></span>

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

### <span data-ttu-id="2bcae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bcae-127">-ResourceGroupName</span></span>
<span data-ttu-id="2bcae-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2bcae-128">Resource Group Name</span></span>

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

### <span data-ttu-id="2bcae-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2bcae-129">-Confirm</span></span>
<span data-ttu-id="2bcae-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2bcae-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bcae-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bcae-131">-WhatIf</span></span>
<span data-ttu-id="2bcae-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2bcae-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bcae-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2bcae-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bcae-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bcae-134">CommonParameters</span></span>
<span data-ttu-id="2bcae-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2bcae-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2bcae-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bcae-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bcae-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2bcae-137">INPUTS</span></span>

### <span data-ttu-id="2bcae-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2bcae-138">System.String</span></span>

### <span data-ttu-id="2bcae-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="2bcae-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="2bcae-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bcae-140">OUTPUTS</span></span>

### <span data-ttu-id="2bcae-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="2bcae-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="2bcae-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2bcae-142">NOTES</span></span>

## <span data-ttu-id="2bcae-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bcae-143">RELATED LINKS</span></span>