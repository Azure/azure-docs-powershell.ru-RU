---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: e5216d3a5727c32bd5e9f185cd48ace068a890b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065133"
---
# <span data-ttu-id="a2ce7-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2ce7-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a2ce7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ce7-103">Обновление шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="a2ce7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2ce7-104">SYNTAX</span></span>

### <span data-ttu-id="a2ce7-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2ce7-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2ce7-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2ce7-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ce7-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="a2ce7-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ce7-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="a2ce7-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2ce7-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="a2ce7-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2ce7-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2ce7-110">DESCRIPTION</span></span>
<span data-ttu-id="a2ce7-111">Командлет **Set-AzVirtualNetworkGateway** обновляет шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="a2ce7-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2ce7-112">EXAMPLES</span></span>

### <span data-ttu-id="a2ce7-113">Пример 1: обновление ASN для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="a2ce7-114">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда обновляет шлюз виртуальной сети, хранящийся в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="a2ce7-115">Команда также задает для ASN значение 1337.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="a2ce7-116">Пример 2: Добавление политики IPsec к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="a2ce7-117">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда создает объект политики IP-безопасности VPN в соответствии с заданными параметрами IPsec.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="a2ce7-118">Третья команда обновляет шлюз виртуальной сети, хранящийся в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="a2ce7-119">Эта команда также задает настраиваемую политику IPSec для VPN, указанную в объекте $vpnclientipsecpolicy в шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="a2ce7-120">Пример 3: Добавление и обновление тегов для существующего шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
```

<span data-ttu-id="a2ce7-121">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда обновляет Gateway01 шлюза виртуальных сетей с помощью тегов @ {testtagKey = "SomeTagKey"; testtagValue = «SomeKeyValue»}.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="a2ce7-122">Пример 4: Добавление и обновление конфигурации проверки подлинности AAD для VpnClient существующего шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
                         Name          Value
                         ============  ============
                         testtagValue  SomeKeyValue
                         testtagKey    SomeTagKey

IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/MyVnet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/Gateway001Ip"
                             },
                             "Name": "vng1ipConfig",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/Gateway001IpConfig"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
vpnClientConfiguration : {
                    "vpnClientProtocols": [
                    "OpenVPN"
                    ],

                    "vpnClientAddressPool": {
                    "addressPrefixes": [
                        "101.10.0.0/16"
                    ]
                    },
                    "vpnClientRootCertificates": "",
                    "vpnClientRevokedCertificates": "",

                    "radiusServerAddress": "",
                    "radiusServerSecret": "",
                    "aadTenantUri": "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4\",
                    "aadAudienceId": "a21fce82-76af-45e6-8583-a08cb3b956g9\",
                    "aadIssuerUri": "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/\"
                },
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "1.2.3.4",
                           "PeerWeight": 0
                         }
                         
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientRootCertificates $rootCert -RemoveAadAuthentication
```

<span data-ttu-id="a2ce7-123">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда обновляет параметры шлюза виртуальной сети Gateway01 с параметрами проверки подлинности AAD: aadTenantUri, aadAudienceId, aadIssuerUri для VpnClient.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="a2ce7-124">Третья команда удаляет конфигурацию проверки подлинности AAD из VpnClient шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="a2ce7-125">Пример 5: Добавление и обновление IpConfigurationBgpPeeringAddresses для существующего шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-125">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\>$ipconfigurationId1 = '/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default'
PS C:\>$addresslist1 = @('169.254.21.25')
PS C:\>$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
PS C:\>Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1

