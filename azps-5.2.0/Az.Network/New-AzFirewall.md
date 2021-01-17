---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 031c926d25fe55a9572fe12922ccee26b6371a2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394591"
---
# <span data-ttu-id="ab048-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ab048-101">New-AzFirewall</span></span>

## <span data-ttu-id="ab048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab048-102">SYNOPSIS</span></span>
<span data-ttu-id="ab048-103">Создает брандмауэр в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab048-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="ab048-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ab048-104">SYNTAX</span></span>

### <span data-ttu-id="ab048-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab048-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab048-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="ab048-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab048-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="ab048-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab048-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab048-108">DESCRIPTION</span></span>
<span data-ttu-id="ab048-109">Для создания брандмауэра Azure создается новый брандмауэр **AzFirewall.**</span><span class="sxs-lookup"><span data-stu-id="ab048-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="ab048-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ab048-110">EXAMPLES</span></span>

### <span data-ttu-id="ab048-111">Пример 1. Создание брандмауэра, подключенного к виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ab048-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="ab048-112">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ab048-113">Так как правила не указаны, брандмауэр будет блокировать весь трафик (поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ab048-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="ab048-114">Технология Threat Intel также будет работать в режиме по умолчанию (оповещение), то есть вредоносный трафик будет регистрироваться, но не будет отклонен.</span><span class="sxs-lookup"><span data-stu-id="ab048-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="ab048-115">Пример 2. Создание брандмауэра, который разрешает весь трафик HTTPS</span><span class="sxs-lookup"><span data-stu-id="ab048-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="ab048-116">В этом примере создается брандмауэр, который разрешает весь ТРАФИК HTTPS в порте 443.</span><span class="sxs-lookup"><span data-stu-id="ab048-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="ab048-117">Технология Threat Intel будет работать в режиме по умолчанию (оповещение), то есть вредоносный трафик будет регистрироваться, но не будет отклонен.</span><span class="sxs-lookup"><span data-stu-id="ab048-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="ab048-118">Пример 3. А1: ПЕРЕнаправление трафика, направляемого в 10.1.2.3:80, в 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="ab048-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="ab048-119">В этом примере создан брандмауэр, который переводил IP-адрес назначения и порт всех пакетов, предназначенных для 10.1.2.3:80, в 10.2.3.4:8080 Threat Intel.</span><span class="sxs-lookup"><span data-stu-id="ab048-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="ab048-120">Пример 4. Создание брандмауэра без правил и с intel-угрозой в режиме оповещения</span><span class="sxs-lookup"><span data-stu-id="ab048-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="ab048-121">В этом примере создается брандмауэр, блок которого блокирует весь трафик (поведение по умолчанию) и в режиме оповещения запущена технология Threat Intel.</span><span class="sxs-lookup"><span data-stu-id="ab048-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="ab048-122">Это означает, что журналы оповещений выделяются вредоносным трафиком, прежде чем применять другие правила (в данном случае только стандартное правило — Запретить все).</span><span class="sxs-lookup"><span data-stu-id="ab048-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="ab048-123">Пример 5. Создание брандмауэра, который разрешает весь HTTP-трафик в порте 8080, но блокирует вредоносные домены, заданные Технологией Threat Intel</span><span class="sxs-lookup"><span data-stu-id="ab048-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="ab048-124">В этом примере создается брандмауэр, который разрешает весь HTTP-трафик в порте 8080, если он не считается вредоносным корпорацией Threat Intel.</span><span class="sxs-lookup"><span data-stu-id="ab048-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="ab048-125">При работе в режиме запрета, в отличие от оповещений, трафик, который считается вредоносным, от корпорации Threat Intel не только регистрируется, но и блокируется.</span><span class="sxs-lookup"><span data-stu-id="ab048-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="ab048-126">Пример 6. Создание брандмауэра без правил и зон доступности</span><span class="sxs-lookup"><span data-stu-id="ab048-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="ab048-127">В этом примере создается брандмауэр со всеми доступными зонами доступности.</span><span class="sxs-lookup"><span data-stu-id="ab048-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="ab048-128">Пример 7. Создание брандмауэра с двумя или более общедоступными IP-адресами</span><span class="sxs-lookup"><span data-stu-id="ab048-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="ab048-129">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet с двумя общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="ab048-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="ab048-130">Пример 8. Создание брандмауэра, который обеспечивает трафик MSSQL в определенные SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="ab048-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="ab048-131">В этом примере создается брандмауэр, который обеспечивает трафик MSSQL со стандартного порта 1433 SQL базы sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="ab048-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="ab048-132">Пример 9. Создание брандмауэра, подключенного к виртуальному концентратору</span><span class="sxs-lookup"><span data-stu-id="ab048-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="ab048-133">В этом примере создается брандмауэр, подключенный к виртуальному концентратору "vHub".</span><span class="sxs-lookup"><span data-stu-id="ab048-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="ab048-134">К брандмауэру будет $fp политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ab048-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="ab048-135">Этот брандмауэр разрешает и не разрешает трафик на основе правил, упомянутых в политике брандмауэра, $fp.</span><span class="sxs-lookup"><span data-stu-id="ab048-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="ab048-136">Виртуальный центр и брандмауэр должны быть в одинаковых регионах.</span><span class="sxs-lookup"><span data-stu-id="ab048-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="ab048-137">Пример 10. Создание брандмауэра с настройкой белого списка threat intelligence</span><span class="sxs-lookup"><span data-stu-id="ab048-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="ab048-138">В этом примере создается брандмауэр с белым списком "www.microsoft.com" и "8.8.8.8" из службы threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="ab048-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="ab048-139">Пример 11. Создание брандмауэра с настроенными настройками закрытого диапазона</span><span class="sxs-lookup"><span data-stu-id="ab048-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="ab048-140">В этом примере создается брандмауэр, который обрабатывает диапазоны IP-адресов 99.99.99.0/24" и "66.66.0.0/16" как частные диапазоны IP-адресов и не будет обрабатывать трафик на эти адреса.</span><span class="sxs-lookup"><span data-stu-id="ab048-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="ab048-141">Пример 12. Создание брандмауэра с подсетей управления и общедоступным IP-адресом</span><span class="sxs-lookup"><span data-stu-id="ab048-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="ab048-142">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ab048-143">Так как правила не указаны, брандмауэр будет блокировать весь трафик (поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ab048-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="ab048-144">Технология Threat Intel также будет работать в режиме по умолчанию (оповещение), то есть вредоносный трафик будет регистрироваться, но не будет отклонен.</span><span class="sxs-lookup"><span data-stu-id="ab048-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="ab048-145">Для поддержки сценариев принудительного туннелизации этот брандмауэр будет использовать подсеть AzureFirewallManagementSubnet и общедоступный IP-адрес управления для своего трафика управления.</span><span class="sxs-lookup"><span data-stu-id="ab048-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="ab048-146">Пример 13. Создание брандмауэра с политикой брандмауэра, подключенной к виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ab048-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="ab048-147">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ab048-148">Правила и аналитика угроз, которые будут применяться к брандмауэру, будут отданы из политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ab048-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="ab048-149">Пример 14. Создание брандмауэра с прокси-серверами DNS и DNS-серверами</span><span class="sxs-lookup"><span data-stu-id="ab048-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="ab048-150">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ab048-151">Для этого брандмауэра включен прокси-сервер DNS, и предоставляется 2 DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="ab048-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="ab048-152">Кроме того, необходимо использовать прокси-сервер DNS для правил сети, поэтому если есть правила сети с FQDNs, для них также будет использоваться прокси-сервер DNS.</span><span class="sxs-lookup"><span data-stu-id="ab048-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="ab048-153">Пример 15. Создание брандмауэра с несколькими IP-ами.</span><span class="sxs-lookup"><span data-stu-id="ab048-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="ab048-154">Брандмауэр можно связывать с виртуальным центром</span><span class="sxs-lookup"><span data-stu-id="ab048-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="ab048-155">В этом примере создается брандмауэр, присоединенный к виртуальному концентратору "концентратор" в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="ab048-156">Брандмауэру будут назначены 2 общедоступных IPS, которые создаются неявно.</span><span class="sxs-lookup"><span data-stu-id="ab048-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="ab048-157">16. Создайте брандмауэр с разрешением активной FTP-службы.</span><span class="sxs-lookup"><span data-stu-id="ab048-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="ab048-158">В этом примере создается брандмауэр с флажком "Разрешить активный FTP".</span><span class="sxs-lookup"><span data-stu-id="ab048-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="ab048-159">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab048-159">PARAMETERS</span></span>

