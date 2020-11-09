---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9a18a995c79e744d4da366c59b621c1313048913
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318554"
---
# <span data-ttu-id="28d6d-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28d6d-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="28d6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28d6d-102">SYNOPSIS</span></span>
<span data-ttu-id="28d6d-103">Обновление шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="28d6d-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="28d6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28d6d-104">SYNTAX</span></span>

### <span data-ttu-id="28d6d-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28d6d-105">Default (Default)</span></span>
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

### <span data-ttu-id="28d6d-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="28d6d-106">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="28d6d-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="28d6d-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
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

### <span data-ttu-id="28d6d-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="28d6d-108">MultipleRadiusServersConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-EnableActiveActiveFeature]
 [-EnablePrivateIpAddress <Boolean>] [-DisableActiveActiveFeature] -RadiusServerList <PSRadiusServer[]>
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28d6d-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="28d6d-109">AadAuthenticationConfiguration</span></span>
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

### <span data-ttu-id="28d6d-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="28d6d-110">UpdateResourceWithTags</span></span>
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

## <span data-ttu-id="28d6d-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28d6d-111">DESCRIPTION</span></span>
<span data-ttu-id="28d6d-112">Командлет **Set-AzVirtualNetworkGateway** обновляет шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="28d6d-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="28d6d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28d6d-113">EXAMPLES</span></span>

### <span data-ttu-id="28d6d-114">Пример 1: обновление ASN для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="28d6d-115">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда обновляет шлюз виртуальной сети, хранящийся в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="28d6d-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="28d6d-116">Команда также задает для ASN значение 1337.</span><span class="sxs-lookup"><span data-stu-id="28d6d-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="28d6d-117">Пример 2: Добавление политики IPsec к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="28d6d-118">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда создает объект политики IP-безопасности VPN в соответствии с заданными параметрами IPsec.</span><span class="sxs-lookup"><span data-stu-id="28d6d-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="28d6d-119">Третья команда обновляет шлюз виртуальной сети, хранящийся в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="28d6d-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="28d6d-120">Эта команда также задает настраиваемую политику IPSec для VPN, указанную в объекте $vpnclientipsecpolicy в шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="28d6d-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="28d6d-121">Пример 3: Добавление и обновление тегов для существующего шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="28d6d-122">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда обновляет Gateway01 шлюза виртуальных сетей с помощью тегов @ {testtagKey = "SomeTagKey"; testtagValue = «SomeKeyValue»}.</span><span class="sxs-lookup"><span data-stu-id="28d6d-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="28d6d-123">Пример 4: Добавление и обновление конфигурации проверки подлинности AAD для VpnClient существующего шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="28d6d-124">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда обновляет параметры шлюза виртуальной сети Gateway01 с параметрами проверки подлинности AAD: aadTenantUri, aadAudienceId, aadIssuerUri для VpnClient.</span><span class="sxs-lookup"><span data-stu-id="28d6d-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="28d6d-125">Третья команда удаляет конфигурацию проверки подлинности AAD из VpnClient шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="28d6d-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="28d6d-126">Пример 5: Добавление и обновление IpConfigurationBgpPeeringAddresses для существующего шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
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

<span data-ttu-id="28d6d-127">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда присваивает значение ИД IP-адресу шлюза виртуальных сетей Gateway01 в переменную ipconfigurationId1.</span><span class="sxs-lookup"><span data-stu-id="28d6d-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="28d6d-128">Третья команда назначает список адресов в addresslist1.</span><span class="sxs-lookup"><span data-stu-id="28d6d-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="28d6d-129">Четвертая команда создала объект PSIpConfigurationBgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="28d6d-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="28d6d-130">Пятая команда задали для этого нового созданного PSIpConfigurationBgpPeeringAddress значение IpConfigurationBgpPeeringAddresses и обновить шлюз.</span><span class="sxs-lookup"><span data-stu-id="28d6d-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="28d6d-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28d6d-131">PARAMETERS</span></span>

