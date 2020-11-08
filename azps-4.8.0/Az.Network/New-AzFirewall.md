---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: a7c38a264860ad4a8458dbdb3555980279a33ff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244861"
---
# <span data-ttu-id="8dd3d-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8dd3d-101">New-AzFirewall</span></span>

## <span data-ttu-id="8dd3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd3d-103">Создание нового брандмауэра в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="8dd3d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dd3d-104">SYNTAX</span></span>

### <span data-ttu-id="8dd3d-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dd3d-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dd3d-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="8dd3d-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dd3d-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="8dd3d-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8dd3d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dd3d-108">DESCRIPTION</span></span>
<span data-ttu-id="8dd3d-109">Командлет **New-AzFirewall** создает брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="8dd3d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dd3d-110">EXAMPLES</span></span>

### <span data-ttu-id="8dd3d-111">Пример 1: создание брандмауэра, подключенного к виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8dd3d-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="8dd3d-112">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="8dd3d-113">Поскольку правила не указаны, брандмауэр блокирует весь трафик (поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="8dd3d-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="8dd3d-114">Угроза Корпорация Intel также работает в режиме по умолчанию – Alert (это значит, что вредоносный трафик будет записан в журнал, но его запрещено использовать).</span><span class="sxs-lookup"><span data-stu-id="8dd3d-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="8dd3d-115">Пример 2: создание брандмауэра, разрешающего весь трафик HTTPS</span><span class="sxs-lookup"><span data-stu-id="8dd3d-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="8dd3d-116">В этом примере создается брандмауэр, разрешающий весь трафик HTTPS для порта 443.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="8dd3d-117">Угроза Intel будет работать в режиме по умолчанию — оповещение — это значит, что вредоносный трафик будет регистрироваться, но не отклоняться.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="8dd3d-118">Пример 3: DNAT-Redirect трафик, направленный на 10.1.2.3:80 в 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="8dd3d-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="8dd3d-119">В этом примере создается брандмауэр, который переадресует IP-адрес назначения и порт всех пакетов, предназначенных для 10.1.2.3:80 на 10.2.3.4: угроза, в этом примере Корпорация Intel отключилась.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="8dd3d-120">Пример 4: создание брандмауэра без правил и с угрозой Intel в режиме оповещения</span><span class="sxs-lookup"><span data-stu-id="8dd3d-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="8dd3d-121">В этом примере создается брандмауэр, блокирующий весь трафик (поведение по умолчанию) и имеющий угрозу для системы безопасности Intel в режиме оповещения.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="8dd3d-122">Это означает, что журналы выдаются для вредоносного трафика, прежде чем применять другие правила (в этом случае единственным правилом по умолчанию является DENY ALL).</span><span class="sxs-lookup"><span data-stu-id="8dd3d-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="8dd3d-123">Пример 5: создание брандмауэра, который разрешает весь трафик HTTP для порта 8080, но блокирует вредоносные домены, идентифицированные угрозой Intel</span><span class="sxs-lookup"><span data-stu-id="8dd3d-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="8dd3d-124">В этом примере создается брандмауэр, который обеспечивает весь трафик HTTP для порта 8080, если он не является вредоносным по сравнению с угрозой Intel.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="8dd3d-125">При работе в режиме запрета, в отличие от предупреждения, трафик, который считается вредоносным в угрозе, не только заносится в журнал, но и заблокирован.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="8dd3d-126">Пример 6: создание брандмауэра без правил и с зонами доступности</span><span class="sxs-lookup"><span data-stu-id="8dd3d-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="8dd3d-127">В этом примере создается брандмауэр со всеми доступными зонами доступности.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="8dd3d-128">Пример 7: создание брандмауэра с двумя и более общими IP-адресами</span><span class="sxs-lookup"><span data-stu-id="8dd3d-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="8dd3d-129">В этом примере создается брандмауэр, подключенный к виртуальной сети "vnet" с двумя общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="8dd3d-130">Пример 8: создание брандмауэра, разрешающего трафик MSSQL для определенной базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="8dd3d-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="8dd3d-131">В этом примере создается брандмауэр, разрешающий трафик MSSQL на стандартном порте 1433 в базу данных SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="8dd3d-132">Пример 9: создание брандмауэра, подключенного к виртуальному концентратору</span><span class="sxs-lookup"><span data-stu-id="8dd3d-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="8dd3d-133">В этом примере создается брандмауэр, подключенный к виртуальному концентратору "vHub".</span><span class="sxs-lookup"><span data-stu-id="8dd3d-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="8dd3d-134">$Fp политики брандмауэра будут подключены к брандмауэру.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="8dd3d-135">Этот брандмауэр разрешает или запрещает трафик согласно правилам, упомянутым в политике брандмауэра $fp.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="8dd3d-136">Виртуальные концентраторы и брандмауэр должны находиться в одном и том же регионах.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="8dd3d-137">Пример 10: создание межсетевого экрана с помощью настройки добавлениеного каталога для угроз</span><span class="sxs-lookup"><span data-stu-id="8dd3d-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="8dd3d-138">В этом примере создается брандмауэр, добавление "www.microsoft.com" и "8.8.8.8" из службы логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="8dd3d-139">Пример 11: создание брандмауэра с настроенным параметром настройки закрытого диапазона</span><span class="sxs-lookup"><span data-stu-id="8dd3d-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="8dd3d-140">В этом примере создается брандмауэр, который обрабатывает диапазоны IP-адресов "99.99.99.0/24" и "66.66.0.0/16", а трафик SNAT не будет проводиться на эти адреса.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="8dd3d-141">Пример 12: создание брандмауэра с подсетью управления и общим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="8dd3d-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="8dd3d-142">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="8dd3d-143">Поскольку правила не указаны, брандмауэр блокирует весь трафик (поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="8dd3d-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="8dd3d-144">Угроза Корпорация Intel также работает в режиме по умолчанию – Alert (это значит, что вредоносный трафик будет записан в журнал, но его запрещено использовать).</span><span class="sxs-lookup"><span data-stu-id="8dd3d-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="8dd3d-145">Для поддержки сценариев с принудительным туннелированием этот брандмауэр будет использовать подсеть "AzureFirewallManagementSubnet" и общедоступный IP-адрес управления для своего трафика управления.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="8dd3d-146">Пример 13: создание брандмауэра с политикой брандмауэра, подключенной к виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8dd3d-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="8dd3d-147">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="8dd3d-148">Правила и логика событий, которые будут применяться к брандмауэру, будут взяты из политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="8dd3d-149">Пример 14: создание межсетевого экрана с DNS-прокси и DNS-серверами</span><span class="sxs-lookup"><span data-stu-id="8dd3d-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="8dd3d-150">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="8dd3d-151">DNS-прокси включен для этого брандмауэра и 2 DNS-серверов предоставляются.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="8dd3d-152">Кроме того, необходимо, чтобы DNS-прокси для сетевых правил был настроен таким образом, что при наличии каких-либо правил сети, использующих полные доменные имена, будет использоваться DNS-прокси.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="8dd3d-153">Пример 15: создание межсетевого экрана с несколькими IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="8dd3d-154">Брандмауэр может быть связан с виртуальным концентратором</span><span class="sxs-lookup"><span data-stu-id="8dd3d-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -Sku AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="8dd3d-155">В этом примере создается брандмауэр, подключенный к концентратору Virtual Hub в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="8dd3d-156">Брандмауэру будут назначены 2 общедоступные IP – адреса, которые будут создаваться неявным образом.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="8dd3d-157">16. Создайте брандмауэр с разрешающим активным FTP.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="8dd3d-158">В этом примере создается брандмауэр с флагом Allow Active FTP.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="8dd3d-159">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dd3d-159">PARAMETERS</span></span>

