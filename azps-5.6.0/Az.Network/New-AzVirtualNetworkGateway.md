---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c9729dd81dc5ff287ab032fdce6ad937c282e1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977880"
---
# <span data-ttu-id="7225b-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7225b-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="7225b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7225b-102">SYNOPSIS</span></span>
<span data-ttu-id="7225b-103">Создание виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="7225b-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="7225b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7225b-104">SYNTAX</span></span>

### <span data-ttu-id="7225b-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7225b-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7225b-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="7225b-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7225b-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="7225b-107">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7225b-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7225b-108">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7225b-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7225b-109">DESCRIPTION</span></span>
<span data-ttu-id="7225b-110">Виртуальный сетевой шлюз — это объект, представляющий шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="7225b-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="7225b-111">Командлет **New-AzVirtualNetworkGateway** создает в Azure объект шлюза на основе конфигурации "Имя", "Имя группы ресурсов", "Расположение" и "IP-адрес", а также тип шлюза и, если VPN, VPN-тип.</span><span class="sxs-lookup"><span data-stu-id="7225b-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="7225b-112">Вы также можете назвать SKU шлюза.</span><span class="sxs-lookup"><span data-stu-id="7225b-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="7225b-113">Если этот шлюз используется для подключений точка-узел, необходимо также включить пул адресов клиентов VPN, из которого можно назначить адреса клиентам, и корневой сертификат клиента VPN, используемый для проверки подлинности VPN-клиентов, подключающихся к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="7225b-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="7225b-114">Вы также можете включить другие функции, такие как BGP и Active-Active.</span><span class="sxs-lookup"><span data-stu-id="7225b-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="7225b-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7225b-115">EXAMPLES</span></span>

### <span data-ttu-id="7225b-116">Пример 1. Создание виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="7225b-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="7225b-117">Выше создается группа ресурсов, запрашивается общедоступный IP-адрес, создается виртуальная сеть и подсеть, а также создается виртуальный сетевой шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="7225b-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7225b-118">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Запад Великобритании" с ранее созданными конфигурациями IP-адресов, сохраненными в переменной ngwIPConfig, типом шлюза VPN, VPN-типом RouteBased и sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="7225b-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="7225b-119">Пример 2. Создание виртуального сетевого шлюза с конфигурацией внешнего радиуса</span><span class="sxs-lookup"><span data-stu-id="7225b-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="7225b-120">Выше создается группа ресурсов, запрашивается общедоступный IP-адрес, создается виртуальная сеть и подсеть, а также создается виртуальный сетевой шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="7225b-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7225b-121">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Запад Великобритании" с ранее созданными конфигурациями IP-адресов, сохраненными в переменной ngwIPConfig, типом шлюза VPN, VPN-типом RouteBased и sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="7225b-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="7225b-122">Она также добавляет внешний сервер радиуса с адресом TestRadiusServer.</span><span class="sxs-lookup"><span data-stu-id="7225b-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="7225b-123">Кроме того, будут настроены настраиваемые маршруты, заданные клиентами на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="7225b-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="7225b-124">Пример 3. Создание виртуального сетевого шлюза с помощью параметров P2S</span><span class="sxs-lookup"><span data-stu-id="7225b-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="7225b-125">Выше создается группа ресурсов, запрашивается общедоступный IP-адрес, создается виртуальная сеть и подсеть, а также создается виртуальный сетевой шлюз с настройками P2S, например VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy и т. д. в Azure.</span><span class="sxs-lookup"><span data-stu-id="7225b-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="7225b-126">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Запад Великобритании" с ранее созданными конфигурациями IP-адресов, сохраненными в переменной ngwIPConfig, типом шлюза VPN, VPN-типом RouteBased и sku "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="7225b-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="7225b-127">Параметры Vpn будут за настроены на шлюзе, например VpnProtocol set as Ikev2, VpnClientAddressPool как "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName и настраиваемая политика vpn ipsec, переданная в объект:$vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="7225b-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="7225b-128">Кроме того, будут настроены настраиваемые маршруты, заданные клиентами на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="7225b-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="7225b-129">Пример 4. Создание виртуального сетевого шлюза с конфигурацией проверки подлинности AAD для VpnClient виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="7225b-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="7225b-130">Выше создается группа ресурсов, запрашивается общедоступный IP-адрес, создается виртуальная сеть и подсеть, а также создается виртуальный сетевой шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="7225b-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7225b-131">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Запад Великобритании" с ранее созданными конфигурациями IP-адресов, сохраненными в переменной ngwIPConfig, типом шлюза VPN, VPN-типом RouteBased и sku "Basic".</span><span class="sxs-lookup"><span data-stu-id="7225b-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="7225b-132">Она также настраивает конфигурации проверки подлинности AAD: AadTenantUri, AadIssuerUri и AadAudienceId для VpnClient виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="7225b-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="7225b-133">Пример 5. Создание виртуального сетевого шлюза с помощью VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="7225b-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="7225b-134">Выше создается группа ресурсов, запрашивается общедоступный IP-адрес, создается виртуальная сеть и подсеть, а также создается виртуальный сетевой шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="7225b-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7225b-135">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Запад Великобритании" с ранее созданными конфигурациями IP-адресов, сохраненными в переменной ngwIPConfig, типом шлюза VPN, VPN-типом RouteBased, sku "VpnGw4" и VpnGatewayGeneration Generation2.</span><span class="sxs-lookup"><span data-stu-id="7225b-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="7225b-136">Пример 6. Создание виртуального сетевого шлюза с помощью IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="7225b-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="7225b-137">Выше создается группа ресурсов, запрашивается общедоступный IP-адрес, создается виртуальная сеть и подсеть, а также создается виртуальный сетевой шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="7225b-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7225b-138">ipconfigurationId1 только что созданной и сохраненной в ngwipconfig шлюза.</span><span class="sxs-lookup"><span data-stu-id="7225b-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="7225b-139">Шлюз будет называться "Шлюз1" в группе ресурсов "resourcegroup1resourcegroup1" в расположении "Западная Часть Великобритании" с ранее созданным адресом Bgppeering ip configurations, сохраненным в переменной gw1ipconfBgp1, тип шлюза "VPN", VPN-тип "RouteBased", sku "VpnGw4" и VpnGatewayGeneration Generation2.</span><span class="sxs-lookup"><span data-stu-id="7225b-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="7225b-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7225b-140">PARAMETERS</span></span>