### <span data-ttu-id="28d6d-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="28d6d-132">-AadAudienceId</span></span>
<span data-ttu-id="28d6d-133">Режим проверки подлинности AAD P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="28d6d-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="28d6d-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="28d6d-134">-AadIssuerUri</span></span>
<span data-ttu-id="28d6d-135">Режим проверки подлинности AAD P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="28d6d-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="28d6d-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="28d6d-136">-AadTenantUri</span></span>
<span data-ttu-id="28d6d-137">Режим проверки подлинности AAD P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="28d6d-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="28d6d-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28d6d-138">-AsJob</span></span>
<span data-ttu-id="28d6d-139">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="28d6d-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28d6d-140">-ASN</span><span class="sxs-lookup"><span data-stu-id="28d6d-140">-Asn</span></span>
<span data-ttu-id="28d6d-141">ASN шлюза виртуальной сети, используемый для настройки сеансов BGP в туннелях IPsec.</span><span class="sxs-lookup"><span data-stu-id="28d6d-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="28d6d-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="28d6d-142">-CustomRoute</span></span>
<span data-ttu-id="28d6d-143">Пользовательские маршруты AddressPool, указанные клиентом</span><span class="sxs-lookup"><span data-stu-id="28d6d-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="28d6d-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d6d-144">-DefaultProfile</span></span>
<span data-ttu-id="28d6d-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28d6d-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28d6d-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="28d6d-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="28d6d-147">Пометка отключения активного активного компонента на шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="28d6d-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="28d6d-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="28d6d-149">Пометка для включения активной функции в шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="28d6d-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="28d6d-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="28d6d-151">Пометка для включения активной функции в шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-151">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="28d6d-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="28d6d-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="28d6d-153">Сайт по умолчанию, используемый для принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="28d6d-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="28d6d-154">Если указан сайт по умолчанию, весь Интернет-трафик из виртуальной сети шлюза пересылается на этот сайт.</span><span class="sxs-lookup"><span data-stu-id="28d6d-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="28d6d-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="28d6d-155">-GatewaySku</span></span>
<span data-ttu-id="28d6d-156">SKU шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="28d6d-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="28d6d-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="28d6d-158">BgpPeeringAddresses для шлюза виртуальной сети bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="28d6d-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="28d6d-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="28d6d-159">-PeerWeight</span></span>
<span data-ttu-id="28d6d-160">Вес, добавленный в маршруты, полученные по протоколу BGP из этого шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="28d6d-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="28d6d-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="28d6d-161">-RadiusServerAddress</span></span>
<span data-ttu-id="28d6d-162">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="28d6d-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="28d6d-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="28d6d-163">-RadiusServerList</span></span>
<span data-ttu-id="28d6d-164">P2S несколько внешних RADIUS-серверов.</span><span class="sxs-lookup"><span data-stu-id="28d6d-164">P2S multiple external Radius servers.</span></span>

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

### <span data-ttu-id="28d6d-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="28d6d-165">-RadiusServerSecret</span></span>
<span data-ttu-id="28d6d-166">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="28d6d-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="28d6d-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="28d6d-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="28d6d-168">Пометка для удаления проверки подлинности AAD для клиента P2S из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="28d6d-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="28d6d-169">-Тег</span><span class="sxs-lookup"><span data-stu-id="28d6d-169">-Tag</span></span>
<span data-ttu-id="28d6d-170">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="28d6d-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="28d6d-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28d6d-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="28d6d-172">Объект шлюза виртуальной сети, для которого изменяются основные изменения.</span><span class="sxs-lookup"><span data-stu-id="28d6d-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="28d6d-173">Это можно получить с помощью Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28d6d-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="28d6d-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="28d6d-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="28d6d-175">Адресное пространство, из которого нужно выделять IP-адреса VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="28d6d-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="28d6d-176">Это не должно перекрываться с помощью виртуальной сети или локальных диапазонов.</span><span class="sxs-lookup"><span data-stu-id="28d6d-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="28d6d-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="28d6d-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="28d6d-178">Список политик IPSec для протоколов туннелирования VPN-клиента P2S.</span><span class="sxs-lookup"><span data-stu-id="28d6d-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="28d6d-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="28d6d-179">-VpnClientProtocol</span></span>
<span data-ttu-id="28d6d-180">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="28d6d-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="28d6d-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="28d6d-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="28d6d-182">Список отозванных сертификатов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="28d6d-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="28d6d-183">VPN-клиент, выступающий сертификат, совпадающий с одним из них, будет указан для выхода.</span><span class="sxs-lookup"><span data-stu-id="28d6d-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="28d6d-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="28d6d-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="28d6d-185">Список корневых сертификатов VPN-клиентов, используемых для проверки подлинности клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="28d6d-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="28d6d-186">Подключение VPN-клиентов должно представлять сертификаты, созданные на основе одного из этих корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="28d6d-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="28d6d-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28d6d-187">-Confirm</span></span>
<span data-ttu-id="28d6d-188">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28d6d-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28d6d-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d6d-189">-WhatIf</span></span>
<span data-ttu-id="28d6d-190">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28d6d-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28d6d-191">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28d6d-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28d6d-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d6d-192">CommonParameters</span></span>
<span data-ttu-id="28d6d-193">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28d6d-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d6d-194">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28d6d-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d6d-195">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28d6d-195">INPUTS</span></span>

### <span data-ttu-id="28d6d-196">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28d6d-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="28d6d-197">System. String</span><span class="sxs-lookup"><span data-stu-id="28d6d-197">System.String</span></span>

### <span data-ttu-id="28d6d-198">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28d6d-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="28d6d-199">System. String []</span><span class="sxs-lookup"><span data-stu-id="28d6d-199">System.String[]</span></span>

### <span data-ttu-id="28d6d-200">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="28d6d-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="28d6d-201">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="28d6d-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="28d6d-202">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="28d6d-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="28d6d-203">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="28d6d-203">System.UInt32</span></span>

### <span data-ttu-id="28d6d-204">System. Int32</span><span class="sxs-lookup"><span data-stu-id="28d6d-204">System.Int32</span></span>

### <span data-ttu-id="28d6d-205">Microsoft. Azure. Commands. Network. Models. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="28d6d-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="28d6d-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="28d6d-206">System.Security.SecureString</span></span>

## <span data-ttu-id="28d6d-207">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28d6d-207">OUTPUTS</span></span>

### <span data-ttu-id="28d6d-208">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="28d6d-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="28d6d-209">Пуск</span><span class="sxs-lookup"><span data-stu-id="28d6d-209">NOTES</span></span>

## <span data-ttu-id="28d6d-210">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28d6d-210">RELATED LINKS</span></span>
