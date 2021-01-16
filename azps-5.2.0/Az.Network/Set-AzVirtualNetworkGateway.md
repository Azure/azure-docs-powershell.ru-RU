---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9a18a995c79e744d4da366c59b621c1313048913
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392303"
---
# <span data-ttu-id="a1dda-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1dda-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a1dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1dda-102">SYNOPSIS</span></span>
<span data-ttu-id="a1dda-103">Обновляет виртуальный сетевой шлюз.</span><span class="sxs-lookup"><span data-stu-id="a1dda-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="a1dda-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1dda-104">SYNTAX</span></span>

### <span data-ttu-id="a1dda-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1dda-105">Default (Default)</span></span>
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

### <span data-ttu-id="a1dda-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1dda-106">RadiusServerConfiguration</span></span>
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

### <span data-ttu-id="a1dda-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="a1dda-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
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

### <span data-ttu-id="a1dda-108">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1dda-108">MultipleRadiusServersConfiguration</span></span>
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

### <span data-ttu-id="a1dda-109">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1dda-109">AadAuthenticationConfiguration</span></span>
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

### <span data-ttu-id="a1dda-110">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="a1dda-110">UpdateResourceWithTags</span></span>
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

## <span data-ttu-id="a1dda-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1dda-111">DESCRIPTION</span></span>
<span data-ttu-id="a1dda-112">Командлет **Set-AzVirtualNetworkGateway** обновляет виртуальный сетевой шлюз.</span><span class="sxs-lookup"><span data-stu-id="a1dda-112">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="a1dda-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1dda-113">EXAMPLES</span></span>

### <span data-ttu-id="a1dda-114">Пример 1. Обновление asN виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="a1dda-114">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="a1dda-115">Первая команда получает виртуальный сетевой шлюз с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда обновляет виртуальный сетевой шлюз, который хранится в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="a1dda-115">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="a1dda-116">Команда также задает для asN 1337.</span><span class="sxs-lookup"><span data-stu-id="a1dda-116">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="a1dda-117">Пример 2. Добавление политики IPsec к виртуальному сетевому шлюзу</span><span class="sxs-lookup"><span data-stu-id="a1dda-117">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="a1dda-118">Первая команда получает виртуальный сетевой шлюз Gateway01, который принадлежит к группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда создает объект политики Ipsec Vpn в указанном параметре ipsec.</span><span class="sxs-lookup"><span data-stu-id="a1dda-118">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="a1dda-119">Третья команда обновляет виртуальный сетевой шлюз, который хранится в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="a1dda-119">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="a1dda-120">Команда также задает настраиваемую политику ipsec VPN, заданную в объекте $vpnclientipsecpolicy виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="a1dda-120">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="a1dda-121">Пример 3. Добавление и обновление тегов для существующего виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="a1dda-121">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="a1dda-122">Первая команда получает виртуальный сетевой шлюз Gateway01, который принадлежит к группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда обновляет виртуальный сетевой шлюз Gateway01 с помощью тегов @{ testkey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span><span class="sxs-lookup"><span data-stu-id="a1dda-122">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="a1dda-123">Пример 4. Настройка проверки подлинности AAD для VpnClient существующего виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="a1dda-123">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="a1dda-124">Первая команда получает виртуальный сетевой шлюз Gateway01, который принадлежит к группе ресурсов ResourceGroup001, и сохраняет его в переменной $Gateway Вторая команда обновляет виртуальный сетевой шлюз Gateway01, используя параметры проверки подлинности AAD:aadTenantUri, aadAudienceId, aadIssuerUri для VpnClient.</span><span class="sxs-lookup"><span data-stu-id="a1dda-124">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="a1dda-125">Третья команда удаляет конфигурацию проверки подлинности AAD из VpnClient виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="a1dda-125">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="a1dda-126">Пример 5. Добавление и обновление IpConfigurationBgpPeeringAddresses для существующего виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="a1dda-126">Example 5: Add/Update IpConfigurationBgpPeeringAddresses to an existing virtual network gateway</span></span>
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

