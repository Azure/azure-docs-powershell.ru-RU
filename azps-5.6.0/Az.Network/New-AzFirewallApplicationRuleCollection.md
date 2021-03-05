---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: c82b150dd10a293bda1a001e4b930bcc2fe7989b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015032"
---
# <span data-ttu-id="19339-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="19339-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="19339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19339-102">SYNOPSIS</span></span>
<span data-ttu-id="19339-103">Создает набор правил брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="19339-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="19339-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19339-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19339-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19339-105">DESCRIPTION</span></span>
<span data-ttu-id="19339-106">С **помощью cmdletRuleCollection New-AzFirewallApplicationRuleCollection** создается коллекция правил брандмауэра приложений.</span><span class="sxs-lookup"><span data-stu-id="19339-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="19339-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19339-107">EXAMPLES</span></span>

### <span data-ttu-id="19339-108">Пример 1. Создание коллекции с одним правилом</span><span class="sxs-lookup"><span data-stu-id="19339-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="19339-109">В этом примере создается коллекция с одним правилом.</span><span class="sxs-lookup"><span data-stu-id="19339-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="19339-110">Будет разрешен весь трафик, который соответствует $rule 1.</span><span class="sxs-lookup"><span data-stu-id="19339-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="19339-111">Первое правило для всего трафика HTTPS в порте 443 от 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="19339-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="19339-112">Если существует еще одно коллекцию правил приложений с более высоким приоритетом (меньшее число), которое также соответствует трафику, занесен в $rule 1, то вместо этого будет действовать действие коллекции правил с более высоким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="19339-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="19339-113">Пример 2. Добавление правила в коллекцию правил</span><span class="sxs-lookup"><span data-stu-id="19339-113">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="19339-114">В этом примере создается новое коллекцию правил приложения с одним правилом, а затем в коллекцию правил добавляется второе правило с использованием метода AddRule для объекта коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="19339-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="19339-115">Каждое имя правила в данном наборе правил должно иметь уникальное имя без учета case.</span><span class="sxs-lookup"><span data-stu-id="19339-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="19339-116">Пример 3. Получите правило из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="19339-116">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="19339-117">В этом примере создается коллекция правил приложения с одним правилом, которое затем получает правило по имени, методу вызова GetRuleByName в объекте коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="19339-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="19339-118">Имя правила для метода GetRuleByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="19339-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="19339-119">Пример 4. Удаление правила из коллекции правил</span><span class="sxs-lookup"><span data-stu-id="19339-119">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="19339-120">В этом примере создается новое коллекцию правил приложения с двумя правилами, а затем удаляется первое правило из коллекции правил, вызывая метод RemoveRuleByName для объекта коллекции правил.</span><span class="sxs-lookup"><span data-stu-id="19339-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="19339-121">Имя правила для метода RemoveRuleByName нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="19339-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="19339-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19339-122">PARAMETERS</span></span>

### <span data-ttu-id="19339-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="19339-123">-ActionType</span></span>
<span data-ttu-id="19339-124">Действие в наборе правил</span><span class="sxs-lookup"><span data-stu-id="19339-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="19339-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19339-125">-DefaultProfile</span></span>
<span data-ttu-id="19339-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19339-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19339-127">-Name</span><span class="sxs-lookup"><span data-stu-id="19339-127">-Name</span></span>
<span data-ttu-id="19339-128">Указывает имя этого правила приложения.</span><span class="sxs-lookup"><span data-stu-id="19339-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="19339-129">Имя должно быть уникальным в наборе правил.</span><span class="sxs-lookup"><span data-stu-id="19339-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="19339-130">-Priority</span><span class="sxs-lookup"><span data-stu-id="19339-130">-Priority</span></span>
<span data-ttu-id="19339-131">Определяет приоритет этого правила.</span><span class="sxs-lookup"><span data-stu-id="19339-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="19339-132">Приоритетом является число от 100 до 65 000.</span><span class="sxs-lookup"><span data-stu-id="19339-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="19339-133">Чем меньше число, тем выше приоритет.</span><span class="sxs-lookup"><span data-stu-id="19339-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="19339-134">-Правило</span><span class="sxs-lookup"><span data-stu-id="19339-134">-Rule</span></span>
<span data-ttu-id="19339-135">Определяет список правил для группировки в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="19339-135">Specifies the list of rules to be grouped under this collection.</span></span>

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

### <span data-ttu-id="19339-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19339-136">-Confirm</span></span>
<span data-ttu-id="19339-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19339-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19339-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19339-138">-WhatIf</span></span>
<span data-ttu-id="19339-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19339-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19339-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19339-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19339-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19339-141">CommonParameters</span></span>
<span data-ttu-id="19339-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19339-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19339-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19339-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19339-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19339-144">INPUTS</span></span>

### <span data-ttu-id="19339-145">Нет</span><span class="sxs-lookup"><span data-stu-id="19339-145">None</span></span>

## <span data-ttu-id="19339-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19339-146">OUTPUTS</span></span>

### <span data-ttu-id="19339-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="19339-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="19339-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19339-148">NOTES</span></span>

## <span data-ttu-id="19339-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19339-149">RELATED LINKS</span></span>

[<span data-ttu-id="19339-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="19339-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="19339-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="19339-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="19339-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="19339-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
