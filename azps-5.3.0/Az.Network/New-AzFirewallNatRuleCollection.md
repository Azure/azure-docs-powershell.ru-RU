---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 4ba57fd922319eb2be6ba001c723b3e668bce59e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506939"
---
# <span data-ttu-id="804c6-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="804c6-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="804c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="804c6-102">SYNOPSIS</span></span>
<span data-ttu-id="804c6-103">Создает набор правил NAT брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="804c6-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="804c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="804c6-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="804c6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="804c6-105">DESCRIPTION</span></span>
<span data-ttu-id="804c6-106">С **помощью cmdlet New-AzFirewallNatRuleCollection** создается коллекция правил NAT брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="804c6-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="804c6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="804c6-107">EXAMPLES</span></span>

### <span data-ttu-id="804c6-108">Пример 1. Создание коллекции с одним правилом</span><span class="sxs-lookup"><span data-stu-id="804c6-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="804c6-109">В этом примере создается коллекция с одним правилом.</span><span class="sxs-lookup"><span data-stu-id="804c6-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="804c6-110">Весь трафик, который соответствует условиям, зазначимых $rule 1, будет переведен на переведенный адрес и порт.</span><span class="sxs-lookup"><span data-stu-id="804c6-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="804c6-111">Пример 2. Добавление правила в коллекцию правил</span><span class="sxs-lookup"><span data-stu-id="804c6-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="804c6-112">В этом примере создается новое коллекцию правил NAT с одним правилом, а затем в коллекцию правил добавляется второе правило с использованием метода AddRule для объекта коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="804c6-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="804c6-113">Имя каждого правила в данном наборе правил должно иметь уникальное имя без учета case.</span><span class="sxs-lookup"><span data-stu-id="804c6-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="804c6-114">Пример 3. Получите правило из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="804c6-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="804c6-115">В этом примере создается коллекция правил NAT с одним правилом, которое затем получает правило по имени, методу вызова GetRuleByName для объекта коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="804c6-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="804c6-116">Имя правила для метода GetRuleByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="804c6-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="804c6-117">Пример 4. Удаление правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="804c6-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="804c6-118">В этом примере создается новое коллекцию правил NAT с двумя правилами, а затем удаляется первое правило из коллекции правил путем вызова метода RemoveRuleByName для объекта коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="804c6-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="804c6-119">Имя правила для метода RemoveRuleByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="804c6-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="804c6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="804c6-120">PARAMETERS</span></span>

### <span data-ttu-id="804c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804c6-121">-DefaultProfile</span></span>
<span data-ttu-id="804c6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="804c6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="804c6-123">-Name</span><span class="sxs-lookup"><span data-stu-id="804c6-123">-Name</span></span>
<span data-ttu-id="804c6-124">Указывает имя правила NAT.</span><span class="sxs-lookup"><span data-stu-id="804c6-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="804c6-125">Имя должно быть уникальным в наборе правил.</span><span class="sxs-lookup"><span data-stu-id="804c6-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="804c6-126">-Priority</span><span class="sxs-lookup"><span data-stu-id="804c6-126">-Priority</span></span>
<span data-ttu-id="804c6-127">Определяет приоритет этого правила.</span><span class="sxs-lookup"><span data-stu-id="804c6-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="804c6-128">Приоритет — это число от 100 до 65 000.</span><span class="sxs-lookup"><span data-stu-id="804c6-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="804c6-129">Чем меньше число, тем выше приоритет.</span><span class="sxs-lookup"><span data-stu-id="804c6-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="804c6-130">-Правило</span><span class="sxs-lookup"><span data-stu-id="804c6-130">-Rule</span></span>
<span data-ttu-id="804c6-131">Определяет список правил для группировки в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="804c6-131">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="804c6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="804c6-132">-Confirm</span></span>
<span data-ttu-id="804c6-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="804c6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="804c6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="804c6-134">-WhatIf</span></span>
<span data-ttu-id="804c6-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="804c6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="804c6-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="804c6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="804c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804c6-137">CommonParameters</span></span>
<span data-ttu-id="804c6-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="804c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804c6-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="804c6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804c6-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="804c6-140">INPUTS</span></span>

### <span data-ttu-id="804c6-141">Нет</span><span class="sxs-lookup"><span data-stu-id="804c6-141">None</span></span>

## <span data-ttu-id="804c6-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="804c6-142">OUTPUTS</span></span>

### <span data-ttu-id="804c6-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="804c6-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="804c6-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="804c6-144">NOTES</span></span>

## <span data-ttu-id="804c6-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="804c6-145">RELATED LINKS</span></span>

[<span data-ttu-id="804c6-146">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="804c6-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="804c6-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="804c6-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="804c6-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="804c6-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
