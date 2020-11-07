---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902181"
---
# <span data-ttu-id="021a5-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="021a5-101">New-AzFirewall</span></span>

## <span data-ttu-id="021a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="021a5-102">SYNOPSIS</span></span>
<span data-ttu-id="021a5-103">Создание нового брандмауэра в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="021a5-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="021a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="021a5-104">SYNTAX</span></span>

### <span data-ttu-id="021a5-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="021a5-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="021a5-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="021a5-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="021a5-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="021a5-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="021a5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="021a5-108">DESCRIPTION</span></span>
<span data-ttu-id="021a5-109">Командлет **New-AzFirewall** создает брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="021a5-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="021a5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="021a5-110">EXAMPLES</span></span>

### <span data-ttu-id="021a5-111">1: создание брандмауэра, подключенного к виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="021a5-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="021a5-112">В этом примере создается брандмауэр, подключенный к виртуальной сети vnet, в той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="021a5-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="021a5-113">Поскольку правила не указаны, брандмауэр блокирует весь трафик (поведение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="021a5-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="021a5-114">Угроза Корпорация Intel также работает в режиме по умолчанию – Alert (это значит, что вредоносный трафик будет записан в журнал, но его запрещено использовать).</span><span class="sxs-lookup"><span data-stu-id="021a5-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="021a5-115">2. Создание брандмауэра, разрешающего весь трафик HTTPS</span><span class="sxs-lookup"><span data-stu-id="021a5-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="021a5-116">В этом примере создается брандмауэр, разрешающий весь трафик HTTPS для порта 443.</span><span class="sxs-lookup"><span data-stu-id="021a5-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="021a5-117">Угроза Intel будет работать в режиме по умолчанию — оповещение — это значит, что вредоносный трафик будет регистрироваться, но не отклоняться.</span><span class="sxs-lookup"><span data-stu-id="021a5-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="021a5-118">3: DNAT-Redirect трафик, направленный на 10.1.2.3:80 в 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="021a5-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="021a5-119">В этом примере создается брандмауэр, который переадресует IP-адрес назначения и порт всех пакетов, предназначенных для 10.1.2.3:80 на 10.2.3.4: угроза, в этом примере Корпорация Intel отключилась.</span><span class="sxs-lookup"><span data-stu-id="021a5-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="021a5-120">4. Создание брандмауэра без правил и с угрозой Intel в режиме оповещения</span><span class="sxs-lookup"><span data-stu-id="021a5-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="021a5-121">В этом примере создается брандмауэр, блокирующий весь трафик (поведение по умолчанию) и имеющий угрозу для системы безопасности Intel в режиме оповещения.</span><span class="sxs-lookup"><span data-stu-id="021a5-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="021a5-122">Это означает, что журналы выдаются для вредоносного трафика, прежде чем применять другие правила (в этом случае единственным правилом по умолчанию является DENY ALL).</span><span class="sxs-lookup"><span data-stu-id="021a5-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="021a5-123">5. Создание брандмауэра, который обеспечивает весь трафик HTTP для порта 8080, но блокирует вредоносные домены, идентифицированные угрозой Intel</span><span class="sxs-lookup"><span data-stu-id="021a5-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="021a5-124">В этом примере создается брандмауэр, который обеспечивает весь трафик HTTP для порта 8080, если он не является вредоносным по сравнению с угрозой Intel.</span><span class="sxs-lookup"><span data-stu-id="021a5-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="021a5-125">При работе в режиме запрета, в отличие от предупреждения, трафик, который считается вредоносным в угрозе, не только заносится в журнал, но и заблокирован.</span><span class="sxs-lookup"><span data-stu-id="021a5-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="021a5-126">6. Создание брандмауэра без правил и с зонами доступности</span><span class="sxs-lookup"><span data-stu-id="021a5-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="021a5-127">В этом примере создается брандмауэр со всеми доступными зонами доступности.</span><span class="sxs-lookup"><span data-stu-id="021a5-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="021a5-128">7. Создание брандмауэра с двумя и более общими IP-адресами</span><span class="sxs-lookup"><span data-stu-id="021a5-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="021a5-129">В этом примере создается брандмауэр, подключенный к виртуальной сети "vnet" с двумя общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="021a5-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="021a5-130">8: создание брандмауэра, позволяющего трафик MSSQL для определенной базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="021a5-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="021a5-131">В этом примере создается брандмауэр, разрешающий трафик MSSQL на стандартном порте 1433 в базу данных SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="021a5-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="021a5-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="021a5-132">PARAMETERS</span></span>