### <span data-ttu-id="ab048-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="ab048-160">-AllowActiveFTP</span></span>
<span data-ttu-id="ab048-161">Разрешает активную FTP-службу в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="ab048-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="ab048-162">По умолчанию он отключен.</span><span class="sxs-lookup"><span data-stu-id="ab048-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="ab048-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ab048-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="ab048-164">Наборы правил для нового брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ab048-164">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="ab048-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab048-165">-AsJob</span></span>
<span data-ttu-id="ab048-166">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ab048-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab048-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab048-167">-DefaultProfile</span></span>
<span data-ttu-id="ab048-168">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab048-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab048-169">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="ab048-169">-DnsServer</span></span>
<span data-ttu-id="ab048-170">Список DNS-серверов, используемых для разрешения DNS,</span><span class="sxs-lookup"><span data-stu-id="ab048-170">The list of DNS Servers to be used for DNS resolution,</span></span>

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

### <span data-ttu-id="ab048-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="ab048-171">-EnableDnsProxy</span></span>
<span data-ttu-id="ab048-172">Включить прокси-сервер DNS.</span><span class="sxs-lookup"><span data-stu-id="ab048-172">Enable DNS Proxy.</span></span> <span data-ttu-id="ab048-173">По умолчанию он отключен.</span><span class="sxs-lookup"><span data-stu-id="ab048-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="ab048-174">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ab048-174">-FirewallPolicyId</span></span>
<span data-ttu-id="ab048-175">Политика брандмауэра, подключенная к брандмауэру</span><span class="sxs-lookup"><span data-stu-id="ab048-175">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="ab048-176">-Force</span><span class="sxs-lookup"><span data-stu-id="ab048-176">-Force</span></span>
<span data-ttu-id="ab048-177">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ab048-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab048-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="ab048-178">-HubIPAddress</span></span>
<span data-ttu-id="ab048-179">IP-адреса брандмауэра, подключенного к виртуальному концентратору</span><span class="sxs-lookup"><span data-stu-id="ab048-179">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab048-180">-Location</span><span class="sxs-lookup"><span data-stu-id="ab048-180">-Location</span></span>
<span data-ttu-id="ab048-181">Определяет регион для брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ab048-181">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="ab048-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ab048-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="ab048-183">Один или несколько общедоступных IP-адресов, которые используются для трафика управления.</span><span class="sxs-lookup"><span data-stu-id="ab048-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="ab048-184">Общедоступные IP-адреса должны использовать стандартный SKU и относятся к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="ab048-185">-Name</span><span class="sxs-lookup"><span data-stu-id="ab048-185">-Name</span></span>
<span data-ttu-id="ab048-186">Указывает имя брандмауэра Azure, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab048-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ab048-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ab048-187">-NatRuleCollection</span></span>
<span data-ttu-id="ab048-188">Список AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="ab048-188">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="ab048-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ab048-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="ab048-190">Список azureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="ab048-190">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="ab048-191">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="ab048-191">-PrivateRange</span></span>
<span data-ttu-id="ab048-192">Закрытые диапазоны IP-адресов, в которые не передается трафик SNAT</span><span class="sxs-lookup"><span data-stu-id="ab048-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="ab048-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ab048-193">-PublicIpAddress</span></span>
<span data-ttu-id="ab048-194">Один или несколько общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ab048-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="ab048-195">Общедоступные IP-адреса должны использовать стандартный SKU и относятся к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="ab048-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="ab048-196">-PublicIpName</span></span>
<span data-ttu-id="ab048-197">Имя общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="ab048-197">Public Ip Name.</span></span> <span data-ttu-id="ab048-198">Общедоступный IP-адрес должен использовать стандартный SKU и принадлежит к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="ab048-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab048-199">-ResourceGroupName</span></span>
<span data-ttu-id="ab048-200">Имя группы ресурсов, которая должна содержать брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-200">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="ab048-201">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ab048-201">-SkuName</span></span>
<span data-ttu-id="ab048-202">Имя SKU брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ab048-202">The sku name for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Sku
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab048-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ab048-203">-SkuTier</span></span>
<span data-ttu-id="ab048-204">Уровень SKU для брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ab048-204">The sku tier for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab048-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab048-205">-Tag</span></span>
<span data-ttu-id="ab048-206">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="ab048-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ab048-207">Например:</span><span class="sxs-lookup"><span data-stu-id="ab048-207">For example:</span></span>

