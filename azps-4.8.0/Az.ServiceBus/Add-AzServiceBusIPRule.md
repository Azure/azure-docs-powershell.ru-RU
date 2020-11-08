---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/add-azservicebusiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Add-AzServiceBusIPRule.md
ms.openlocfilehash: 7eb4265042083135f8306f601e2a14818aaacb06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078742"
---
# <span data-ttu-id="a07d0-101">Add-AzServiceBusIPRule</span><span class="sxs-lookup"><span data-stu-id="a07d0-101">Add-AzServiceBusIPRule</span></span>

## <span data-ttu-id="a07d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a07d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a07d0-103">Добавление отдельного правила IP-адреса в NetworkRuleSet указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="a07d0-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="a07d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a07d0-104">SYNTAX</span></span>

### <span data-ttu-id="a07d0-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a07d0-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a07d0-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a07d0-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzServiceBusIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a07d0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a07d0-107">DESCRIPTION</span></span>
<span data-ttu-id="a07d0-108">Добавление отдельного правила IP-адреса в NetworkRuleSet указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="a07d0-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="a07d0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a07d0-109">EXAMPLES</span></span>

### <span data-ttu-id="a07d0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a07d0-110">Example 1</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="a07d0-111">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="a07d0-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="a07d0-112">Добавьте IPRule с IpMask "11.22.33.44" и действие разрешено решение заданное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="a07d0-112">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

### <span data-ttu-id="a07d0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a07d0-113">Example 2</span></span>
```powershell
PS C:\> Add-AzServiceBusIPRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -IpRuleObject $ipruleObject
```
<span data-ttu-id="a07d0-114">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type: Microsoft. ServiceBus/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="a07d0-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.ServiceBus/namespaces/ServiceBus-Namespace-2389/networkRuleSets/default Type                : Microsoft.ServiceBus/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="a07d0-115">Добавьте IPRule с IpMask "11.22.33.44" и действие разрешено решение заданное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="a07d0-115">add the IPRule with IpMask "11.22.33.44" and Action Allow fro the given namespace.</span></span>

## <span data-ttu-id="a07d0-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a07d0-116">PARAMETERS</span></span>

### <span data-ttu-id="a07d0-117">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="a07d0-117">-Action</span></span>
<span data-ttu-id="a07d0-118">Действие фильтра IP</span><span class="sxs-lookup"><span data-stu-id="a07d0-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="a07d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07d0-119">-DefaultProfile</span></span>
<span data-ttu-id="a07d0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a07d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a07d0-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="a07d0-121">-IpMask</span></span>
<span data-ttu-id="a07d0-122">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="a07d0-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="a07d0-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="a07d0-123">-IpRuleObject</span></span>
<span data-ttu-id="a07d0-124">Объект конфигурации IPRule, который нужно добавить</span><span class="sxs-lookup"><span data-stu-id="a07d0-124">IPRule Configuration Object to be added</span></span>

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

### <span data-ttu-id="a07d0-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a07d0-125">-Name</span></span>
<span data-ttu-id="a07d0-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="a07d0-126">Namespace Name</span></span>

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

### <span data-ttu-id="a07d0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a07d0-127">-ResourceGroupName</span></span>
<span data-ttu-id="a07d0-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a07d0-128">Resource Group Name</span></span>

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

### <span data-ttu-id="a07d0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a07d0-129">-Confirm</span></span>
<span data-ttu-id="a07d0-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a07d0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a07d0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a07d0-131">-WhatIf</span></span>
<span data-ttu-id="a07d0-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a07d0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a07d0-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a07d0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a07d0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07d0-134">CommonParameters</span></span>
<span data-ttu-id="a07d0-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a07d0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a07d0-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a07d0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07d0-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a07d0-137">INPUTS</span></span>

### <span data-ttu-id="a07d0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a07d0-138">System.String</span></span>

### <span data-ttu-id="a07d0-139">Microsoft. Azure. Commands. ServiceBus. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="a07d0-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="a07d0-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a07d0-140">OUTPUTS</span></span>

### <span data-ttu-id="a07d0-141">Microsoft. Azure. Commands. ServiceBus. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="a07d0-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="a07d0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a07d0-142">NOTES</span></span>

## <span data-ttu-id="a07d0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a07d0-143">RELATED LINKS</span></span>