### <span data-ttu-id="7225b-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="7225b-141">-AadAudienceId</span></span>
<span data-ttu-id="7225b-142">Параметр проверки подлинности AAD P2S:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="7225b-142">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="7225b-143">-AadIssuerUri</span></span>
<span data-ttu-id="7225b-144">Параметр проверки подлинности AAD P2S:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="7225b-144">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="7225b-145">-AadTenantUri</span></span>
<span data-ttu-id="7225b-146">Параметр проверки подлинности AAD P2S:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="7225b-146">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7225b-147">-AsJob</span></span>
<span data-ttu-id="7225b-148">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7225b-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7225b-149">-Asn</span><span class="sxs-lookup"><span data-stu-id="7225b-149">-Asn</span></span>
<span data-ttu-id="7225b-150">ASN виртуального сетевого шлюза для BGP через VPN</span><span class="sxs-lookup"><span data-stu-id="7225b-150">The virtual network gateway's ASN for BGP over VPN</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="7225b-151">-CustomRoute</span></span>
<span data-ttu-id="7225b-152">Настраиваемые маршруты AddressPool, заданные клиентом</span><span class="sxs-lookup"><span data-stu-id="7225b-152">Custom routes AddressPool specified by customer</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7225b-153">-DefaultProfile</span></span>
<span data-ttu-id="7225b-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7225b-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7225b-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="7225b-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="7225b-156">Пометка для того, чтобы включить активную функцию на виртуальном сетевом шлюзе</span><span class="sxs-lookup"><span data-stu-id="7225b-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7225b-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7225b-157">-EnableBgp</span></span>
<span data-ttu-id="7225b-158">Флаг EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7225b-158">EnableBgp Flag</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7225b-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="7225b-160">Пометка для того, чтобы включить частный IPAddress в виртуальном сетевом шлюзе</span><span class="sxs-lookup"><span data-stu-id="7225b-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="7225b-161">-Force</span><span class="sxs-lookup"><span data-stu-id="7225b-161">-Force</span></span>
<span data-ttu-id="7225b-162">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="7225b-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7225b-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7225b-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="7225b-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7225b-164">GatewayDefaultSite</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="7225b-165">-GatewaySku</span></span>
<span data-ttu-id="7225b-166">Уровень SKU шлюза</span><span class="sxs-lookup"><span data-stu-id="7225b-166">The Gateway Sku Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="7225b-167">-GatewayType</span></span>
<span data-ttu-id="7225b-168">Тип виртуального сетевого шлюза: Vpn, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7225b-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="7225b-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="7225b-170">BgpPeeringAddresses для виртуальных сетевых шлюзов bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="7225b-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="7225b-171">-IpConfigurations</span></span>
<span data-ttu-id="7225b-172">IpConfigurations для виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="7225b-172">The IpConfigurations for Virtual network gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-173">-Location</span><span class="sxs-lookup"><span data-stu-id="7225b-173">-Location</span></span>
<span data-ttu-id="7225b-174">расположение.</span><span class="sxs-lookup"><span data-stu-id="7225b-174">location.</span></span>

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