### <span data-ttu-id="8dd3d-160">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8dd3d-160">-ApplicationRuleCollection</span></span>
<span data-ttu-id="8dd3d-161">Определяет наборы правил приложений для нового брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-161">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-162">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dd3d-162">-AsJob</span></span>
<span data-ttu-id="8dd3d-163">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8dd3d-163">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd3d-164">-DefaultProfile</span></span>
<span data-ttu-id="8dd3d-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-166">-DnsProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8dd3d-166">-DnsProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="8dd3d-167">В сетевых правилах для полных доменных имен требуются функции DNS-прокси.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-167">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-168">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="8dd3d-168">-DnsServer</span></span>
<span data-ttu-id="8dd3d-169">Список DNS-серверов, которые будут использоваться для разрешения DNS,</span><span class="sxs-lookup"><span data-stu-id="8dd3d-169">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-170">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="8dd3d-170">-EnableDnsProxy</span></span>
<span data-ttu-id="8dd3d-171">Включите DNS-прокси.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-171">Enable DNS Proxy.</span></span> <span data-ttu-id="8dd3d-172">По умолчанию это значение отключено.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-172">By default it is disabled.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-173">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="8dd3d-173">-AllowActiveFTP</span></span>
<span data-ttu-id="8dd3d-174">Разрешение активного FTP на брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-174">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="8dd3d-175">По умолчанию это значение отключено.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-175">By default it is disabled.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-176">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8dd3d-176">-FirewallPolicyId</span></span>
<span data-ttu-id="8dd3d-177">Политика брандмауэра, вложенная в брандмауэр</span><span class="sxs-lookup"><span data-stu-id="8dd3d-177">The firewall policy attached to the firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-178">-Force</span><span class="sxs-lookup"><span data-stu-id="8dd3d-178">-Force</span></span>
<span data-ttu-id="8dd3d-179">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-179">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-180">-HubIPAddresses</span><span class="sxs-lookup"><span data-stu-id="8dd3d-180">-HubIPAddresses</span></span>
<span data-ttu-id="8dd3d-181">IP-адреса для брандмауэра, подключенного к виртуальному концентратору</span><span class="sxs-lookup"><span data-stu-id="8dd3d-181">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-182">-Location</span><span class="sxs-lookup"><span data-stu-id="8dd3d-182">-Location</span></span>
<span data-ttu-id="8dd3d-183">Указывает регион для брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-183">Specifies the region for the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-184">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8dd3d-184">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="8dd3d-185">Один или несколько общедоступных IP-адресов, которые нужно использовать для трафика управления.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-185">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="8dd3d-186">Общедоступные IP-адреса должны использовать стандартную SKU и должны принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-186">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-187">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8dd3d-187">-Name</span></span>
<span data-ttu-id="8dd3d-188">Указывает имя брандмауэра Azure, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-188">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-189">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8dd3d-189">-NatRuleCollection</span></span>
<span data-ttu-id="8dd3d-190">Список AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="8dd3d-190">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-191">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8dd3d-191">-NetworkRuleCollection</span></span>
<span data-ttu-id="8dd3d-192">Список AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="8dd3d-192">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-193">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="8dd3d-193">-PrivateRange</span></span>
<span data-ttu-id="8dd3d-194">Частный диапазон IP-адресов, в который не SNAT'ed трафик</span><span class="sxs-lookup"><span data-stu-id="8dd3d-194">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-195">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8dd3d-195">-PublicIpAddress</span></span>
<span data-ttu-id="8dd3d-196">Один или несколько общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-196">One or more Public IP Addresses.</span></span> <span data-ttu-id="8dd3d-197">Общедоступные IP-адреса должны использовать стандартную SKU и должны принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-197">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-198">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="8dd3d-198">-PublicIpName</span></span>
<span data-ttu-id="8dd3d-199">Общедоступное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-199">Public Ip Name.</span></span> <span data-ttu-id="8dd3d-200">Общедоступный IP-адрес должен использовать стандартную SKU и должен принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-200">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-201">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd3d-201">-ResourceGroupName</span></span>
<span data-ttu-id="8dd3d-202">Указывает имя группы ресурсов, в которой будет содержаться брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-202">Specifies the name of a resource group to contain the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-203">-SKU</span><span class="sxs-lookup"><span data-stu-id="8dd3d-203">-Sku</span></span>
<span data-ttu-id="8dd3d-204">Тип SKU для брандмауэра</span><span class="sxs-lookup"><span data-stu-id="8dd3d-204">The sku type for firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-205">-Тег</span><span class="sxs-lookup"><span data-stu-id="8dd3d-205">-Tag</span></span>
<span data-ttu-id="8dd3d-206">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8dd3d-207">Например:</span><span class="sxs-lookup"><span data-stu-id="8dd3d-207">For example:</span></span>

