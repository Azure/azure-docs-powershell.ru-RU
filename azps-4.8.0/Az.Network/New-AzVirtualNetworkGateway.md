---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244354"
---
# <span data-ttu-id="f8d1a-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8d1a-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f8d1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d1a-103">Создание шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f8d1a-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="f8d1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8d1a-104">SYNTAX</span></span>

### <span data-ttu-id="f8d1a-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8d1a-105">Default (Default)</span></span>
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

### <span data-ttu-id="f8d1a-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8d1a-106">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="f8d1a-107">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8d1a-107">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="f8d1a-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8d1a-108">AadAuthenticationConfiguration</span></span>
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

## <span data-ttu-id="f8d1a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8d1a-109">DESCRIPTION</span></span>
<span data-ttu-id="f8d1a-110">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f8d1a-111">Командлет **New-AzVirtualNetworkGateway** создает объект шлюза в Azure на основе имени, имени группы ресурсов, расположения и IP-конфигурации, а также типа шлюза и VPN-типа.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="f8d1a-112">Вы также можете присвоить имя SKU Gateway.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="f8d1a-113">Если этот шлюз используется для подключений между сайтами, необходимо также включить пул адресов VPN-клиента, из которого будут назначаться адреса для подключения клиентов и корневой сертификат VPN-клиента, который используется для проверки подлинности VPN-клиентов, подключающихся к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="f8d1a-114">Вы также можете включить другие функции, такие как BGP и Active-Active.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="f8d1a-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8d1a-115">EXAMPLES</span></span>

### <span data-ttu-id="f8d1a-116">Пример 1: Создание шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f8d1a-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="f8d1a-117">В описанном выше примере будет создана группа ресурсов, запрос общедоступного IP-адреса, создание виртуальной сети и подсети и создание шлюза виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f8d1a-118">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Великобритания" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", тип шлюза "VPN", тип VPN "RouteBased" и SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="f8d1a-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="f8d1a-119">Пример 2: Создание шлюза виртуальной сети с внешней конфигурацией RADIUS</span><span class="sxs-lookup"><span data-stu-id="f8d1a-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
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

<span data-ttu-id="f8d1a-120">В описанном выше примере будет создана группа ресурсов, запрос общедоступного IP-адреса, создание виртуальной сети и подсети и создание шлюза виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f8d1a-121">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Великобритания" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", тип шлюза "VPN", тип VPN "RouteBased" и SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="f8d1a-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f8d1a-122">Кроме того, он добавляет внешний RADIUS-сервер с адресом "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="f8d1a-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="f8d1a-123">Кроме того, будут заданы пользовательские маршруты, заданные пользователями на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f8d1a-124">Пример 3: Создание шлюза виртуальной сети с параметрами P2S</span><span class="sxs-lookup"><span data-stu-id="f8d1a-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
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

<span data-ttu-id="f8d1a-125">В описанном выше примере создается группа ресурсов, запрашивается общедоступный IP-адрес, создается виртуальная сеть и подсеть и создается шлюз виртуальных сетей с параметрами P2S, например VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy и. в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="f8d1a-126">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Великобритания" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", тип шлюза "VPN", тип VPN "RouteBased" и SKU "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="f8d1a-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="f8d1a-127">Параметры VPN будут заданы для шлюза, например VpnProtocol Set as Ikev2, VpnClientAddressPool как "201.169.0.0/16", VpnClientRootCertificate задается как отправленный один: clientRootCertName и настраиваемая политика IPSec для VPN, переданная в объект: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="f8d1a-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="f8d1a-128">Кроме того, будут заданы пользовательские маршруты, заданные пользователями на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="f8d1a-129">Пример 4: Создание шлюза виртуальной сети с конфигурацией проверки подлинности AAD для VpnClient шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
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

