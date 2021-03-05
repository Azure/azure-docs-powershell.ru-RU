---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 3ccce01d969f6d6601d4db7383aab505923a7063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985774"
---
# <span data-ttu-id="4befb-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4befb-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="4befb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4befb-102">SYNOPSIS</span></span>
<span data-ttu-id="4befb-103">Создает коллекцию сетевых правил брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="4befb-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="4befb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4befb-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4befb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4befb-105">DESCRIPTION</span></span>
<span data-ttu-id="4befb-106">Командлет **New-AzFirewallNetworkRuleCollection** создает коллекцию правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4befb-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="4befb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4befb-107">EXAMPLES</span></span>

### <span data-ttu-id="4befb-108">Пример 1. Создание сетевого сбора с двумя правилами</span><span class="sxs-lookup"><span data-stu-id="4befb-108">Example 1: Create a network collection with two rules</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="4befb-109">В этом примере создается коллекция, которая позволит использовать весь трафик, который соответствует обоим правилам.</span><span class="sxs-lookup"><span data-stu-id="4befb-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="4befb-110">Первое правило для всего трафика UDP.</span><span class="sxs-lookup"><span data-stu-id="4befb-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="4befb-111">Второе правило для трафика TCP от 10.0.0.0 до 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4befb-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="4befb-112">Если существует еще одно собрание сетевых правил с более высоким приоритетом (меньшее число), которое также соответствует трафику, занесенму в $rule 1 или $rule 2, то вместо этого будет действовать действие коллекции правил с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="4befb-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="4befb-113">Пример 2. Добавление правила в коллекцию правил</span><span class="sxs-lookup"><span data-stu-id="4befb-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="4befb-114">В этом примере создается коллекция сетевых правил с одним правилом, а затем в коллекцию правил добавляется второе правило с использованием метода AddRule для объекта коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="4befb-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="4befb-115">Каждое имя правила в данном наборе правил должно иметь уникальное имя без учета case.</span><span class="sxs-lookup"><span data-stu-id="4befb-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="4befb-116">Пример 3. Получите правило из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="4befb-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="4befb-117">В этом примере создается коллекция сетевых правил с одним правилом, которое затем получает правило по имени и методу вызова GetRuleByName для объекта коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="4befb-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="4befb-118">Имя правила для метода GetRuleByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="4befb-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="4befb-119">Пример 4. Удаление правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="4befb-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="4befb-120">В этом примере создается коллекция правил сети с двумя правилами, а затем удаляется первое правило из коллекции правил путем вызова метода RemoveRuleByName в объекте коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="4befb-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="4befb-121">Имя правила для метода RemoveRuleByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="4befb-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="4befb-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4befb-122">PARAMETERS</span></span>

### <span data-ttu-id="4befb-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="4befb-123">-ActionType</span></span>
<span data-ttu-id="4befb-124">Указывает действие, необходимое для соответствие трафика условиям этого правила.</span><span class="sxs-lookup"><span data-stu-id="4befb-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="4befb-125">Допустимые действия: "Разрешить" или "Запретить".</span><span class="sxs-lookup"><span data-stu-id="4befb-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4befb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4befb-126">-DefaultProfile</span></span>
<span data-ttu-id="4befb-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4befb-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4befb-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4befb-128">-Name</span></span>
<span data-ttu-id="4befb-129">Имя этого сбора правил сети.</span><span class="sxs-lookup"><span data-stu-id="4befb-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="4befb-130">Имя должно быть уникальным во всем наборе правил сети.</span><span class="sxs-lookup"><span data-stu-id="4befb-130">The name must be unique across all network rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4befb-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="4befb-131">-Priority</span></span>
<span data-ttu-id="4befb-132">Определяет приоритет для этого сбора правил.</span><span class="sxs-lookup"><span data-stu-id="4befb-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="4befb-133">Приоритетом является число от 100 до 65 000.</span><span class="sxs-lookup"><span data-stu-id="4befb-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="4befb-134">Чем меньше число, тем выше приоритет.</span><span class="sxs-lookup"><span data-stu-id="4befb-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4befb-135">-Правило</span><span class="sxs-lookup"><span data-stu-id="4befb-135">-Rule</span></span>
<span data-ttu-id="4befb-136">Определяет список правил для группировки в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="4befb-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4befb-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4befb-137">-Confirm</span></span>
<span data-ttu-id="4befb-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4befb-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4befb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4befb-139">-WhatIf</span></span>
<span data-ttu-id="4befb-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4befb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4befb-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4befb-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4befb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4befb-142">CommonParameters</span></span>
<span data-ttu-id="4befb-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4befb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4befb-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4befb-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4befb-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4befb-145">INPUTS</span></span>

### <span data-ttu-id="4befb-146">Нет</span><span class="sxs-lookup"><span data-stu-id="4befb-146">None</span></span>

## <span data-ttu-id="4befb-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4befb-147">OUTPUTS</span></span>

### <span data-ttu-id="4befb-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4befb-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="4befb-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4befb-149">NOTES</span></span>

## <span data-ttu-id="4befb-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4befb-150">RELATED LINKS</span></span>

[<span data-ttu-id="4befb-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4befb-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="4befb-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4befb-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4befb-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4befb-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