Name                   : Gateway001
ResourceGroupName      : ResourceGroup001
Location               : westcentralus
Id                     : /subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001
Etag                   : W/"a08f13d3-6106-44e0-9127-e35e6f9793d5"
ResourceGuid           : 30993429-a1ed-42ca-9862-9156b013626e
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworks/newApipaNet/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/publicIPAddresses/newapipaip"
                             },
                             "Name": "default",
                             "Etag": "W/\"a08f13d3-6106-44e0-9127-e35e6f9793d5\"",
                             "Id": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "10.1.255.30",
                           "PeerWeight": 0,
                           "BgpPeeringAddresses": [
                             {
                               "IpconfigurationId": "/subscriptions/59ac12a6-f2b7-46d4-af3d-98ba9d9dbd92/resourceGroups/ResourceGroup001/providers/Microsoft.Network/virtualNetworkGateways/Gateway001/ipConfigurations/default",
                               "DefaultBgpIpAddresses": [
                                 "10.1.255.30"
                               ],
                               "CustomBgpIpAddresses": [
                                 "169.254.21.55"
                               ],
                               "TunnelIpAddresses": [
                                 "13.78.146.151"
                               ]
                             }
                           ]
                         }
```

<span data-ttu-id="a2ce7-126">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда присваивает значение ИД IP-адресу шлюза виртуальных сетей Gateway01 в переменную ipconfigurationId1.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-126">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="a2ce7-127">Третья команда назначает список адресов в addresslist1.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-127">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="a2ce7-128">Четвертая команда создала объект PSIpConfigurationBgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-128">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="a2ce7-129">Пятая команда задали для этого нового созданного PSIpConfigurationBgpPeeringAddress значение IpConfigurationBgpPeeringAddresses и обновить шлюз.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-129">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="a2ce7-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2ce7-130">PARAMETERS</span></span>

### <span data-ttu-id="a2ce7-131">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="a2ce7-131">-AadAudienceId</span></span>
<span data-ttu-id="a2ce7-132">Режим проверки подлинности AAD P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-132">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="a2ce7-133">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="a2ce7-133">-AadIssuerUri</span></span>
<span data-ttu-id="a2ce7-134">Режим проверки подлинности AAD P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-134">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="a2ce7-135">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="a2ce7-135">-AadTenantUri</span></span>
<span data-ttu-id="a2ce7-136">Режим проверки подлинности AAD P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-136">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="a2ce7-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2ce7-137">-AsJob</span></span>
<span data-ttu-id="a2ce7-138">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a2ce7-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2ce7-139">-ASN</span><span class="sxs-lookup"><span data-stu-id="a2ce7-139">-Asn</span></span>
<span data-ttu-id="a2ce7-140">ASN шлюза виртуальной сети, используемый для настройки сеансов BGP в туннелях IPsec.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-140">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="a2ce7-141">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="a2ce7-141">-CustomRoute</span></span>
<span data-ttu-id="a2ce7-142">Пользовательские маршруты AddressPool, указанные клиентом</span><span class="sxs-lookup"><span data-stu-id="a2ce7-142">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="a2ce7-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ce7-143">-DefaultProfile</span></span>
<span data-ttu-id="a2ce7-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2ce7-145">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="a2ce7-145">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="a2ce7-146">Пометка отключения активного активного компонента на шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-146">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="a2ce7-147">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="a2ce7-147">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="a2ce7-148">Пометка для включения активной функции в шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-148">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="a2ce7-149">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a2ce7-149">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="a2ce7-150">Пометка для включения активной функции в шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-150">Flag to enable Active Active feature on virtual network gateway</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ce7-151">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a2ce7-151">-GatewayDefaultSite</span></span>
<span data-ttu-id="a2ce7-152">Сайт по умолчанию, используемый для принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-152">The default site to use for force tunneling.</span></span>
<span data-ttu-id="a2ce7-153">Если указан сайт по умолчанию, весь Интернет-трафик из виртуальной сети шлюза пересылается на этот сайт.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-153">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="a2ce7-154">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="a2ce7-154">-GatewaySku</span></span>
<span data-ttu-id="a2ce7-155">SKU шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-155">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="a2ce7-156">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="a2ce7-156">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="a2ce7-157">BgpPeeringAddresses для шлюза виртуальной сети bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-157">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="a2ce7-158">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="a2ce7-158">-PeerWeight</span></span>
<span data-ttu-id="a2ce7-159">Вес, добавленный в маршруты, полученные по протоколу BGP из этого шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a2ce7-159">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="a2ce7-160">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a2ce7-160">-RadiusServerAddress</span></span>
<span data-ttu-id="a2ce7-161">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-161">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ce7-162">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a2ce7-162">-RadiusServerSecret</span></span>
<span data-ttu-id="a2ce7-163">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-163">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration, RadiusServerConfigurationUpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ce7-164">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a2ce7-164">-RemoveAadAuthentication</span></span>
<span data-ttu-id="a2ce7-165">Пометка для удаления проверки подлинности AAD для клиента P2S из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-165">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="a2ce7-166">-Тег</span><span class="sxs-lookup"><span data-stu-id="a2ce7-166">-Tag</span></span>
<span data-ttu-id="a2ce7-167">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-167">P2S External Radius server address.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: RadiusServerConfigurationUpdateResourceWithTags, UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ce7-168">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2ce7-168">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a2ce7-169">Объект шлюза виртуальной сети, для которого изменяются основные изменения.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-169">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="a2ce7-170">Это можно получить с помощью Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2ce7-170">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ce7-171">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="a2ce7-171">-VpnClientAddressPool</span></span>
<span data-ttu-id="a2ce7-172">Адресное пространство, из которого нужно выделять IP-адреса VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-172">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="a2ce7-173">Это не должно перекрываться с помощью виртуальной сети или локальных диапазонов.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-173">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="a2ce7-174">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a2ce7-174">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a2ce7-175">Список политик IPSec для протоколов туннелирования VPN-клиента P2S.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-175">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a2ce7-176">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="a2ce7-176">-VpnClientProtocol</span></span>
<span data-ttu-id="a2ce7-177">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="a2ce7-177">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="a2ce7-178">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="a2ce7-178">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="a2ce7-179">Список отозванных сертификатов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-179">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="a2ce7-180">VPN-клиент, выступающий сертификат, совпадающий с одним из них, будет указан для выхода.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-180">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="a2ce7-181">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="a2ce7-181">-VpnClientRootCertificates</span></span>
<span data-ttu-id="a2ce7-182">Список корневых сертификатов VPN-клиентов, используемых для проверки подлинности клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-182">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="a2ce7-183">Подключение VPN-клиентов должно представлять сертификаты, созданные на основе одного из этих корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-183">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="a2ce7-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2ce7-184">-Confirm</span></span>
<span data-ttu-id="a2ce7-185">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2ce7-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2ce7-186">-WhatIf</span></span>
<span data-ttu-id="a2ce7-187">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2ce7-188">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2ce7-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ce7-189">CommonParameters</span></span>
<span data-ttu-id="a2ce7-190">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2ce7-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ce7-191">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2ce7-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ce7-192">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2ce7-192">INPUTS</span></span>

### <span data-ttu-id="a2ce7-193">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2ce7-193">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a2ce7-194">System. String</span><span class="sxs-lookup"><span data-stu-id="a2ce7-194">System.String</span></span>

### <span data-ttu-id="a2ce7-195">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2ce7-195">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="a2ce7-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="a2ce7-196">System.String[]</span></span>

### <span data-ttu-id="a2ce7-197">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="a2ce7-197">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="a2ce7-198">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="a2ce7-198">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="a2ce7-199">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="a2ce7-199">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="a2ce7-200">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="a2ce7-200">System.UInt32</span></span>

### <span data-ttu-id="a2ce7-201">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a2ce7-201">System.Int32</span></span>

### <span data-ttu-id="a2ce7-202">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="a2ce7-202">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="a2ce7-203">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a2ce7-203">System.Security.SecureString</span></span>

## <span data-ttu-id="a2ce7-204">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2ce7-204">OUTPUTS</span></span>

### <span data-ttu-id="a2ce7-205">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a2ce7-205">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a2ce7-206">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2ce7-206">NOTES</span></span>

## <span data-ttu-id="a2ce7-207">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2ce7-207">RELATED LINKS</span></span>
