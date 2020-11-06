---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
ms.openlocfilehash: 79ead5ac618b4631c3ec790156fe1a75e4169882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565857"
---
# <span data-ttu-id="381f9-101">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="381f9-101">New-AzureRmFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="381f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="381f9-102">SYNOPSIS</span></span>
<span data-ttu-id="381f9-103">Создание сетевого семейства брандмауэра Azure для сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="381f9-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="381f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="381f9-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="381f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="381f9-105">DESCRIPTION</span></span>
<span data-ttu-id="381f9-106">Командлет **New-AzureRmFirewallNetworkRuleCollection** создает набор правил сетевого брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="381f9-106">The **New-AzureRmFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="381f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="381f9-107">EXAMPLES</span></span>

### <span data-ttu-id="381f9-108">1: создание сетевого семейства с двумя правилами</span><span class="sxs-lookup"><span data-stu-id="381f9-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzureRmFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="381f9-109">В этом примере создается коллекция, которая обеспечивает весь трафик, совпадающий с одним из двух правил.</span><span class="sxs-lookup"><span data-stu-id="381f9-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="381f9-110">Первое правило для всего UDP-трафика.</span><span class="sxs-lookup"><span data-stu-id="381f9-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="381f9-111">Второе правило — трафик TCP от 10.0.0.0 до 60.1.5.0:4040.</span><span class="sxs-lookup"><span data-stu-id="381f9-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="381f9-112">Если еще есть другая коллекция сетевых правил с более высоким приоритетом (меньшее число), которая также соответствует трафику, определенному в $rule 1 или $rule 2, вместо этого будет применено действие коллекции правил с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="381f9-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="381f9-113">2. Добавление правила в коллекцию правил</span><span class="sxs-lookup"><span data-stu-id="381f9-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="381f9-114">В этом примере создается новая коллекция сетевых правил с одним правилом, а затем к коллекции правил добавляется второе правило с помощью метода AddRule в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="381f9-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="381f9-115">Имя каждого правила в семействе правил должно иметь уникальное имя и не зависят от регистра.</span><span class="sxs-lookup"><span data-stu-id="381f9-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="381f9-116">3. получение правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="381f9-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="381f9-117">В этом примере создается новая коллекция сетевых правил с одним правилом, а затем это правило получается по имени и вызывается метод GetRuleByName для объекта коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="381f9-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="381f9-118">Имя правила для метода GetRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="381f9-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="381f9-119">4. Удаление правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="381f9-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="381f9-120">В этом примере создается новая коллекция сетевых правил с двумя правилами, а затем из коллекции правил удаляется первое правило, которое вызывает метод RemoveRuleByName в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="381f9-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="381f9-121">Имя правила для метода RemoveRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="381f9-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="381f9-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="381f9-122">PARAMETERS</span></span>

### <span data-ttu-id="381f9-123">-Себя</span><span class="sxs-lookup"><span data-stu-id="381f9-123">-ActionType</span></span>
<span data-ttu-id="381f9-124">Задает действие, которое будет выполняться для условий соответствия трафика для этого правила.</span><span class="sxs-lookup"><span data-stu-id="381f9-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="381f9-125">Принятые действия: "разрешить" или "запретить".</span><span class="sxs-lookup"><span data-stu-id="381f9-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381f9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="381f9-126">-DefaultProfile</span></span>
<span data-ttu-id="381f9-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="381f9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381f9-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="381f9-128">-Name</span></span>
<span data-ttu-id="381f9-129">Указывает имя этой коллекции сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="381f9-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="381f9-130">Имя должно быть уникальным для всех семейств сетевых правил.</span><span class="sxs-lookup"><span data-stu-id="381f9-130">The name must be unique across all network rule collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381f9-131">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="381f9-131">-Priority</span></span>
<span data-ttu-id="381f9-132">Задает приоритет этой коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="381f9-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="381f9-133">Priority — число между 100 и 65000.</span><span class="sxs-lookup"><span data-stu-id="381f9-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="381f9-134">Чем меньше число, тем выше приоритет.</span><span class="sxs-lookup"><span data-stu-id="381f9-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381f9-135">-Правило</span><span class="sxs-lookup"><span data-stu-id="381f9-135">-Rule</span></span>
<span data-ttu-id="381f9-136">Задает список правил для группировки в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="381f9-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381f9-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="381f9-137">-Confirm</span></span>
<span data-ttu-id="381f9-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="381f9-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381f9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="381f9-139">-WhatIf</span></span>
<span data-ttu-id="381f9-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="381f9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="381f9-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="381f9-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="381f9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381f9-142">CommonParameters</span></span>
<span data-ttu-id="381f9-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="381f9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381f9-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="381f9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381f9-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="381f9-145">INPUTS</span></span>

### <span data-ttu-id="381f9-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="381f9-146">None</span></span>
<span data-ttu-id="381f9-147">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="381f9-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="381f9-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="381f9-148">OUTPUTS</span></span>

### <span data-ttu-id="381f9-149">Microsoft. Azure. Commands. Network. Models. PSFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="381f9-149">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="381f9-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="381f9-150">NOTES</span></span>

## <span data-ttu-id="381f9-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="381f9-151">RELATED LINKS</span></span>

[<span data-ttu-id="381f9-152">New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="381f9-152">New-AzureRmFirewallNetworkRule</span></span>](./New-AzureRmFirewallNetworkRule.md)

[<span data-ttu-id="381f9-153">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="381f9-153">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="381f9-154">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="381f9-154">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
