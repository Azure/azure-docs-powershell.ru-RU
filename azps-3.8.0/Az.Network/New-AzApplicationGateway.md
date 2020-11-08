---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 46eb4979c62a5c1f2cb8277ddc1461ee09a339c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074846"
---
# <span data-ttu-id="06b57-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06b57-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="06b57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06b57-102">SYNOPSIS</span></span>
<span data-ttu-id="06b57-103">Создание шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-103">Creates an application gateway.</span></span>

## <span data-ttu-id="06b57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06b57-104">SYNTAX</span></span>

### <span data-ttu-id="06b57-105">IdentityByUserAssignedIdentityId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="06b57-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>]
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b57-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="06b57-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b57-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="06b57-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b57-108">IdentityByIdentityObject</span><span class="sxs-lookup"><span data-stu-id="06b57-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-ForceFirewallPolicyAssociation] [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity>
 [-Force] [-AsJob] [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06b57-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06b57-109">DESCRIPTION</span></span>
<span data-ttu-id="06b57-110">Командлет **New-AzApplicationGateway** создает шлюз приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="06b57-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="06b57-111">Для шлюза приложений требуются указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="06b57-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="06b57-112">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06b57-112">A resource group.</span></span>
- <span data-ttu-id="06b57-113">Виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="06b57-113">A virtual network.</span></span>
- <span data-ttu-id="06b57-114">Пул серверного сервера, содержащий IP-адреса серверных серверов.</span><span class="sxs-lookup"><span data-stu-id="06b57-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="06b57-115">Параметры пула серверов для заднего сервера.</span><span class="sxs-lookup"><span data-stu-id="06b57-115">Back-end server pool settings.</span></span> <span data-ttu-id="06b57-116">У каждого пула есть такие параметры, как порт, протокол и сходство на основе файлов cookie, которые применяются ко всем серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="06b57-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="06b57-117">IP-адреса переднего плана, которые являются IP-адресами, открытыми на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="06b57-118">Интерфейсный IP-адрес может быть общедоступным IP-адресом или внутренним IP-адресом.</span><span class="sxs-lookup"><span data-stu-id="06b57-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="06b57-119">Внешние порты, которые являются общедоступными портами, открытыми на шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="06b57-120">Трафик, который нажимает эти порты, перенаправляется на серверные серверы.</span><span class="sxs-lookup"><span data-stu-id="06b57-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="06b57-121">Правило маршрутизации запросов, связывающее прослушиватель и пул серверного сервера.</span><span class="sxs-lookup"><span data-stu-id="06b57-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="06b57-122">Правило определяет, на какой серверный пул должен перенаправляться трафик при каждом обращении к определенному прослушивателю.</span><span class="sxs-lookup"><span data-stu-id="06b57-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="06b57-123">У прослушивателя есть интерфейсный порт, клиентский IP-адрес, протокол (HTTP или HTTPS) и имя сертификата SSL (при настройке разгрузки SSL).</span><span class="sxs-lookup"><span data-stu-id="06b57-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="06b57-124">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06b57-124">EXAMPLES</span></span>

### <span data-ttu-id="06b57-125">Пример 1: Создание шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="06b57-125">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="06b57-126">В следующем примере создается шлюз приложений, в результате чего создаются группа ресурсов и виртуальная сеть, а также указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="06b57-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="06b57-127">Пул серверов в серверной части</span><span class="sxs-lookup"><span data-stu-id="06b57-127">A back-end server pool</span></span>
- <span data-ttu-id="06b57-128">Параметры пула серверов в серверной части</span><span class="sxs-lookup"><span data-stu-id="06b57-128">Back-end server pool settings</span></span>
- <span data-ttu-id="06b57-129">Интерфейсные порты</span><span class="sxs-lookup"><span data-stu-id="06b57-129">Front-end ports</span></span>
- <span data-ttu-id="06b57-130">IP-адреса интерфейса пользователя</span><span class="sxs-lookup"><span data-stu-id="06b57-130">Front-end IP addresses</span></span>
- <span data-ttu-id="06b57-131">Правило маршрутизации запросов эти четыре команды создают виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="06b57-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="06b57-132">Первая команда создает конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="06b57-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="06b57-133">Вторая команда создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="06b57-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="06b57-134">Третья команда проверяет конфигурацию подсети, а четвертая команда проверяет, успешно ли создана виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="06b57-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="06b57-135">Следующие команды создают шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="06b57-136">Первая команда создает IP-конфигурацию с именем GatewayIp01 для подсети, созданной ранее.</span><span class="sxs-lookup"><span data-stu-id="06b57-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="06b57-137">Вторая команда создает пул серверных серверов с именем Pool01 со списком серверных IP-адресов и сохраняет пул в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="06b57-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="06b57-138">Третья команда создает параметры для пула ресурсов на внутреннем сервере и сохраняет параметры в переменной $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="06b57-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="06b57-139">В этой команде создается порт переднего плана на порту 80 с именем FrontEndPort01 и хранится порт в переменной $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="06b57-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="06b57-140">Пятая команда создает общедоступный IP-адрес с помощью New-AzPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="06b57-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="06b57-141">Шестая команда создает IP-конфигурацию переднего плана с помощью $PublicIp, называет ее FrontEndPortConfig01 и сохраняет в переменной $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="06b57-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="06b57-142">Команда седьмая создает прослушиватель с помощью ранее созданного $FrontEndIpConfig $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="06b57-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="06b57-143">Восьмая команда создает правило для слушателя.</span><span class="sxs-lookup"><span data-stu-id="06b57-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="06b57-144">Команда девятка задает SKU.</span><span class="sxs-lookup"><span data-stu-id="06b57-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="06b57-145">Десятая команда создает шлюз, используя объекты, заданные предыдущими командами.</span><span class="sxs-lookup"><span data-stu-id="06b57-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="06b57-146">Пример 2: Создание шлюза приложений с удостоверением UserAssigned</span><span class="sxs-lookup"><span data-stu-id="06b57-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
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

## <span data-ttu-id="06b57-147">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06b57-147">PARAMETERS</span></span>

### <span data-ttu-id="06b57-148">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06b57-148">-AsJob</span></span>
<span data-ttu-id="06b57-149">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="06b57-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06b57-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="06b57-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="06b57-151">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-151">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-152">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b57-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="06b57-153">Настройка автомасштабирования</span><span class="sxs-lookup"><span data-stu-id="06b57-153">Autoscale Configuration</span></span>

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

### <span data-ttu-id="06b57-154">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="06b57-154">-BackendAddressPools</span></span>
<span data-ttu-id="06b57-155">Указывает список пулов серверных адресов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-155">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="06b57-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="06b57-157">Указывает список параметров HTTP для серверного шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b57-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="06b57-159">Ошибка клиента в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="06b57-159">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="06b57-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b57-160">-DefaultProfile</span></span>
<span data-ttu-id="06b57-161">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06b57-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06b57-162">-EnableFIPS</span><span class="sxs-lookup"><span data-stu-id="06b57-162">-EnableFIPS</span></span>
<span data-ttu-id="06b57-163">Включен ли FIPS.</span><span class="sxs-lookup"><span data-stu-id="06b57-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="06b57-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="06b57-164">-EnableHttp2</span></span>
<span data-ttu-id="06b57-165">Включена ли HTTP2.</span><span class="sxs-lookup"><span data-stu-id="06b57-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="06b57-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="06b57-166">-FirewallPolicy</span></span>
<span data-ttu-id="06b57-167">Настройка брандмауэра</span><span class="sxs-lookup"><span data-stu-id="06b57-167">Firewall configuration</span></span>

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

### <span data-ttu-id="06b57-168">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="06b57-168">-FirewallPolicyId</span></span>
<span data-ttu-id="06b57-169">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="06b57-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="06b57-170">-Force</span><span class="sxs-lookup"><span data-stu-id="06b57-170">-Force</span></span>
<span data-ttu-id="06b57-171">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="06b57-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06b57-172">-ForceFirewallPolicyAssociation</span><span class="sxs-lookup"><span data-stu-id="06b57-172">-ForceFirewallPolicyAssociation</span></span>
<span data-ttu-id="06b57-173">Включена ли ассоциация принудительного firewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="06b57-173">Whether Force firewallPolicy association is enabled.</span></span>

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

### <span data-ttu-id="06b57-174">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="06b57-174">-FrontendIPConfigurations</span></span>
<span data-ttu-id="06b57-175">Задает список IP-конфигураций интерфейсов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-175">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-176">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="06b57-176">-FrontendPorts</span></span>
<span data-ttu-id="06b57-177">Задает список интерфейсных портов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-177">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-178">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="06b57-178">-GatewayIPConfigurations</span></span>
<span data-ttu-id="06b57-179">Задает список IP-конфигураций для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-179">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-180">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="06b57-180">-HttpListeners</span></span>
<span data-ttu-id="06b57-181">Задает список прослушивателей HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-181">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-182">-Identity</span><span class="sxs-lookup"><span data-stu-id="06b57-182">-Identity</span></span>
<span data-ttu-id="06b57-183">Удостоверение шлюза приложения, назначаемое шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-183">Application Gateway Identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="06b57-184">-Location</span><span class="sxs-lookup"><span data-stu-id="06b57-184">-Location</span></span>
<span data-ttu-id="06b57-185">Указывает область, в которой нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="06b57-185">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="06b57-186">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06b57-186">-Name</span></span>
<span data-ttu-id="06b57-187">Указывает имя шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-187">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="06b57-188">-Зонды</span><span class="sxs-lookup"><span data-stu-id="06b57-188">-Probes</span></span>
<span data-ttu-id="06b57-189">Указывает зонды для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-189">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-190">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="06b57-190">-RedirectConfigurations</span></span>
<span data-ttu-id="06b57-191">Список конфигурации перенаправления</span><span class="sxs-lookup"><span data-stu-id="06b57-191">The list of redirect configuration</span></span>

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

### <span data-ttu-id="06b57-192">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="06b57-192">-RequestRoutingRules</span></span>
<span data-ttu-id="06b57-193">Указывает список правил маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-193">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-194">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b57-194">-ResourceGroupName</span></span>
<span data-ttu-id="06b57-195">Указывает имя группы ресурсов, в которой нужно создать шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="06b57-195">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="06b57-196">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="06b57-196">-RewriteRuleSet</span></span>
<span data-ttu-id="06b57-197">Список RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="06b57-197">The list of RewriteRuleSet</span></span>

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

### <span data-ttu-id="06b57-198">-SKU</span><span class="sxs-lookup"><span data-stu-id="06b57-198">-Sku</span></span>
<span data-ttu-id="06b57-199">Задает единицу хранения (SKU) шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-199">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="06b57-200">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="06b57-200">-SslCertificates</span></span>
<span data-ttu-id="06b57-201">Указывает список SSL-сертификатов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-201">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-202">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="06b57-202">-SslPolicy</span></span>
<span data-ttu-id="06b57-203">Указывает политику SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-203">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-204">-Тег</span><span class="sxs-lookup"><span data-stu-id="06b57-204">-Tag</span></span>
<span data-ttu-id="06b57-205">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="06b57-205">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="06b57-206">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="06b57-206">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="06b57-207">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="06b57-207">-TrustedRootCertificate</span></span>
<span data-ttu-id="06b57-208">Список доверенных корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="06b57-208">The list of trusted root certificates</span></span>

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

### <span data-ttu-id="06b57-209">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="06b57-209">-UrlPathMaps</span></span>
<span data-ttu-id="06b57-210">Указывает карты URL-пути для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-210">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="06b57-211">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="06b57-211">-UserAssignedIdentityId</span></span>
<span data-ttu-id="06b57-212">ResourceId для пользователя, которому назначена идентификация, назначаемая шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="06b57-212">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

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

### <span data-ttu-id="06b57-213">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b57-213">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="06b57-214">Определяет конфигурацию брандмауэра веб-приложения (WAF).</span><span class="sxs-lookup"><span data-stu-id="06b57-214">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="06b57-215">Вы можете использовать командлет Get-AzApplicationGatewayWebApplicationFirewallConfiguration, чтобы получить WAF.</span><span class="sxs-lookup"><span data-stu-id="06b57-215">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="06b57-216">-Zone</span><span class="sxs-lookup"><span data-stu-id="06b57-216">-Zone</span></span>
<span data-ttu-id="06b57-217">Список зон доступности, обозначающих, откуда должен быть получен шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="06b57-217">A list of availability zones denoting where the application gateway needs to come from.</span></span>

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

### <span data-ttu-id="06b57-218">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06b57-218">-Confirm</span></span>
<span data-ttu-id="06b57-219">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="06b57-219">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b57-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b57-220">-WhatIf</span></span>
<span data-ttu-id="06b57-221">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="06b57-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b57-222">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="06b57-222">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b57-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b57-223">CommonParameters</span></span>
<span data-ttu-id="06b57-224">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06b57-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b57-225">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06b57-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b57-226">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06b57-226">INPUTS</span></span>

### <span data-ttu-id="06b57-227">System. String</span><span class="sxs-lookup"><span data-stu-id="06b57-227">System.String</span></span>

### <span data-ttu-id="06b57-228">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06b57-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="06b57-229">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="06b57-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="06b57-230">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="06b57-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="06b57-231">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="06b57-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="06b57-232">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="06b57-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="06b57-233">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="06b57-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="06b57-234">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="06b57-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="06b57-235">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="06b57-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="06b57-236">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="06b57-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="06b57-237">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="06b57-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="06b57-238">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="06b57-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="06b57-239">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="06b57-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="06b57-240">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="06b57-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="06b57-241">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="06b57-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="06b57-242">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="06b57-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="06b57-243">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="06b57-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="06b57-244">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b57-244">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="06b57-245">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b57-245">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="06b57-246">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="06b57-246">System.Collections.Hashtable</span></span>

### <span data-ttu-id="06b57-247">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="06b57-247">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="06b57-248">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06b57-248">OUTPUTS</span></span>

### <span data-ttu-id="06b57-249">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06b57-249">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="06b57-250">Пуск</span><span class="sxs-lookup"><span data-stu-id="06b57-250">NOTES</span></span>

## <span data-ttu-id="06b57-251">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06b57-251">RELATED LINKS</span></span>

[<span data-ttu-id="06b57-252">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="06b57-252">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="06b57-253">New-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="06b57-253">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="06b57-254">New-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="06b57-254">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="06b57-255">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06b57-255">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="06b57-256">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06b57-256">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="06b57-257">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="06b57-257">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="06b57-258">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="06b57-258">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="06b57-259">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="06b57-259">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="06b57-260">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="06b57-260">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="06b57-261">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="06b57-261">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