<span data-ttu-id="f8d1a-130">В описанном выше примере будет создана группа ресурсов, запрос общедоступного IP-адреса, создание виртуальной сети и подсети и создание шлюза виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f8d1a-131">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Великобритания" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", тип шлюза "VPN", тип VPN "RouteBased" и SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="f8d1a-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="f8d1a-132">Кроме того, настраиваются конфигурации проверки подлинности AAD: AadTenantUri, AadIssuerUri и AadAudienceId для VpnClient шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="f8d1a-133">Пример 5: Создание шлюза виртуальной сети с помощью VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="f8d1a-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="f8d1a-134">В описанном выше примере будет создана группа ресурсов, запрос общедоступного IP-адреса, создание виртуальной сети и подсети и создание шлюза виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f8d1a-135">Шлюз будет называться "myNGW" в группе ресурсов "vnet — шлюз" в местоположении "Великобритания-Gateway" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", типом шлюза "VPN", VPN-типом "RouteBased", SKU "VpnGw4" и VpnGatewayGeneration Generation2.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="f8d1a-136">Пример 6: Создание шлюза виртуальной сети с помощью IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="f8d1a-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
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

<span data-ttu-id="f8d1a-137">В описанном выше примере будет создана группа ресурсов, запрос общедоступного IP-адреса, создание виртуальной сети и подсети и создание шлюза виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f8d1a-138">ipconfigurationId1 IP Gateway, только что создан и сохранен в ngwipconfig.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="f8d1a-139">Шлюз будет называться "gateway1" в группе ресурсов "resourcegroup1resourcegroup1" в расположении "Великобритания Запад" с ранее созданными настройками IP-адресов Bgppeering, сохраненными в переменной "gw1ipconfBgp1", типом шлюза "VPN", VPN-типом "RouteBased", SKU "VpnGw4" и VpnGatewayGeneration Generation2.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="f8d1a-140">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8d1a-140">PARAMETERS</span></span>

### <span data-ttu-id="f8d1a-141">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="f8d1a-141">-AadAudienceId</span></span>
<span data-ttu-id="f8d1a-142">Режим проверки подлинности AAD P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="f8d1a-143">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="f8d1a-143">-AadIssuerUri</span></span>
<span data-ttu-id="f8d1a-144">Режим проверки подлинности AAD P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="f8d1a-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="f8d1a-145">-AadTenantUri</span></span>
<span data-ttu-id="f8d1a-146">Режим проверки подлинности AAD P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="f8d1a-147">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8d1a-147">-AsJob</span></span>
<span data-ttu-id="f8d1a-148">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f8d1a-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8d1a-149">-ASN</span><span class="sxs-lookup"><span data-stu-id="f8d1a-149">-Asn</span></span>
<span data-ttu-id="f8d1a-150">ASN для виртуального сетевого шлюза в BGP для VPN</span><span class="sxs-lookup"><span data-stu-id="f8d1a-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="f8d1a-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="f8d1a-151">-CustomRoute</span></span>
<span data-ttu-id="f8d1a-152">Пользовательские маршруты AddressPool, указанные клиентом</span><span class="sxs-lookup"><span data-stu-id="f8d1a-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="f8d1a-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d1a-153">-DefaultProfile</span></span>
<span data-ttu-id="f8d1a-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8d1a-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="f8d1a-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="f8d1a-156">Пометка для включения активной функции в шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f8d1a-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="f8d1a-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f8d1a-157">-EnableBgp</span></span>
<span data-ttu-id="f8d1a-158">Флаг EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f8d1a-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="f8d1a-159">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f8d1a-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="f8d1a-160">Флаг для включения личного IP-адреса в шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f8d1a-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="f8d1a-161">-Force</span><span class="sxs-lookup"><span data-stu-id="f8d1a-161">-Force</span></span>
<span data-ttu-id="f8d1a-162">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="f8d1a-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f8d1a-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f8d1a-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="f8d1a-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="f8d1a-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="f8d1a-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="f8d1a-165">-GatewaySku</span></span>
<span data-ttu-id="f8d1a-166">Уровень SKU Gateway</span><span class="sxs-lookup"><span data-stu-id="f8d1a-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="f8d1a-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="f8d1a-167">-GatewayType</span></span>
<span data-ttu-id="f8d1a-168">Тип шлюза виртуальной сети: VPN, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f8d1a-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="f8d1a-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="f8d1a-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="f8d1a-170">BgpPeeringAddresses для шлюза виртуальной сети bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="f8d1a-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="f8d1a-171">-IpConfigurations</span></span>
<span data-ttu-id="f8d1a-172">IpConfigurations для шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="f8d1a-173">-Location</span><span class="sxs-lookup"><span data-stu-id="f8d1a-173">-Location</span></span>
<span data-ttu-id="f8d1a-174">поиска.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-174">location.</span></span>

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