<span data-ttu-id="ab048-208">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ab048-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ab048-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="ab048-209">-ThreatIntelMode</span></span>
<span data-ttu-id="ab048-210">Определяет режим операции для Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="ab048-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="ab048-211">Режим по умолчанию — "Оповещение", а не "Выключить".</span><span class="sxs-lookup"><span data-stu-id="ab048-211">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="ab048-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="ab048-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="ab048-213">Белый список для Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="ab048-213">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="ab048-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="ab048-214">-VirtualHubId</span></span>
<span data-ttu-id="ab048-215">Виртуальный центр, к который подключен брандмауэр</span><span class="sxs-lookup"><span data-stu-id="ab048-215">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="ab048-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab048-216">-VirtualNetwork</span></span>
<span data-ttu-id="ab048-217">Виртуальная сеть</span><span class="sxs-lookup"><span data-stu-id="ab048-217">Virtual Network</span></span>

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

### <span data-ttu-id="ab048-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ab048-218">-VirtualNetworkName</span></span>
<span data-ttu-id="ab048-219">Указывает имя виртуальной сети, для которой будет развернут брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="ab048-220">Виртуальная сеть и брандмауэр должны принадлежать к одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab048-220">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="ab048-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="ab048-221">-Zone</span></span>
<span data-ttu-id="ab048-222">Список зон доступности, в которых должен получиться брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="ab048-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="ab048-223">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab048-223">-Confirm</span></span>
<span data-ttu-id="ab048-224">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab048-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab048-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab048-225">-WhatIf</span></span>
<span data-ttu-id="ab048-226">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab048-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab048-227">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ab048-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab048-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab048-228">CommonParameters</span></span>
<span data-ttu-id="ab048-229">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab048-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab048-230">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab048-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab048-231">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ab048-231">INPUTS</span></span>

### <span data-ttu-id="ab048-232">System.String</span><span class="sxs-lookup"><span data-stu-id="ab048-232">System.String</span></span>

### <span data-ttu-id="ab048-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab048-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="ab048-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span><span class="sxs-lookup"><span data-stu-id="ab048-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="ab048-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ab048-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="ab048-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="ab048-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="ab048-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="ab048-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="ab048-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="ab048-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="ab048-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ab048-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ab048-240">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ab048-240">OUTPUTS</span></span>

### <span data-ttu-id="ab048-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ab048-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="ab048-242">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ab048-242">NOTES</span></span>

## <span data-ttu-id="ab048-243">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab048-243">RELATED LINKS</span></span>

[<span data-ttu-id="ab048-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ab048-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="ab048-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ab048-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="ab048-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ab048-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="ab048-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ab048-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="ab048-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ab048-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="ab048-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ab048-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