### <span data-ttu-id="021a5-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="021a5-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="021a5-134">Определяет наборы правил приложений для нового брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="021a5-134">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="021a5-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="021a5-135">-AsJob</span></span>
<span data-ttu-id="021a5-136">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="021a5-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="021a5-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021a5-137">-DefaultProfile</span></span>
<span data-ttu-id="021a5-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="021a5-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="021a5-139">-Force</span><span class="sxs-lookup"><span data-stu-id="021a5-139">-Force</span></span>
<span data-ttu-id="021a5-140">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="021a5-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="021a5-141">-Location</span><span class="sxs-lookup"><span data-stu-id="021a5-141">-Location</span></span>
<span data-ttu-id="021a5-142">Указывает регион для брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="021a5-142">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="021a5-143">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="021a5-143">-Name</span></span>
<span data-ttu-id="021a5-144">Указывает имя брандмауэра Azure, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="021a5-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="021a5-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="021a5-145">-NatRuleCollection</span></span>
<span data-ttu-id="021a5-146">Список AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="021a5-146">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="021a5-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="021a5-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="021a5-148">Список AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="021a5-148">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="021a5-149">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="021a5-149">-PublicIpAddress</span></span>
<span data-ttu-id="021a5-150">Один или несколько общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="021a5-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="021a5-151">Общедоступные IP-адреса должны использовать стандартную SKU и должны принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="021a5-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="021a5-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="021a5-152">-PublicIpName</span></span>
<span data-ttu-id="021a5-153">Общедоступное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="021a5-153">Public Ip Name.</span></span> <span data-ttu-id="021a5-154">Общедоступный IP-адрес должен использовать стандартную SKU и должен принадлежать к той же группе ресурсов, что и брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="021a5-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="021a5-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="021a5-155">-ResourceGroupName</span></span>
<span data-ttu-id="021a5-156">Указывает имя группы ресурсов, в которой будет содержаться брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="021a5-156">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="021a5-157">-Zone</span><span class="sxs-lookup"><span data-stu-id="021a5-157">-Zone</span></span>
<span data-ttu-id="021a5-158">Список зон доступности, обозначающих, откуда следует поступать брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="021a5-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="021a5-159">-Тег</span><span class="sxs-lookup"><span data-stu-id="021a5-159">-Tag</span></span>
<span data-ttu-id="021a5-160">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="021a5-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="021a5-161">Например:</span><span class="sxs-lookup"><span data-stu-id="021a5-161">For example:</span></span>

<span data-ttu-id="021a5-162">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="021a5-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="021a5-163">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="021a5-163">-ThreatIntelMode</span></span>
<span data-ttu-id="021a5-164">Задает режим работы для логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="021a5-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="021a5-165">Режим по умолчанию — оповещение.</span><span class="sxs-lookup"><span data-stu-id="021a5-165">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="021a5-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="021a5-166">-VirtualNetwork</span></span>
<span data-ttu-id="021a5-167">Виртуальная сеть</span><span class="sxs-lookup"><span data-stu-id="021a5-167">Virtual Network</span></span>

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

### <span data-ttu-id="021a5-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="021a5-168">-VirtualNetworkName</span></span>
<span data-ttu-id="021a5-169">Указывает имя виртуальной сети, для которой будет развернут брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="021a5-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="021a5-170">Виртуальная сеть и брандмауэр должны принадлежать к одной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="021a5-170">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="021a5-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="021a5-171">-Confirm</span></span>
<span data-ttu-id="021a5-172">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="021a5-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="021a5-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="021a5-173">-WhatIf</span></span>
<span data-ttu-id="021a5-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="021a5-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="021a5-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="021a5-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="021a5-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021a5-176">CommonParameters</span></span>
<span data-ttu-id="021a5-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="021a5-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021a5-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="021a5-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021a5-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="021a5-179">INPUTS</span></span>

### <span data-ttu-id="021a5-180">System. String</span><span class="sxs-lookup"><span data-stu-id="021a5-180">System.String</span></span>

### <span data-ttu-id="021a5-181">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="021a5-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="021a5-182">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="021a5-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="021a5-183">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="021a5-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="021a5-184">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="021a5-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="021a5-185">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="021a5-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="021a5-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="021a5-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="021a5-187">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="021a5-187">OUTPUTS</span></span>

### <span data-ttu-id="021a5-188">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="021a5-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="021a5-189">Пуск</span><span class="sxs-lookup"><span data-stu-id="021a5-189">NOTES</span></span>

## <span data-ttu-id="021a5-190">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="021a5-190">RELATED LINKS</span></span>

[<span data-ttu-id="021a5-191">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="021a5-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="021a5-192">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="021a5-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="021a5-193">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="021a5-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="021a5-194">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="021a5-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="021a5-195">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="021a5-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="021a5-196">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="021a5-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