### <span data-ttu-id="f8d1a-175">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8d1a-175">-Name</span></span>
<span data-ttu-id="f8d1a-176">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-176">The resource name.</span></span>

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

### <span data-ttu-id="f8d1a-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="f8d1a-177">-PeerWeight</span></span>
<span data-ttu-id="f8d1a-178">Вес, добавленный в маршруты, полученные по протоколу BGP из этого шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f8d1a-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="f8d1a-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="f8d1a-179">-RadiusServerAddress</span></span>
<span data-ttu-id="f8d1a-180">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="f8d1a-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="f8d1a-181">-RadiusServerList</span></span>
<span data-ttu-id="f8d1a-182">P2S несколько внешних серверных серверов RADIUS.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-182">P2S multiple external Radius server servers.</span></span>

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

### <span data-ttu-id="f8d1a-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="f8d1a-183">-RadiusServerSecret</span></span>
<span data-ttu-id="f8d1a-184">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="f8d1a-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d1a-185">-ResourceGroupName</span></span>
<span data-ttu-id="f8d1a-186">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-186">The resource group name.</span></span>

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

### <span data-ttu-id="f8d1a-187">-Тег</span><span class="sxs-lookup"><span data-stu-id="f8d1a-187">-Tag</span></span>
<span data-ttu-id="f8d1a-188">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f8d1a-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="f8d1a-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="f8d1a-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="f8d1a-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="f8d1a-191">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f8d1a-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="f8d1a-192">Список политик IPSec для протоколов туннелирования VPN-клиента P2S.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="f8d1a-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="f8d1a-193">-VpnClientProtocol</span></span>
<span data-ttu-id="f8d1a-194">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="f8d1a-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="f8d1a-195">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="f8d1a-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="f8d1a-196">Список VpnClientCertificates, который нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="f8d1a-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="f8d1a-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="f8d1a-198">Список VpnClientRootCertificates, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="f8d1a-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="f8d1a-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="f8d1a-200">Создание для этого VirtualNetwork VPN-шлюза.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="f8d1a-201">Если GatewayType не является VPN, должно быть значение None (нет).</span><span class="sxs-lookup"><span data-stu-id="f8d1a-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="f8d1a-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="f8d1a-202">-VpnType</span></span>
<span data-ttu-id="f8d1a-203">Тип VPN: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="f8d1a-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="f8d1a-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8d1a-204">-Confirm</span></span>
<span data-ttu-id="f8d1a-205">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8d1a-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d1a-206">-WhatIf</span></span>
<span data-ttu-id="f8d1a-207">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8d1a-208">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8d1a-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d1a-209">CommonParameters</span></span>
<span data-ttu-id="f8d1a-210">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8d1a-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d1a-211">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8d1a-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d1a-212">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8d1a-212">INPUTS</span></span>

### <span data-ttu-id="f8d1a-213">System. String</span><span class="sxs-lookup"><span data-stu-id="f8d1a-213">System.String</span></span>

### <span data-ttu-id="f8d1a-214">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f8d1a-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="f8d1a-215">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8d1a-215">System.Boolean</span></span>

### <span data-ttu-id="f8d1a-216">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8d1a-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="f8d1a-217">System. String []</span><span class="sxs-lookup"><span data-stu-id="f8d1a-217">System.String[]</span></span>

### <span data-ttu-id="f8d1a-218">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="f8d1a-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="f8d1a-219">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="f8d1a-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="f8d1a-220">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="f8d1a-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f8d1a-221">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="f8d1a-221">System.UInt32</span></span>

### <span data-ttu-id="f8d1a-222">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f8d1a-222">System.Int32</span></span>

### <span data-ttu-id="f8d1a-223">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="f8d1a-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="f8d1a-224">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f8d1a-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f8d1a-225">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="f8d1a-225">System.Security.SecureString</span></span>

## <span data-ttu-id="f8d1a-226">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8d1a-226">OUTPUTS</span></span>

### <span data-ttu-id="f8d1a-227">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f8d1a-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f8d1a-228">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8d1a-228">NOTES</span></span>

## <span data-ttu-id="f8d1a-229">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8d1a-229">RELATED LINKS</span></span>
