---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730345"
---
# <span data-ttu-id="032dc-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="032dc-101">New-AzFirewall</span></span>

## <span data-ttu-id="032dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="032dc-102">SYNOPSIS</span></span>
<span data-ttu-id="032dc-103">Создание нового брандмауэра в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="032dc-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="032dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="032dc-104">SYNTAX</span></span>

### <span data-ttu-id="032dc-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="032dc-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="032dc-106">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="032dc-106">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="032dc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="032dc-107">DESCRIPTION</span></span>
<span data-ttu-id="032dc-108">Командлет **New-AzFirewall** создает брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="032dc-108">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="032dc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="032dc-109">EXAMPLES</span></span>

### <span data-ttu-id="032dc-110">1: создание брандмауэра, подключенного к виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="032dc-110">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="032dc-111">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="032dc-111">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="032dc-112">Поскольку правила не указаны, брандмауэр блокирует весь трафик (поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="032dc-112">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="032dc-113">Угроза Корпорация Intel также работает в режиме по умолчанию – Alert (это значит, что вредоносный трафик будет записан в журнал, но его запрещено использовать).</span><span class="sxs-lookup"><span data-stu-id="032dc-113">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="032dc-114">2. Создание брандмауэра, разрешающего весь трафик HTTPS</span><span class="sxs-lookup"><span data-stu-id="032dc-114">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="032dc-115">В этом примере создается брандмауэр, разрешающий весь трафик HTTPS для порта 443.</span><span class="sxs-lookup"><span data-stu-id="032dc-115">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="032dc-116">Угроза Intel будет работать в режиме по умолчанию — оповещение — это значит, что вредоносный трафик будет регистрироваться, но не отклоняться.</span><span class="sxs-lookup"><span data-stu-id="032dc-116">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="032dc-117">3: DNAT-Redirect трафик, направленный на 10.1.2.3:80 в 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="032dc-117">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="032dc-118">В этом примере создается брандмауэр, который переадресует IP-адрес назначения и порт всех пакетов, предназначенных для 10.1.2.3:80 на 10.2.3.4: угроза, в этом примере Корпорация Intel отключилась.</span><span class="sxs-lookup"><span data-stu-id="032dc-118">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="032dc-119">4. Создание брандмауэра без правил и с угрозой Intel в режиме оповещения</span><span class="sxs-lookup"><span data-stu-id="032dc-119">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

<span data-ttu-id="032dc-120">В этом примере создается брандмауэр, блокирующий весь трафик (поведение по умолчанию) и имеющий угрозу для системы безопасности Intel в режиме оповещения.</span><span class="sxs-lookup"><span data-stu-id="032dc-120">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="032dc-121">Это означает, что журналы выдаются для вредоносного трафика, прежде чем применять другие правила (в этом случае единственным правилом по умолчанию является DENY ALL).</span><span class="sxs-lookup"><span data-stu-id="032dc-121">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="032dc-122">5. Создание брандмауэра, который обеспечивает весь трафик HTTP для порта 8080, но блокирует вредоносные домены, идентифицированные угрозой Intel</span><span class="sxs-lookup"><span data-stu-id="032dc-122">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="032dc-123">В этом примере создается брандмауэр, который обеспечивает весь трафик HTTP для порта 8080, если он не является вредоносным по сравнению с угрозой Intel.</span><span class="sxs-lookup"><span data-stu-id="032dc-123">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="032dc-124">При работе в режиме запрета, в отличие от предупреждения, трафик, который считается вредоносным в угрозе, не только заносится в журнал, но и заблокирован.</span><span class="sxs-lookup"><span data-stu-id="032dc-124">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

## <span data-ttu-id="032dc-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="032dc-125">PARAMETERS</span></span>

### <span data-ttu-id="032dc-126">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="032dc-126">-ApplicationRuleCollection</span></span>
<span data-ttu-id="032dc-127">Определяет наборы правил приложений для нового брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="032dc-127">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="032dc-128">-AsJob</span></span>
<span data-ttu-id="032dc-129">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="032dc-129">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="032dc-130">-DefaultProfile</span></span>
<span data-ttu-id="032dc-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="032dc-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="032dc-132">-Force</span><span class="sxs-lookup"><span data-stu-id="032dc-132">-Force</span></span>
<span data-ttu-id="032dc-133">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="032dc-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-134">-Location</span><span class="sxs-lookup"><span data-stu-id="032dc-134">-Location</span></span>
<span data-ttu-id="032dc-135">Указывает регион для брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="032dc-135">Specifies the region for the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="032dc-136">-Name</span></span>
<span data-ttu-id="032dc-137">Указывает имя брандмауэра Azure, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="032dc-137">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-138">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="032dc-138">-NatRuleCollection</span></span>
<span data-ttu-id="032dc-139">Список AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="032dc-139">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-140">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="032dc-140">-NetworkRuleCollection</span></span>
<span data-ttu-id="032dc-141">Список AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="032dc-141">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-142">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="032dc-142">-PublicIpName</span></span>
<span data-ttu-id="032dc-143">Общедоступное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="032dc-143">Public Ip Name.</span></span> <span data-ttu-id="032dc-144">Общедоступный IP-адрес должен использовать стандартную SKU и должен принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="032dc-144">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="032dc-145">-ResourceGroupName</span></span>
<span data-ttu-id="032dc-146">Указывает имя группы ресурсов, в которой будет содержаться брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="032dc-146">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-147">-Тег</span><span class="sxs-lookup"><span data-stu-id="032dc-147">-Tag</span></span>
<span data-ttu-id="032dc-148">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="032dc-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="032dc-149">Например:</span><span class="sxs-lookup"><span data-stu-id="032dc-149">For example:</span></span>

<span data-ttu-id="032dc-150">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="032dc-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-151">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="032dc-151">-ThreatIntelMode</span></span>
<span data-ttu-id="032dc-152">Задает режим работы для логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="032dc-152">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="032dc-153">Режим по умолчанию — оповещение.</span><span class="sxs-lookup"><span data-stu-id="032dc-153">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-154">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="032dc-154">-VirtualNetworkName</span></span>
<span data-ttu-id="032dc-155">Указывает имя виртуальной сети, для которой будет развернут брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="032dc-155">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="032dc-156">Виртуальная сеть и брандмауэр должны принадлежать к одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="032dc-156">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032dc-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="032dc-157">-Confirm</span></span>
<span data-ttu-id="032dc-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="032dc-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="032dc-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="032dc-159">-WhatIf</span></span>
<span data-ttu-id="032dc-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="032dc-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="032dc-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="032dc-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="032dc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="032dc-162">CommonParameters</span></span>
<span data-ttu-id="032dc-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="032dc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="032dc-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="032dc-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="032dc-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="032dc-165">INPUTS</span></span>

### <span data-ttu-id="032dc-166">System. String</span><span class="sxs-lookup"><span data-stu-id="032dc-166">System.String</span></span>

### <span data-ttu-id="032dc-167">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="032dc-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="032dc-168">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="032dc-168">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="032dc-169">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="032dc-169">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="032dc-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="032dc-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="032dc-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="032dc-171">OUTPUTS</span></span>

### <span data-ttu-id="032dc-172">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="032dc-172">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="032dc-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="032dc-173">NOTES</span></span>

## <span data-ttu-id="032dc-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="032dc-174">RELATED LINKS</span></span>

[<span data-ttu-id="032dc-175">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="032dc-175">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="032dc-176">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="032dc-176">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="032dc-177">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="032dc-177">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="032dc-178">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="032dc-178">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="032dc-179">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="032dc-179">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="032dc-180">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="032dc-180">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
