---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 3b4014b56a36228fe53221430ffe79a43118f8fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911731"
---
# <span data-ttu-id="4f0cb-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4f0cb-101">New-AzFirewall</span></span>

## <span data-ttu-id="4f0cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="4f0cb-103">Создание нового брандмауэра в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="4f0cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f0cb-104">SYNTAX</span></span>

### <span data-ttu-id="4f0cb-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f0cb-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f0cb-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="4f0cb-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f0cb-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="4f0cb-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f0cb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f0cb-108">DESCRIPTION</span></span>
<span data-ttu-id="4f0cb-109">Командлет **New-AzFirewall** создает брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="4f0cb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f0cb-110">EXAMPLES</span></span>

### <span data-ttu-id="4f0cb-111">1: создание брандмауэра, подключенного к виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="4f0cb-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="4f0cb-112">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="4f0cb-113">Поскольку правила не указаны, брандмауэр блокирует весь трафик (поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4f0cb-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="4f0cb-114">Угроза Корпорация Intel также работает в режиме по умолчанию – Alert (это значит, что вредоносный трафик будет записан в журнал, но его запрещено использовать).</span><span class="sxs-lookup"><span data-stu-id="4f0cb-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="4f0cb-115">2. Создание брандмауэра, разрешающего весь трафик HTTPS</span><span class="sxs-lookup"><span data-stu-id="4f0cb-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="4f0cb-116">В этом примере создается брандмауэр, разрешающий весь трафик HTTPS для порта 443.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="4f0cb-117">Угроза Intel будет работать в режиме по умолчанию — оповещение — это значит, что вредоносный трафик будет регистрироваться, но не отклоняться.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="4f0cb-118">3: DNAT-Redirect трафик, направленный на 10.1.2.3:80 в 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="4f0cb-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="4f0cb-119">В этом примере создается брандмауэр, который переадресует IP-адрес назначения и порт всех пакетов, предназначенных для 10.1.2.3:80 на 10.2.3.4: угроза, в этом примере Корпорация Intel отключилась.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="4f0cb-120">4. Создание брандмауэра без правил и с угрозой Intel в режиме оповещения</span><span class="sxs-lookup"><span data-stu-id="4f0cb-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="4f0cb-121">В этом примере создается брандмауэр, блокирующий весь трафик (поведение по умолчанию) и имеющий угрозу для системы безопасности Intel в режиме оповещения.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="4f0cb-122">Это означает, что журналы выдаются для вредоносного трафика, прежде чем применять другие правила (в этом случае единственным правилом по умолчанию является DENY ALL).</span><span class="sxs-lookup"><span data-stu-id="4f0cb-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="4f0cb-123">5. Создание брандмауэра, который обеспечивает весь трафик HTTP для порта 8080, но блокирует вредоносные домены, идентифицированные угрозой Intel</span><span class="sxs-lookup"><span data-stu-id="4f0cb-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="4f0cb-124">В этом примере создается брандмауэр, который обеспечивает весь трафик HTTP для порта 8080, если он не является вредоносным по сравнению с угрозой Intel.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="4f0cb-125">При работе в режиме запрета, в отличие от предупреждения, трафик, который считается вредоносным в угрозе, не только заносится в журнал, но и заблокирован.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="4f0cb-126">6. Создание брандмауэра без правил и с зонами доступности</span><span class="sxs-lookup"><span data-stu-id="4f0cb-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="4f0cb-127">В этом примере создается брандмауэр со всеми доступными зонами доступности.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="4f0cb-128">7. Создание брандмауэра с двумя и более общими IP-адресами</span><span class="sxs-lookup"><span data-stu-id="4f0cb-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="4f0cb-129">В этом примере создается брандмауэр, подключенный к виртуальной сети "vnet" с двумя общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="4f0cb-130">8: создание брандмауэра, позволяющего трафик MSSQL для определенной базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="4f0cb-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="4f0cb-131">В этом примере создается брандмауэр, разрешающий трафик MSSQL на стандартном порте 1433 в базу данных SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="4f0cb-132">9: создание брандмауэра, подключенного к виртуальному концентратору</span><span class="sxs-lookup"><span data-stu-id="4f0cb-132">9:  Create a Firewall attached to a virtual hub</span></span>
```
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="4f0cb-133">В этом примере создается брандмауэр, подключенный к виртуальному концентратору "vHub".</span><span class="sxs-lookup"><span data-stu-id="4f0cb-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="4f0cb-134">$Fp политики брандмауэра будут подключены к брандмауэру.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="4f0cb-135">Этот брандмауэр разрешает или запрещает трафик согласно правилам, упомянутым в политике брандмауэра $fp.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="4f0cb-136">Виртуальные концентраторы и брандмауэр должны находиться в одном и том же регионах.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="4f0cb-137">10: создание межсетевого экрана с помощью настройки добавлениеного каталога для угроз</span><span class="sxs-lookup"><span data-stu-id="4f0cb-137">10: Create a Firewall with threat intelligence whitelist setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="4f0cb-138">В этом примере создается брандмауэр, добавление "www.microsoft.com" и "8.8.8.8" из службы логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="4f0cb-139">11. Создание брандмауэра с настроенным параметром настройки закрытого диапазона</span><span class="sxs-lookup"><span data-stu-id="4f0cb-139">11: Create a Firewall with customized private range setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="4f0cb-140">В этом примере создается брандмауэр, который обрабатывает диапазоны IP-адресов "99.99.99.0/24" и "66.66.0.0/16", а трафик SNAT не будет проводиться на эти адреса.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="4f0cb-141">12: создание брандмауэра с подсетью управления и общим IP-адресом</span><span class="sxs-lookup"><span data-stu-id="4f0cb-141">12:  Create a Firewall with a management subnet and Public IP address</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="4f0cb-142">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="4f0cb-143">Поскольку правила не указаны, брандмауэр блокирует весь трафик (поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4f0cb-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="4f0cb-144">Угроза Корпорация Intel также работает в режиме по умолчанию – Alert (это значит, что вредоносный трафик будет записан в журнал, но его запрещено использовать).</span><span class="sxs-lookup"><span data-stu-id="4f0cb-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="4f0cb-145">Для поддержки сценариев с принудительным туннелированием этот брандмауэр будет использовать подсеть "AzureFirewallManagementSubnet" и общедоступный IP-адрес управления для своего трафика управления.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="4f0cb-146">13: создание брандмауэра с политикой брандмауэра, подключенной к виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-146">13:  Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="4f0cb-147">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="4f0cb-148">Правила и логика событий, которые будут применяться к брандмауэру, будут взяты из политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

## <span data-ttu-id="4f0cb-149">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f0cb-149">PARAMETERS</span></span>

### <span data-ttu-id="4f0cb-150">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4f0cb-150">-ApplicationRuleCollection</span></span>
<span data-ttu-id="4f0cb-151">Определяет наборы правил приложений для нового брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-151">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="4f0cb-152">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f0cb-152">-AsJob</span></span>
<span data-ttu-id="4f0cb-153">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4f0cb-153">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f0cb-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f0cb-154">-DefaultProfile</span></span>
<span data-ttu-id="4f0cb-155">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f0cb-156">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="4f0cb-156">-FirewallPolicyId</span></span>
<span data-ttu-id="4f0cb-157">Политика брандмауэра, вложенная в брандмауэр</span><span class="sxs-lookup"><span data-stu-id="4f0cb-157">The firewall policy attached to the firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-158">-Force</span><span class="sxs-lookup"><span data-stu-id="4f0cb-158">-Force</span></span>
<span data-ttu-id="4f0cb-159">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-159">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f0cb-160">-Location</span><span class="sxs-lookup"><span data-stu-id="4f0cb-160">-Location</span></span>
<span data-ttu-id="4f0cb-161">Указывает регион для брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-161">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="4f0cb-162">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4f0cb-162">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="4f0cb-163">Один или несколько общедоступных IP-адресов, которые нужно использовать для трафика управления.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-163">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="4f0cb-164">Общедоступные IP-адреса должны использовать стандартную SKU и должны принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-164">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-165">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4f0cb-165">-Name</span></span>
<span data-ttu-id="4f0cb-166">Указывает имя брандмауэра Azure, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-166">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4f0cb-167">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4f0cb-167">-NatRuleCollection</span></span>
<span data-ttu-id="4f0cb-168">Список AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="4f0cb-168">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="4f0cb-169">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4f0cb-169">-NetworkRuleCollection</span></span>
<span data-ttu-id="4f0cb-170">Список AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="4f0cb-170">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="4f0cb-171">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="4f0cb-171">-PrivateRange</span></span>
<span data-ttu-id="4f0cb-172">Частный диапазон IP-адресов, в который не SNAT'ed трафик</span><span class="sxs-lookup"><span data-stu-id="4f0cb-172">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-173">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4f0cb-173">-PublicIpAddress</span></span>
<span data-ttu-id="4f0cb-174">Один или несколько общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-174">One or more Public IP Addresses.</span></span> <span data-ttu-id="4f0cb-175">Общедоступные IP-адреса должны использовать стандартную SKU и должны принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-175">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-176">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="4f0cb-176">-PublicIpName</span></span>
<span data-ttu-id="4f0cb-177">Общедоступное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-177">Public Ip Name.</span></span> <span data-ttu-id="4f0cb-178">Общедоступный IP-адрес должен использовать стандартную SKU и должен принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-178">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f0cb-179">-ResourceGroupName</span></span>
<span data-ttu-id="4f0cb-180">Указывает имя группы ресурсов, в которой будет содержаться брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-180">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="4f0cb-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="4f0cb-181">-Sku</span></span>
<span data-ttu-id="4f0cb-182">Тип SKU для брандмауэра</span><span class="sxs-lookup"><span data-stu-id="4f0cb-182">The sku type for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-183">-Тег</span><span class="sxs-lookup"><span data-stu-id="4f0cb-183">-Tag</span></span>
<span data-ttu-id="4f0cb-184">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4f0cb-185">Например:</span><span class="sxs-lookup"><span data-stu-id="4f0cb-185">For example:</span></span>

<span data-ttu-id="4f0cb-186">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="4f0cb-186">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4f0cb-187">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="4f0cb-187">-ThreatIntelMode</span></span>
<span data-ttu-id="4f0cb-188">Задает режим работы для логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-188">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="4f0cb-189">Режим по умолчанию — оповещение.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-189">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-190">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="4f0cb-190">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="4f0cb-191">Добавление для логики операций с угрозами</span><span class="sxs-lookup"><span data-stu-id="4f0cb-191">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-192">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="4f0cb-192">-VirtualHubId</span></span>
<span data-ttu-id="4f0cb-193">Виртуальный концентратор, к которому подключен брандмауэр</span><span class="sxs-lookup"><span data-stu-id="4f0cb-193">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-194">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f0cb-194">-VirtualNetwork</span></span>
<span data-ttu-id="4f0cb-195">Виртуальная сеть</span><span class="sxs-lookup"><span data-stu-id="4f0cb-195">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-196">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4f0cb-196">-VirtualNetworkName</span></span>
<span data-ttu-id="4f0cb-197">Указывает имя виртуальной сети, для которой будет развернут брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-197">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="4f0cb-198">Виртуальная сеть и брандмауэр должны принадлежать к одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-198">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-199">-Zone</span><span class="sxs-lookup"><span data-stu-id="4f0cb-199">-Zone</span></span>
<span data-ttu-id="4f0cb-200">Список зон доступности, обозначающих, откуда следует поступать брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-200">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0cb-201">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f0cb-201">-Confirm</span></span>
<span data-ttu-id="4f0cb-202">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f0cb-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f0cb-203">-WhatIf</span></span>
<span data-ttu-id="4f0cb-204">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f0cb-205">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f0cb-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f0cb-206">CommonParameters</span></span>
<span data-ttu-id="4f0cb-207">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f0cb-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f0cb-208">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f0cb-208">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f0cb-209">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f0cb-209">INPUTS</span></span>

### <span data-ttu-id="4f0cb-210">System. String</span><span class="sxs-lookup"><span data-stu-id="4f0cb-210">System.String</span></span>

### <span data-ttu-id="4f0cb-211">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f0cb-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="4f0cb-212">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="4f0cb-212">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="4f0cb-213">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4f0cb-213">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="4f0cb-214">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="4f0cb-214">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="4f0cb-215">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="4f0cb-215">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="4f0cb-216">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="4f0cb-216">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="4f0cb-217">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f0cb-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f0cb-218">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f0cb-218">OUTPUTS</span></span>

### <span data-ttu-id="4f0cb-219">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="4f0cb-219">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="4f0cb-220">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f0cb-220">NOTES</span></span>

## <span data-ttu-id="4f0cb-221">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f0cb-221">RELATED LINKS</span></span>

[<span data-ttu-id="4f0cb-222">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4f0cb-222">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="4f0cb-223">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4f0cb-223">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="4f0cb-224">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="4f0cb-224">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="4f0cb-225">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4f0cb-225">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="4f0cb-226">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4f0cb-226">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="4f0cb-227">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4f0cb-227">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
