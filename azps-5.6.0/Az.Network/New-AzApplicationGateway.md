---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 00e1cb4856afc00f13730dbee55de9499d603290
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961763"
---
# <span data-ttu-id="1bb3f-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bb3f-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="1bb3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb3f-103">Создает шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-103">Creates an application gateway.</span></span>

## <span data-ttu-id="1bb3f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1bb3f-104">SYNTAX</span></span>

### <span data-ttu-id="1bb3f-105">IdentityByUserAssignedIdidId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1bb3f-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bb3f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb3f-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bb3f-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1bb3f-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bb3f-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="1bb3f-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 [-SslProfiles <PSApplicationGatewaySslProfile[]>] -HttpListeners <PSApplicationGatewayHttpListener[]>
 [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-PrivateLinkConfiguration <PSApplicationGatewayPrivateLinkConfiguration[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb3f-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bb3f-109">DESCRIPTION</span></span>
<span data-ttu-id="1bb3f-110">Для создания шлюза приложения Azure создается **cmdlet New-AzApplicationGateway.**</span><span class="sxs-lookup"><span data-stu-id="1bb3f-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="1bb3f-111">Для шлюза приложения требуется следующее:</span><span class="sxs-lookup"><span data-stu-id="1bb3f-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="1bb3f-112">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-112">A resource group.</span></span>
- <span data-ttu-id="1bb3f-113">Виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-113">A virtual network.</span></span>
- <span data-ttu-id="1bb3f-114">Серверный пул серверов, содержащий IP-адреса серверов.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="1bb3f-115">Параметры серверного пула.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-115">Back-end server pool settings.</span></span> <span data-ttu-id="1bb3f-116">В каждом пуле есть параметры портов, протоколов и сходства на основе cookie, которые применяются на всех серверах в пуле.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="1bb3f-117">IP-адреса переднего ip-адреса, открытые на шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="1bb3f-118">Конечным IP-адресом может быть общедоступный или внутренний IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="1bb3f-119">Передне-конечные порты , которые являются общедоступными портами, открытыми на шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="1bb3f-120">Трафик, который попадает в эти порты, перенаправляется на серверные серверы.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="1bb3f-121">Правило маршрутки запроса, которое связывает слушателя и серверный пул серверов.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="1bb3f-122">Это правило определяет, на какие серверные серверы следует направить трафик при его попадании на определенного слушателя.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="1bb3f-123">У слушателя есть порт переднего и переднего IP-адреса, протокол (HTTP или HTTPS) и имя SSL-сертификата (при настройке offload SSL).</span><span class="sxs-lookup"><span data-stu-id="1bb3f-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="1bb3f-124">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1bb3f-124">EXAMPLES</span></span>

### <span data-ttu-id="1bb3f-125">Пример 1. Создание шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="1bb3f-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="1bb3f-126">В следующем примере создается шлюз приложения, сначала создается группа ресурсов и виртуальная сеть, а также следующие:</span><span class="sxs-lookup"><span data-stu-id="1bb3f-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="1bb3f-127">Серверный пул серверов</span><span class="sxs-lookup"><span data-stu-id="1bb3f-127">A back-end server pool</span></span>
- <span data-ttu-id="1bb3f-128">Параметры серверного пула</span><span class="sxs-lookup"><span data-stu-id="1bb3f-128">Back-end server pool settings</span></span>
- <span data-ttu-id="1bb3f-129">Передне-конечные порты</span><span class="sxs-lookup"><span data-stu-id="1bb3f-129">Front-end ports</span></span>
- <span data-ttu-id="1bb3f-130">IP-адреса переднего ip-адреса</span><span class="sxs-lookup"><span data-stu-id="1bb3f-130">Front-end IP addresses</span></span>
- <span data-ttu-id="1bb3f-131">Правило маршрутинга запросов с помощью этих четырех команд создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="1bb3f-132">Первая команда создает конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="1bb3f-133">Вторая команда создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="1bb3f-134">Третья команда проверяет конфигурацию подсети, а четвертая команда —, что виртуальная сеть создана успешно.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="1bb3f-135">Следующие команды создают шлюз приложения:</span><span class="sxs-lookup"><span data-stu-id="1bb3f-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="1bb3f-136">Первая команда создает конфигурацию IP-адреса с именем GatewayIp01 для созданной ранее подсети.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="1bb3f-137">Вторая команда создает серверный пул с именем Pool01 со списком серверных IP-адресов и сохраняет пул в переменной $Pool серверов.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="1bb3f-138">Третья команда создает параметры для серверного пула серверов и сохраняет их в переменной $PoolSetting сервера.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="1bb3f-139">Для этой команды создается стойкий порт порта 80, именуется FrontEndPort01, а порт сохраняется в переменной $FrontEndPort портом.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="1bb3f-140">Пятая команда создает общедоступный IP-адрес с использованием New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="1bb3f-141">Шестая команда создает конфигурацию ip-адреса переднего $PublicIp, именует ее FrontEndPortConfig01 и сохраняет ее в переменной $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="1bb3f-142">При использовании седьмой команды создается слушатель, используя ранее созданную $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="1bb3f-143">Команда в качестве первой команды создает правило для слушателя.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="1bb3f-144">Невероятная команда задает SKU.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="1bb3f-145">Десятая команда создает шлюз с использованием объектов, которые были за настроены предыдущими командами.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="1bb3f-146">Пример 2. Создание шлюза приложения с помощью удостоверения UserAssigned</span><span class="sxs-lookup"><span data-stu-id="1bb3f-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="1bb3f-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bb3f-147">PARAMETERS</span></span>

### <span data-ttu-id="1bb3f-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bb3f-148">-AsJob</span></span>
<span data-ttu-id="1bb3f-149">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1bb3f-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bb3f-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="1bb3f-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="1bb3f-151">Определяет сертификаты проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bb3f-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="1bb3f-153">Настройка авто шкалы</span><span class="sxs-lookup"><span data-stu-id="1bb3f-153">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="1bb3f-154">-BackendAddressPools</span></span>
<span data-ttu-id="1bb3f-155">Определяет список пулов конечных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="1bb3f-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="1bb3f-157">Определяет список back-end HTTP-параметров шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bb3f-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="1bb3f-159">Ошибка клиента шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="1bb3f-159">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb3f-160">-DefaultProfile</span></span>
<span data-ttu-id="1bb3f-161">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bb3f-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="1bb3f-162">-EnableFIPS</span></span>
<span data-ttu-id="1bb3f-163">Будет ли включена ли fiPS.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="1bb3f-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="1bb3f-164">-EnableHttp2</span></span>
<span data-ttu-id="1bb3f-165">Включена ли протокол HTTP2.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="1bb3f-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="1bb3f-166">-FirewallPolicy</span></span>
<span data-ttu-id="1bb3f-167">Конфигурация брандмауэра</span><span class="sxs-lookup"><span data-stu-id="1bb3f-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="1bb3f-168">-FirewallPolicyId</span></span>
<span data-ttu-id="1bb3f-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="1bb3f-169">FirewallPolicyId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-170">-Force</span><span class="sxs-lookup"><span data-stu-id="1bb3f-170">-Force</span></span>
<span data-ttu-id="1bb3f-171">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1bb3f-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="1bb3f-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="1bb3f-173">Включена ли связь firewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="1bb3f-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="1bb3f-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="1bb3f-175">Определяет список конфигураций IP-адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="1bb3f-176">-FrontendPorts</span></span>
<span data-ttu-id="1bb3f-177">Список переднего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-177">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="1bb3f-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="1bb3f-179">Определяет список конфигураций IP-адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-179">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="1bb3f-180">-HttpListeners</span></span>
<span data-ttu-id="1bb3f-181">Список HTTP-протоколов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-182">-Identity</span><span class="sxs-lookup"><span data-stu-id="1bb3f-182">-Identity</span></span>
<span data-ttu-id="1bb3f-183">Удостоверение шлюза приложения, которое будет назначено шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-184">-Location</span><span class="sxs-lookup"><span data-stu-id="1bb3f-184">-Location</span></span>
<span data-ttu-id="1bb3f-185">Определяет регион, в котором нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="1bb3f-186">-Name</span><span class="sxs-lookup"><span data-stu-id="1bb3f-186">-Name</span></span>
<span data-ttu-id="1bb3f-187">Указывает имя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="1bb3f-188">-PrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bb3f-188">-PrivateLinkConfiguration</span></span>
<span data-ttu-id="1bb3f-189">Список настройки privateLink</span><span class="sxs-lookup"><span data-stu-id="1bb3f-189">The list of privateLink Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-190">-Разротные</span><span class="sxs-lookup"><span data-stu-id="1bb3f-190">-Probes</span></span>
<span data-ttu-id="1bb3f-191">Указывает, что для шлюза приложения заданы зао-висячие зао-висячие.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-191">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-192">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="1bb3f-192">-RedirectConfigurations</span></span>
<span data-ttu-id="1bb3f-193">Список конфигурации перенаправления</span><span class="sxs-lookup"><span data-stu-id="1bb3f-193">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-194">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="1bb3f-194">-RequestRoutingRules</span></span>
<span data-ttu-id="1bb3f-195">Список правил маршрутки запросов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-195">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb3f-196">-ResourceGroupName</span></span>
<span data-ttu-id="1bb3f-197">Имя группы ресурсов, в которой нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-197">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="1bb3f-198">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1bb3f-198">-RewriteRuleSet</span></span>
<span data-ttu-id="1bb3f-199">Список rewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="1bb3f-199">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-200">-SKU</span><span class="sxs-lookup"><span data-stu-id="1bb3f-200">-Sku</span></span>
<span data-ttu-id="1bb3f-201">Указывает единицу сохраняемого акций (SKU) шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-201">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-202">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="1bb3f-202">-SslCertificates</span></span>
<span data-ttu-id="1bb3f-203">Список SSL-сертификатов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-203">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-204">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="1bb3f-204">-SslPolicy</span></span>
<span data-ttu-id="1bb3f-205">Политика SSL для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-205">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-206">-SslProfiles</span><span class="sxs-lookup"><span data-stu-id="1bb3f-206">-SslProfiles</span></span>
<span data-ttu-id="1bb3f-207">Список профилей SSL</span><span class="sxs-lookup"><span data-stu-id="1bb3f-207">The list of ssl profiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-208">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bb3f-208">-Tag</span></span>
<span data-ttu-id="1bb3f-209">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-209">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1bb3f-210">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1bb3f-210">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1bb3f-211">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="1bb3f-211">-TrustedClientCertificates</span></span>
<span data-ttu-id="1bb3f-212">Список цепочки сертификатов доверенных клиентских ЦС</span><span class="sxs-lookup"><span data-stu-id="1bb3f-212">The list of trusted client CA certificate chains</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-213">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1bb3f-213">-TrustedRootCertificate</span></span>
<span data-ttu-id="1bb3f-214">Список доверенных корневых сертификатов</span><span class="sxs-lookup"><span data-stu-id="1bb3f-214">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-215">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="1bb3f-215">-UrlPathMaps</span></span>
<span data-ttu-id="1bb3f-216">Указывает карты URL-пути для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-216">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-217">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="1bb3f-217">-UserAssignedIdentityId</span></span>
<span data-ttu-id="1bb3f-218">ResourceId идентификатора пользователя, назначенного шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-218">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-219">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bb3f-219">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="1bb3f-220">Указывает конфигурацию брандмауэра веб-приложения (WAF).</span><span class="sxs-lookup"><span data-stu-id="1bb3f-220">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="1bb3f-221">Вы можете использовать Get-AzApplicationGatewayWebApplicationFirewallConfiguration WAF.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-221">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bb3f-222">-Zone</span><span class="sxs-lookup"><span data-stu-id="1bb3f-222">-Zone</span></span>
<span data-ttu-id="1bb3f-223">Список зон доступности, обозначающий, из которых должен получиться шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-223">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="1bb3f-224">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bb3f-224">-Confirm</span></span>
<span data-ttu-id="1bb3f-225">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-225">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bb3f-226">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb3f-226">-WhatIf</span></span>
<span data-ttu-id="1bb3f-227">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-227">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb3f-228">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-228">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bb3f-229">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb3f-229">CommonParameters</span></span>
<span data-ttu-id="1bb3f-230">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb3f-230">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb3f-231">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bb3f-231">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb3f-232">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bb3f-232">INPUTS</span></span>

### <span data-ttu-id="1bb3f-233">System.String</span><span class="sxs-lookup"><span data-stu-id="1bb3f-233">System.String</span></span>

### <span data-ttu-id="1bb3f-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1bb3f-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="1bb3f-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="1bb3f-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="1bb3f-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="1bb3f-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="1bb3f-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="1bb3f-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="1bb3f-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="1bb3f-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="1bb3f-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="1bb3f-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="1bb3f-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="1bb3f-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="1bb3f-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="1bb3f-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-247">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="1bb3f-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-248">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="1bb3f-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="1bb3f-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="1bb3f-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bb3f-250">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="1bb3f-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bb3f-251">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="1bb3f-252">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1bb3f-252">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1bb3f-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="1bb3f-253">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="1bb3f-254">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1bb3f-254">OUTPUTS</span></span>

### <span data-ttu-id="1bb3f-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bb3f-255">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1bb3f-256">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1bb3f-256">NOTES</span></span>

## <span data-ttu-id="1bb3f-257">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bb3f-257">RELATED LINKS</span></span>

[<span data-ttu-id="1bb3f-258">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1bb3f-258">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1bb3f-259">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1bb3f-259">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="1bb3f-260">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="1bb3f-260">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="1bb3f-261">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="1bb3f-261">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="1bb3f-262">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1bb3f-262">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1bb3f-263">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bb3f-263">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1bb3f-264">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="1bb3f-264">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="1bb3f-265">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="1bb3f-265">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="1bb3f-266">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1bb3f-266">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="1bb3f-267">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1bb3f-267">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
