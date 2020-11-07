---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 959fcab661139a1cacae46a315db0eaa93f0c09e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730859"
---
# <span data-ttu-id="dd9d6-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="dd9d6-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="dd9d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="dd9d6-103">Добавление одного IPrule к NetworkRuleSet для указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="dd9d6-103">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="dd9d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd9d6-104">SYNTAX</span></span>

### <span data-ttu-id="dd9d6-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd9d6-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd9d6-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd9d6-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd9d6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd9d6-107">DESCRIPTION</span></span>
<span data-ttu-id="dd9d6-108">Добавление одного IPrule к NetworkRuleSet для указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="dd9d6-108">Add a single IPrule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="dd9d6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd9d6-109">EXAMPLES</span></span>

### <span data-ttu-id="dd9d6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd9d6-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="dd9d6-111">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="dd9d6-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="dd9d6-112">Добавьте IPRule с IpMask "11.22.33.44" и разрешенными действиями для данного namesapce.</span><span class="sxs-lookup"><span data-stu-id="dd9d6-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namesapce.</span></span>

### <span data-ttu-id="dd9d6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dd9d6-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="dd9d6-114">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type: Microsoft. Eventhub/Namespaces/NetworkRuleSet IpRules: {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="dd9d6-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="dd9d6-115">Добавьте IPRule с IpMask "11.22.33.44" и разрешенными действиями для данного namesapce.</span><span class="sxs-lookup"><span data-stu-id="dd9d6-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namesapce.</span></span>

## <span data-ttu-id="dd9d6-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd9d6-116">PARAMETERS</span></span>

### <span data-ttu-id="dd9d6-117">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="dd9d6-117">-Action</span></span>
<span data-ttu-id="dd9d6-118">Действие фильтра IP</span><span class="sxs-lookup"><span data-stu-id="dd9d6-118">The IP Filter Action</span></span>

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

### <span data-ttu-id="dd9d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd9d6-119">-DefaultProfile</span></span>
<span data-ttu-id="dd9d6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd9d6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd9d6-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="dd9d6-121">-IpMask</span></span>
<span data-ttu-id="dd9d6-122">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="dd9d6-122">Subnet Resource ID</span></span>

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

### <span data-ttu-id="dd9d6-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="dd9d6-123">-IpRuleObject</span></span>
<span data-ttu-id="dd9d6-124">Объект конфигурации IPRule, который нужно добавить</span><span class="sxs-lookup"><span data-stu-id="dd9d6-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd9d6-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd9d6-125">-Name</span></span>
<span data-ttu-id="dd9d6-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="dd9d6-126">Namespace Name</span></span>

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

### <span data-ttu-id="dd9d6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd9d6-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd9d6-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dd9d6-128">Resource Group Name</span></span>

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

### <span data-ttu-id="dd9d6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd9d6-129">-Confirm</span></span>
<span data-ttu-id="dd9d6-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd9d6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd9d6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd9d6-131">-WhatIf</span></span>
<span data-ttu-id="dd9d6-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd9d6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd9d6-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd9d6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd9d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd9d6-134">CommonParameters</span></span>
<span data-ttu-id="dd9d6-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd9d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dd9d6-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd9d6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd9d6-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd9d6-137">INPUTS</span></span>

### <span data-ttu-id="dd9d6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dd9d6-138">System.String</span></span>

### <span data-ttu-id="dd9d6-139">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="dd9d6-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="dd9d6-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd9d6-140">OUTPUTS</span></span>

### <span data-ttu-id="dd9d6-141">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="dd9d6-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="dd9d6-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd9d6-142">NOTES</span></span>

## <span data-ttu-id="dd9d6-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd9d6-143">RELATED LINKS</span></span>