<span data-ttu-id="a1dda-127">Первая команда получает виртуальный сетевой шлюз Gateway01, который принадлежит к группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда назначает значение виртуального сетевого шлюза Gateway01 IpConfiguration Id в переменную ipconfigurationId1.</span><span class="sxs-lookup"><span data-stu-id="a1dda-127">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command assigns the value of virtual network gateway Gateway01 IpConfiguration Id into variable ipconfigurationId1.</span></span>
<span data-ttu-id="a1dda-128">Третья команда назначает список адресов списку адресов в список адресов1.</span><span class="sxs-lookup"><span data-stu-id="a1dda-128">The third command assigns the address list into addresslist1.</span></span>
<span data-ttu-id="a1dda-129">Четвертая команда создает объект PSIpConfigurationBgpPeeringAddress.</span><span class="sxs-lookup"><span data-stu-id="a1dda-129">The fourth command created a PSIpConfigurationBgpPeeringAddress object.</span></span>
<span data-ttu-id="a1dda-130">Пятая команда, задав созданную командой PSIpConfigurationBgpPeeringAddress для IpConfigurationBgpPeeringAddresses и обновив шлюз.</span><span class="sxs-lookup"><span data-stu-id="a1dda-130">The fifth command set this new created PSIpConfigurationBgpPeeringAddress to IpConfigurationBgpPeeringAddresses and update the gateway.</span></span>

## <span data-ttu-id="a1dda-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1dda-131">PARAMETERS</span></span>

### <span data-ttu-id="a1dda-132">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="a1dda-132">-AadAudienceId</span></span>
<span data-ttu-id="a1dda-133">Параметр проверки подлинности AAD P2S:AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="a1dda-133">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="a1dda-134">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="a1dda-134">-AadIssuerUri</span></span>
<span data-ttu-id="a1dda-135">Параметр проверки подлинности AAD P2S:AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="a1dda-135">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="a1dda-136">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="a1dda-136">-AadTenantUri</span></span>
<span data-ttu-id="a1dda-137">Параметр проверки подлинности AAD P2S:AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="a1dda-137">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="a1dda-138">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1dda-138">-AsJob</span></span>
<span data-ttu-id="a1dda-139">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a1dda-139">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1dda-140">-Asn</span><span class="sxs-lookup"><span data-stu-id="a1dda-140">-Asn</span></span>
<span data-ttu-id="a1dda-141">AsN виртуального сетевого шлюза, используемая для настроить сеансы BGP в туннельх IPsec.</span><span class="sxs-lookup"><span data-stu-id="a1dda-141">The virtual network gateway's ASN, used to set up BGP sessions inside IPsec tunnels</span></span>

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

### <span data-ttu-id="a1dda-142">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="a1dda-142">-CustomRoute</span></span>
<span data-ttu-id="a1dda-143">Настраиваемые маршруты AddressPool, заданные клиентом</span><span class="sxs-lookup"><span data-stu-id="a1dda-143">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="a1dda-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1dda-144">-DefaultProfile</span></span>
<span data-ttu-id="a1dda-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dda-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1dda-146">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="a1dda-146">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="a1dda-147">Пометка для отключения активной функции в виртуальном сетевом шлюзе</span><span class="sxs-lookup"><span data-stu-id="a1dda-147">Flag to disable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="a1dda-148">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="a1dda-148">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="a1dda-149">Пометка для того, чтобы включить активную функцию на виртуальном сетевом шлюзе</span><span class="sxs-lookup"><span data-stu-id="a1dda-149">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="a1dda-150">-EnablePrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a1dda-150">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="a1dda-151">Пометка для того, чтобы включить активную функцию на виртуальном сетевом шлюзе</span><span class="sxs-lookup"><span data-stu-id="a1dda-151">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="a1dda-152">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a1dda-152">-GatewayDefaultSite</span></span>
<span data-ttu-id="a1dda-153">Стандартный сайт для принудительного туннелинга.</span><span class="sxs-lookup"><span data-stu-id="a1dda-153">The default site to use for force tunneling.</span></span>
<span data-ttu-id="a1dda-154">Если задан сайт по умолчанию, весь интернет-трафик из сети VNET шлюза маршрутизируется на этот сайт.</span><span class="sxs-lookup"><span data-stu-id="a1dda-154">If a default site is specified, all internet traffic from the gateway's vnet is routed to that site.</span></span>

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

### <span data-ttu-id="a1dda-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="a1dda-155">-GatewaySku</span></span>
<span data-ttu-id="a1dda-156">SKU виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="a1dda-156">The virtual network gateway's SKU</span></span>

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

### <span data-ttu-id="a1dda-157">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="a1dda-157">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="a1dda-158">BgpPeeringAddresses для виртуальных сетевых шлюзов bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="a1dda-158">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

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

### <span data-ttu-id="a1dda-159">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="a1dda-159">-PeerWeight</span></span>
<span data-ttu-id="a1dda-160">Вес, добавленный для маршрутов, которые были узнать через BGP из этого виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="a1dda-160">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="a1dda-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a1dda-161">-RadiusServerAddress</span></span>
<span data-ttu-id="a1dda-162">Адрес сервера внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="a1dda-162">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="a1dda-163">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="a1dda-163">-RadiusServerList</span></span>
<span data-ttu-id="a1dda-164">Несколько внешних серверов радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="a1dda-164">P2S multiple external Radius servers.</span></span>

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

