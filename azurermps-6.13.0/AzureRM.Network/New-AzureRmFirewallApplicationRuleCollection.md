---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
ms.openlocfilehash: e5fbad2b63213af972260948439984754e9eaa3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734615"
---
# <span data-ttu-id="5d826-101">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5d826-101">New-AzureRmFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="5d826-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d826-102">SYNOPSIS</span></span>
<span data-ttu-id="5d826-103">Создание коллекции правил брандмауэра для приложений.</span><span class="sxs-lookup"><span data-stu-id="5d826-103">Creates a collection of Firewall application rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d826-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d826-104">SYNTAX</span></span>

```
New-AzureRmFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d826-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d826-105">DESCRIPTION</span></span>
<span data-ttu-id="5d826-106">Командлет **New-AzureRmFirewallApplicationRuleCollection** создает набор правил брандмауэра для приложения.</span><span class="sxs-lookup"><span data-stu-id="5d826-106">The **New-AzureRmFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="5d826-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d826-107">EXAMPLES</span></span>

### <span data-ttu-id="5d826-108">1: создание коллекции с одним правилом</span><span class="sxs-lookup"><span data-stu-id="5d826-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="5d826-109">В этом примере создается коллекция с одним правилом.</span><span class="sxs-lookup"><span data-stu-id="5d826-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="5d826-110">Весь трафик, совпадающий с условиями, указанными в $rule 1, будет разрешен.</span><span class="sxs-lookup"><span data-stu-id="5d826-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="5d826-111">Первое правило для всего трафика HTTPS в порте 443 от 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="5d826-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="5d826-112">Если существует другая коллекция правил приложения с более высоким приоритетом (чем меньшее число), которая также соответствует трафику, определенному в $rule 1, вместо этого будет применено действие коллекции правил с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="5d826-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="5d826-113">2. Добавление правила в коллекцию правил</span><span class="sxs-lookup"><span data-stu-id="5d826-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="5d826-114">В этом примере создается новая коллекция правил приложений с одним правилом, а затем к коллекции правил добавляется второе правило с помощью метода AddRule в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="5d826-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="5d826-115">Имя каждого правила в семействе правил должно иметь уникальное имя и не зависят от регистра.</span><span class="sxs-lookup"><span data-stu-id="5d826-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="5d826-116">3. получение правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="5d826-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="5d826-117">В этом примере создается новая коллекция правил приложений с одним правилом, а затем это правило получается по имени, а затем вызывается метод GetRuleByName в объекте Collection для правила.</span><span class="sxs-lookup"><span data-stu-id="5d826-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="5d826-118">Имя правила для метода GetRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="5d826-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="5d826-119">4. Удаление правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="5d826-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="5d826-120">В этом примере создается новая коллекция правил приложений с двумя правилами, а затем из коллекции правил удаляется первое правило, которое вызывает метод RemoveRuleByName в объекте Collection.</span><span class="sxs-lookup"><span data-stu-id="5d826-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="5d826-121">Имя правила для метода RemoveRuleByName не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="5d826-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="5d826-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d826-122">PARAMETERS</span></span>

### <span data-ttu-id="5d826-123">-Себя</span><span class="sxs-lookup"><span data-stu-id="5d826-123">-ActionType</span></span>
<span data-ttu-id="5d826-124">Действие коллекции правил</span><span class="sxs-lookup"><span data-stu-id="5d826-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="5d826-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d826-125">-DefaultProfile</span></span>
<span data-ttu-id="5d826-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d826-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d826-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d826-127">-Name</span></span>
<span data-ttu-id="5d826-128">Задает имя этого правила приложения.</span><span class="sxs-lookup"><span data-stu-id="5d826-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="5d826-129">Имя должно быть уникальным в пределах коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="5d826-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="5d826-130">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="5d826-130">-Priority</span></span>
<span data-ttu-id="5d826-131">Задает приоритет этого правила.</span><span class="sxs-lookup"><span data-stu-id="5d826-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="5d826-132">Priority — число между 100 и 65000.</span><span class="sxs-lookup"><span data-stu-id="5d826-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="5d826-133">Чем меньше число, тем больше приоритет.</span><span class="sxs-lookup"><span data-stu-id="5d826-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="5d826-134">-Правило</span><span class="sxs-lookup"><span data-stu-id="5d826-134">-Rule</span></span>
<span data-ttu-id="5d826-135">Задает список правил для группировки в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="5d826-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d826-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d826-136">-Confirm</span></span>
<span data-ttu-id="5d826-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d826-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d826-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d826-138">-WhatIf</span></span>
<span data-ttu-id="5d826-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d826-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d826-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d826-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d826-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d826-141">CommonParameters</span></span>
<span data-ttu-id="5d826-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d826-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d826-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d826-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d826-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d826-144">INPUTS</span></span>

### <span data-ttu-id="5d826-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="5d826-145">None</span></span>
<span data-ttu-id="5d826-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5d826-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d826-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d826-147">OUTPUTS</span></span>

### <span data-ttu-id="5d826-148">Microsoft. Azure. Commands. Network. Models. PSFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="5d826-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="5d826-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d826-149">NOTES</span></span>

## <span data-ttu-id="5d826-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d826-150">RELATED LINKS</span></span>

[<span data-ttu-id="5d826-151">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="5d826-151">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="5d826-152">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="5d826-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="5d826-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="5d826-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
