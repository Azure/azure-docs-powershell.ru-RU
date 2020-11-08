---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: 16643ba0060f4f242f8c36ff16737a03aec7507b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073264"
---
# <span data-ttu-id="4671d-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4671d-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="4671d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4671d-102">SYNOPSIS</span></span>
<span data-ttu-id="4671d-103">Создание сетевого семейства брандмауэра Azure для сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="4671d-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="4671d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4671d-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4671d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4671d-105">DESCRIPTION</span></span>
<span data-ttu-id="4671d-106">Командлет **New-AzFirewallNetworkRuleCollection** создает набор правил сетевого брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4671d-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="4671d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4671d-107">EXAMPLES</span></span>

### <span data-ttu-id="4671d-108">1: создание сетевого семейства с двумя правилами</span><span class="sxs-lookup"><span data-stu-id="4671d-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="4671d-109">В этом примере создается коллекция, которая обеспечивает весь трафик, совпадающий с одним из двух правил.</span><span class="sxs-lookup"><span data-stu-id="4671d-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="4671d-110">Первое правило для всего UDP-трафика.</span><span class="sxs-lookup"><span data-stu-id="4671d-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="4671d-111">Второе правило — трафик TCP от 10.0.0.0 до 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="4671d-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="4671d-112">Если еще есть другая коллекция сетевых правил с более высоким приоритетом (меньшее число), которая также соответствует трафику, определенному в $rule 1 или $rule 2, вместо этого будет применено действие коллекции правил с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="4671d-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="4671d-113">2. Добавление правила в коллекцию правил</span><span class="sxs-lookup"><span data-stu-id="4671d-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="4671d-114">В этом примере создается новая коллекция сетевых правил с одним правилом, а затем к коллекции правил добавляется второе правило с помощью метода AddRule в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="4671d-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="4671d-115">Имя каждого правила в семействе правил должно иметь уникальное имя и не зависят от регистра.</span><span class="sxs-lookup"><span data-stu-id="4671d-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="4671d-116">3. получение правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="4671d-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="4671d-117">В этом примере создается новая коллекция сетевых правил с одним правилом, а затем это правило получается по имени и вызывается метод GetRuleByName для объекта коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="4671d-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="4671d-118">Имя правила для метода GetRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="4671d-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="4671d-119">4. Удаление правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="4671d-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="4671d-120">В этом примере создается новая коллекция сетевых правил с двумя правилами, а затем из коллекции правил удаляется первое правило, которое вызывает метод RemoveRuleByName в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="4671d-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="4671d-121">Имя правила для метода RemoveRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="4671d-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="4671d-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4671d-122">PARAMETERS</span></span>

### <span data-ttu-id="4671d-123">-Себя</span><span class="sxs-lookup"><span data-stu-id="4671d-123">-ActionType</span></span>
<span data-ttu-id="4671d-124">Задает действие, которое будет выполняться для условий соответствия трафика для этого правила.</span><span class="sxs-lookup"><span data-stu-id="4671d-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="4671d-125">Принятые действия: "разрешить" или "запретить".</span><span class="sxs-lookup"><span data-stu-id="4671d-125">Accepted actions are "Allow" or "Deny".</span></span>

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

### <span data-ttu-id="4671d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4671d-126">-DefaultProfile</span></span>
<span data-ttu-id="4671d-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4671d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4671d-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4671d-128">-Name</span></span>
<span data-ttu-id="4671d-129">Указывает имя этой коллекции сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="4671d-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="4671d-130">Имя должно быть уникальным для всех семейств сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="4671d-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="4671d-131">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="4671d-131">-Priority</span></span>
<span data-ttu-id="4671d-132">Задает приоритет этой коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="4671d-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="4671d-133">Priority — число между 100 и 65000.</span><span class="sxs-lookup"><span data-stu-id="4671d-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="4671d-134">Чем меньше число, тем выше приоритет.</span><span class="sxs-lookup"><span data-stu-id="4671d-134">The smaller the number, the higher the priority.</span></span>

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

### <span data-ttu-id="4671d-135">-Правило</span><span class="sxs-lookup"><span data-stu-id="4671d-135">-Rule</span></span>
<span data-ttu-id="4671d-136">Задает список правил для группировки в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="4671d-136">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="4671d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4671d-137">-Confirm</span></span>
<span data-ttu-id="4671d-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4671d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4671d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4671d-139">-WhatIf</span></span>
<span data-ttu-id="4671d-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4671d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4671d-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4671d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4671d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4671d-142">CommonParameters</span></span>
<span data-ttu-id="4671d-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4671d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4671d-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4671d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4671d-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4671d-145">INPUTS</span></span>

### <span data-ttu-id="4671d-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="4671d-146">None</span></span>

## <span data-ttu-id="4671d-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4671d-147">OUTPUTS</span></span>

### <span data-ttu-id="4671d-148">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4671d-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="4671d-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="4671d-149">NOTES</span></span>

## <span data-ttu-id="4671d-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4671d-150">RELATED LINKS</span></span>

[<span data-ttu-id="4671d-151">New-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4671d-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="4671d-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4671d-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="4671d-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4671d-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
