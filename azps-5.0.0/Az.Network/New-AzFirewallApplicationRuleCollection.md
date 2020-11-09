---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 3e70aa93db8a230308687ce8b03d05d80ab3ab1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248325"
---
# <span data-ttu-id="9b329-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9b329-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="9b329-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b329-102">SYNOPSIS</span></span>
<span data-ttu-id="9b329-103">Создание коллекции правил брандмауэра для приложений.</span><span class="sxs-lookup"><span data-stu-id="9b329-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="9b329-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b329-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b329-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b329-105">DESCRIPTION</span></span>
<span data-ttu-id="9b329-106">Командлет **New-AzFirewallApplicationRuleCollection** создает набор правил брандмауэра для приложения.</span><span class="sxs-lookup"><span data-stu-id="9b329-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="9b329-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b329-107">EXAMPLES</span></span>

### <span data-ttu-id="9b329-108">Пример 1: создание коллекции с одним правилом</span><span class="sxs-lookup"><span data-stu-id="9b329-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="9b329-109">В этом примере создается коллекция с одним правилом.</span><span class="sxs-lookup"><span data-stu-id="9b329-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="9b329-110">Весь трафик, совпадающий с условиями, указанными в $rule 1, будет разрешен.</span><span class="sxs-lookup"><span data-stu-id="9b329-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="9b329-111">Первое правило для всего трафика HTTPS в порте 443 от 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="9b329-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="9b329-112">Если существует другая коллекция правил приложения с более высоким приоритетом (чем меньшее число), которая также соответствует трафику, определенному в $rule 1, вместо этого будет применено действие коллекции правил с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="9b329-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="9b329-113">Пример 2: Добавление правила в коллекцию правил</span><span class="sxs-lookup"><span data-stu-id="9b329-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="9b329-114">В этом примере создается новая коллекция правил приложений с одним правилом, а затем к коллекции правил добавляется второе правило с помощью метода AddRule в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="9b329-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="9b329-115">Имя каждого правила в семействе правил должно иметь уникальное имя и не зависят от регистра.</span><span class="sxs-lookup"><span data-stu-id="9b329-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="9b329-116">Пример 3: получение правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="9b329-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="9b329-117">В этом примере создается новая коллекция правил приложений с одним правилом, а затем это правило получается по имени, а затем вызывается метод GetRuleByName в объекте Collection для правила.</span><span class="sxs-lookup"><span data-stu-id="9b329-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="9b329-118">Имя правила для метода GetRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9b329-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="9b329-119">Пример 4: Удаление правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="9b329-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="9b329-120">В этом примере создается новая коллекция правил приложений с двумя правилами, а затем из коллекции правил удаляется первое правило, которое вызывает метод RemoveRuleByName в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="9b329-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="9b329-121">Имя правила для метода RemoveRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9b329-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="9b329-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b329-122">PARAMETERS</span></span>

### <span data-ttu-id="9b329-123">-Себя</span><span class="sxs-lookup"><span data-stu-id="9b329-123">-ActionType</span></span>
<span data-ttu-id="9b329-124">Действие коллекции правил</span><span class="sxs-lookup"><span data-stu-id="9b329-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="9b329-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b329-125">-DefaultProfile</span></span>
<span data-ttu-id="9b329-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b329-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b329-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b329-127">-Name</span></span>
<span data-ttu-id="9b329-128">Задает имя этого правила приложения.</span><span class="sxs-lookup"><span data-stu-id="9b329-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="9b329-129">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="9b329-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="9b329-130">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="9b329-130">-Priority</span></span>
<span data-ttu-id="9b329-131">Задает приоритет этого правила.</span><span class="sxs-lookup"><span data-stu-id="9b329-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="9b329-132">Priority — число между 100 и 65000.</span><span class="sxs-lookup"><span data-stu-id="9b329-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="9b329-133">Чем меньше число, тем больше приоритет.</span><span class="sxs-lookup"><span data-stu-id="9b329-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="9b329-134">-Правило</span><span class="sxs-lookup"><span data-stu-id="9b329-134">-Rule</span></span>
<span data-ttu-id="9b329-135">Задает список правил для группировки в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="9b329-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b329-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b329-136">-Confirm</span></span>
<span data-ttu-id="9b329-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b329-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b329-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b329-138">-WhatIf</span></span>
<span data-ttu-id="9b329-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b329-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b329-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b329-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b329-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b329-141">CommonParameters</span></span>
<span data-ttu-id="9b329-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b329-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b329-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b329-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b329-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b329-144">INPUTS</span></span>

### <span data-ttu-id="9b329-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="9b329-145">None</span></span>

## <span data-ttu-id="9b329-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b329-146">OUTPUTS</span></span>

### <span data-ttu-id="9b329-147">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="9b329-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="9b329-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b329-148">NOTES</span></span>

## <span data-ttu-id="9b329-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b329-149">RELATED LINKS</span></span>

[<span data-ttu-id="9b329-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="9b329-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="9b329-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9b329-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="9b329-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="9b329-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)