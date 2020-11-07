---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 171431e02627177bbb62f64c9a170c02234e0c61
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902697"
---
# <span data-ttu-id="d618c-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d618c-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="d618c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d618c-102">SYNOPSIS</span></span>
<span data-ttu-id="d618c-103">Создание коллекции правил NAT в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="d618c-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="d618c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d618c-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d618c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d618c-105">DESCRIPTION</span></span>
<span data-ttu-id="d618c-106">Командлет **New-AzFirewallNatRuleCollection** создает коллекцию правил NAT межсетевого экрана.</span><span class="sxs-lookup"><span data-stu-id="d618c-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="d618c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d618c-107">EXAMPLES</span></span>

### <span data-ttu-id="d618c-108">1: создание коллекции с одним правилом</span><span class="sxs-lookup"><span data-stu-id="d618c-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="d618c-109">В этом примере создается коллекция с одним правилом.</span><span class="sxs-lookup"><span data-stu-id="d618c-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="d618c-110">Весь трафик, совпадающий с условиями, указанными в $rule 1, будет DNAT'ed на переведенный адрес и порт.</span><span class="sxs-lookup"><span data-stu-id="d618c-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="d618c-111">2. Добавление правила в коллекцию правил</span><span class="sxs-lookup"><span data-stu-id="d618c-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="d618c-112">В этом примере создается новая коллекция правил NAT с одним правилом, а затем к коллекции правил добавляется второе правило с помощью метода AddRule в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="d618c-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="d618c-113">Имя каждого правила в семействе правил должно иметь уникальное имя и не зависят от регистра.</span><span class="sxs-lookup"><span data-stu-id="d618c-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="d618c-114">3. получение правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="d618c-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="d618c-115">В этом примере создается новая коллекция правил NAT с одним правилом, а затем это правило получается по имени, а затем вызывается метод GetRuleByName в объекте Collection для правила.</span><span class="sxs-lookup"><span data-stu-id="d618c-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="d618c-116">Имя правила для метода GetRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d618c-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="d618c-117">4. Удаление правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="d618c-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="d618c-118">В этом примере создается новая коллекция правил NAT с двумя правилами, а затем из коллекции правил удаляется первое правило, вызывая метод RemoveRuleByName в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="d618c-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="d618c-119">Имя правила для метода RemoveRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="d618c-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="d618c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d618c-120">PARAMETERS</span></span>

### <span data-ttu-id="d618c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d618c-121">-DefaultProfile</span></span>
<span data-ttu-id="d618c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d618c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d618c-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d618c-123">-Name</span></span>
<span data-ttu-id="d618c-124">Указывает имя этого правила NAT.</span><span class="sxs-lookup"><span data-stu-id="d618c-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="d618c-125">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="d618c-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="d618c-126">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="d618c-126">-Priority</span></span>
<span data-ttu-id="d618c-127">Задает приоритет этого правила.</span><span class="sxs-lookup"><span data-stu-id="d618c-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="d618c-128">Priority — число между 100 и 65000.</span><span class="sxs-lookup"><span data-stu-id="d618c-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="d618c-129">Чем меньше число, тем больше приоритет.</span><span class="sxs-lookup"><span data-stu-id="d618c-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="d618c-130">-Правило</span><span class="sxs-lookup"><span data-stu-id="d618c-130">-Rule</span></span>
<span data-ttu-id="d618c-131">Задает список правил для группировки в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="d618c-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d618c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d618c-132">-Confirm</span></span>
<span data-ttu-id="d618c-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d618c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d618c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d618c-134">-WhatIf</span></span>
<span data-ttu-id="d618c-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d618c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d618c-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d618c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d618c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d618c-137">CommonParameters</span></span>
<span data-ttu-id="d618c-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d618c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d618c-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d618c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d618c-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d618c-140">INPUTS</span></span>

### <span data-ttu-id="d618c-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="d618c-141">None</span></span>

## <span data-ttu-id="d618c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d618c-142">OUTPUTS</span></span>

### <span data-ttu-id="d618c-143">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d618c-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="d618c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d618c-144">NOTES</span></span>

## <span data-ttu-id="d618c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d618c-145">RELATED LINKS</span></span>

[<span data-ttu-id="d618c-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="d618c-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="d618c-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d618c-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="d618c-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d618c-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