### <span data-ttu-id="a1dda-165">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a1dda-165">-RadiusServerSecret</span></span>
<span data-ttu-id="a1dda-166">Секрет внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="a1dda-166">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="a1dda-167">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a1dda-167">-RemoveAadAuthentication</span></span>
<span data-ttu-id="a1dda-168">Пометить, чтобы удалить проверку подлинности AAD для клиента P2S из виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="a1dda-168">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="a1dda-169">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1dda-169">-Tag</span></span>
<span data-ttu-id="a1dda-170">Адрес сервера внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="a1dda-170">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="a1dda-171">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1dda-171">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a1dda-172">Объект виртуального сетевого шлюза, относя который к базовым изменениями.</span><span class="sxs-lookup"><span data-stu-id="a1dda-172">The virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="a1dda-173">Это можно получить с помощью Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1dda-173">This can be retrieved using Get-AzVirtualNetworkGateway</span></span>

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

### <span data-ttu-id="a1dda-174">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="a1dda-174">-VpnClientAddressPool</span></span>
<span data-ttu-id="a1dda-175">Адресное пространство для выделения IP-адресов клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="a1dda-175">The address space to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="a1dda-176">Она не должна перекрываться с виртуальными сетевыми или локальной диапазонами.</span><span class="sxs-lookup"><span data-stu-id="a1dda-176">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="a1dda-177">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a1dda-177">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a1dda-178">Список политик IPSec для протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="a1dda-178">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="a1dda-179">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="a1dda-179">-VpnClientProtocol</span></span>
<span data-ttu-id="a1dda-180">A list of P2S VPN client tunneling protocols</span><span class="sxs-lookup"><span data-stu-id="a1dda-180">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="a1dda-181">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="a1dda-181">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="a1dda-182">Список отозванных сертификатов клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="a1dda-182">A list of revoked VPN client certificates.</span></span>
<span data-ttu-id="a1dda-183">Vpn-клиент с сертификатом, который соответствует одному из этих, будет выдан, чтобы выйти.</span><span class="sxs-lookup"><span data-stu-id="a1dda-183">A VPN client presenting a certificate that matches one of these will be told to go away.</span></span>

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

### <span data-ttu-id="a1dda-184">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="a1dda-184">-VpnClientRootCertificates</span></span>
<span data-ttu-id="a1dda-185">Список корневых сертификатов клиента VPN, которые нужно использовать для проверки подлинности клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="a1dda-185">A list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="a1dda-186">Подключение VPN-клиентов должно представлять сертификаты, созданные на основе одного из этих корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a1dda-186">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="a1dda-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1dda-187">-Confirm</span></span>
<span data-ttu-id="a1dda-188">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1dda-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1dda-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1dda-189">-WhatIf</span></span>
<span data-ttu-id="a1dda-190">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1dda-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1dda-191">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a1dda-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1dda-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1dda-192">CommonParameters</span></span>
<span data-ttu-id="a1dda-193">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1dda-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1dda-194">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1dda-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1dda-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1dda-195">INPUTS</span></span>

### <span data-ttu-id="a1dda-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1dda-196">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a1dda-197">System.String</span><span class="sxs-lookup"><span data-stu-id="a1dda-197">System.String</span></span>

### <span data-ttu-id="a1dda-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1dda-198">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="a1dda-199">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a1dda-199">System.String[]</span></span>

### <span data-ttu-id="a1dda-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span><span class="sxs-lookup"><span data-stu-id="a1dda-200">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="a1dda-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span><span class="sxs-lookup"><span data-stu-id="a1dda-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="a1dda-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="a1dda-202">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="a1dda-203">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="a1dda-203">System.UInt32</span></span>

### <span data-ttu-id="a1dda-204">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a1dda-204">System.Int32</span></span>

### <span data-ttu-id="a1dda-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span><span class="sxs-lookup"><span data-stu-id="a1dda-205">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="a1dda-206">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="a1dda-206">System.Security.SecureString</span></span>

## <span data-ttu-id="a1dda-207">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1dda-207">OUTPUTS</span></span>

### <span data-ttu-id="a1dda-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a1dda-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a1dda-209">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1dda-209">NOTES</span></span>

## <span data-ttu-id="a1dda-210">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1dda-210">RELATED LINKS</span></span>