### <span data-ttu-id="7225b-175">-Name</span><span class="sxs-lookup"><span data-stu-id="7225b-175">-Name</span></span>
<span data-ttu-id="7225b-176">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="7225b-176">The resource name.</span></span>

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

### <span data-ttu-id="7225b-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="7225b-177">-PeerWeight</span></span>
<span data-ttu-id="7225b-178">Вес, добавленный для маршрутов, которые были узнать через BGP из этого виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="7225b-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="7225b-179">-RadiusServerAddress</span></span>
<span data-ttu-id="7225b-180">Адрес сервера внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="7225b-180">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="7225b-181">-RadiusServerList</span></span>
<span data-ttu-id="7225b-182">Несколько внешних серверов радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="7225b-182">P2S multiple external Radius server servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="7225b-183">-RadiusServerSecret</span></span>
<span data-ttu-id="7225b-184">Секрет внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="7225b-184">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7225b-185">-ResourceGroupName</span></span>
<span data-ttu-id="7225b-186">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7225b-186">The resource group name.</span></span>

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

### <span data-ttu-id="7225b-187">-Tag</span><span class="sxs-lookup"><span data-stu-id="7225b-187">-Tag</span></span>
<span data-ttu-id="7225b-188">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="7225b-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7225b-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="7225b-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="7225b-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="7225b-190">P2S VpnClient AddressPool</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="7225b-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="7225b-192">Список политик IPSec для протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="7225b-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="7225b-193">-VpnClientProtocol</span></span>
<span data-ttu-id="7225b-194">Список протоколов туннелинга VPN-клиентов P2S</span><span class="sxs-lookup"><span data-stu-id="7225b-194">The list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="7225b-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="7225b-196">Список VPNClientCertificates для отзыва.</span><span class="sxs-lookup"><span data-stu-id="7225b-196">The list of VpnClientCertificates to be revoked.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="7225b-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="7225b-198">Список vpnClientRootCertificates, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="7225b-198">The list of VpnClientRootCertificates to be added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="7225b-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="7225b-200">Новое поколение для этого VPN-шлюза VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="7225b-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="7225b-201">Если GatewayType не является VPN, не должно быть none (Нет).</span><span class="sxs-lookup"><span data-stu-id="7225b-201">Must be None if GatewayType is not VPN.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="7225b-202">-VpnType</span></span>
<span data-ttu-id="7225b-203">Тип vpn:PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="7225b-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7225b-204">-Confirm</span></span>
<span data-ttu-id="7225b-205">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7225b-205">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7225b-206">-WhatIf</span></span>
<span data-ttu-id="7225b-207">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7225b-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7225b-208">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7225b-208">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7225b-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7225b-209">CommonParameters</span></span>
<span data-ttu-id="7225b-210">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7225b-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7225b-211">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7225b-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7225b-212">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7225b-212">INPUTS</span></span>

### <span data-ttu-id="7225b-213">System.String</span><span class="sxs-lookup"><span data-stu-id="7225b-213">System.String</span></span>

### <span data-ttu-id="7225b-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="7225b-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="7225b-215">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7225b-215">System.Boolean</span></span>

### <span data-ttu-id="7225b-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7225b-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="7225b-217">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7225b-217">System.String[]</span></span>

### <span data-ttu-id="7225b-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="7225b-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="7225b-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="7225b-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="7225b-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="7225b-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="7225b-221">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="7225b-221">System.UInt32</span></span>

### <span data-ttu-id="7225b-222">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7225b-222">System.Int32</span></span>

### <span data-ttu-id="7225b-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="7225b-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="7225b-224">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7225b-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7225b-225">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="7225b-225">System.Security.SecureString</span></span>

## <span data-ttu-id="7225b-226">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7225b-226">OUTPUTS</span></span>

### <span data-ttu-id="7225b-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7225b-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7225b-228">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7225b-228">NOTES</span></span>

## <span data-ttu-id="7225b-229">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7225b-229">RELATED LINKS</span></span>