<span data-ttu-id="8dd3d-208">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8dd3d-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="8dd3d-209">-ThreatIntelMode</span></span>
<span data-ttu-id="8dd3d-210">Задает режим работы для логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="8dd3d-211">Режим по умолчанию — оповещение.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="8dd3d-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="8dd3d-213">Добавление для логики операций с угрозами</span><span class="sxs-lookup"><span data-stu-id="8dd3d-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="8dd3d-214">-VirtualHubId</span></span>
<span data-ttu-id="8dd3d-215">Виртуальный концентратор, к которому подключен брандмауэр</span><span class="sxs-lookup"><span data-stu-id="8dd3d-215">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8dd3d-216">-VirtualNetwork</span></span>
<span data-ttu-id="8dd3d-217">Виртуальная сеть</span><span class="sxs-lookup"><span data-stu-id="8dd3d-217">Virtual Network</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8dd3d-218">-VirtualNetworkName</span></span>
<span data-ttu-id="8dd3d-219">Указывает имя виртуальной сети, для которой будет развернут брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="8dd3d-220">Виртуальная сеть и брандмауэр должны принадлежать к одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="8dd3d-221">-Zone</span></span>
<span data-ttu-id="8dd3d-222">Список зон доступности, обозначающих, откуда следует поступать брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd3d-223">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dd3d-223">-Confirm</span></span>
<span data-ttu-id="8dd3d-224">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd3d-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd3d-225">-WhatIf</span></span>
<span data-ttu-id="8dd3d-226">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dd3d-227">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd3d-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd3d-228">CommonParameters</span></span>
<span data-ttu-id="8dd3d-229">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dd3d-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd3d-230">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dd3d-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd3d-231">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dd3d-231">INPUTS</span></span>

### <span data-ttu-id="8dd3d-232">System. String</span><span class="sxs-lookup"><span data-stu-id="8dd3d-232">System.String</span></span>

### <span data-ttu-id="8dd3d-233">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8dd3d-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="8dd3d-234">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="8dd3d-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="8dd3d-235">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8dd3d-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="8dd3d-236">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="8dd3d-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="8dd3d-237">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="8dd3d-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="8dd3d-238">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="8dd3d-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="8dd3d-239">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8dd3d-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8dd3d-240">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dd3d-240">OUTPUTS</span></span>

### <span data-ttu-id="8dd3d-241">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="8dd3d-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="8dd3d-242">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dd3d-242">NOTES</span></span>

## <span data-ttu-id="8dd3d-243">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dd3d-243">RELATED LINKS</span></span>

[<span data-ttu-id="8dd3d-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8dd3d-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="8dd3d-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8dd3d-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="8dd3d-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="8dd3d-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="8dd3d-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8dd3d-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="8dd3d-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8dd3d-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="8dd3d-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8dd3d-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
