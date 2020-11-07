---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: df3b8df85cd53931de5da7dc710e4558aedcdd48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904377"
---
# <span data-ttu-id="d5abe-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d5abe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5abe-102">SYNOPSIS</span></span>
<span data-ttu-id="d5abe-103">Обновление шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5abe-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="d5abe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5abe-104">SYNTAX</span></span>

### <span data-ttu-id="d5abe-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5abe-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5abe-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5abe-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5abe-107">RadiusServerConfigurationUpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="d5abe-107">RadiusServerConfigurationUpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5abe-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5abe-108">AadAuthenticationConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-RemoveAadAuthentication]
 [-CustomRoute <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5abe-109">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="d5abe-109">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-RemoveAadAuthentication] [-CustomRoute <String[]>] -Tag <Hashtable> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5abe-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5abe-110">DESCRIPTION</span></span>
<span data-ttu-id="d5abe-111">Командлет **Set-AzVirtualNetworkGateway** обновляет шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5abe-111">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="d5abe-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5abe-112">EXAMPLES</span></span>

### <span data-ttu-id="d5abe-113">Пример 1: обновление ASN для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d5abe-113">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="d5abe-114">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда обновляет шлюз виртуальной сети, хранящийся в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="d5abe-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="d5abe-115">Команда также задает для ASN значение 1337.</span><span class="sxs-lookup"><span data-stu-id="d5abe-115">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="d5abe-116">Пример 2: Добавление политики IPsec к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d5abe-116">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="d5abe-117">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway Вторая команда создает объект политики IP-безопасности VPN в соответствии с заданными параметрами IPsec.</span><span class="sxs-lookup"><span data-stu-id="d5abe-117">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="d5abe-118">Третья команда обновляет шлюз виртуальной сети, хранящийся в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="d5abe-118">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="d5abe-119">Эта команда также задает настраиваемую политику IPSec для VPN, указанную в объекте $vpnclientipsecpolicy в шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5abe-119">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

### <span data-ttu-id="d5abe-120">Пример 3: Добавление и обновление тегов для существующего шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d5abe-120">Example 3: Add/Update Tags to an existing virtual network gateway</span></span>
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

<span data-ttu-id="d5abe-121">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда обновляет Gateway01 шлюза виртуальных сетей с помощью тегов @ {testtagKey = "SomeTagKey"; testtagValue = «SomeKeyValue»}.</span><span class="sxs-lookup"><span data-stu-id="d5abe-121">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the tags @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }.</span></span>

### <span data-ttu-id="d5abe-122">Пример 4: Добавление и обновление конфигурации проверки подлинности AAD для VpnClient существующего шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d5abe-122">Example 4: Add/Update AAD authentication configuration for VpnClient of an existing virtual network gateway</span></span>
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

<span data-ttu-id="d5abe-123">Первая команда получает шлюз виртуальной сети с именем Gateway01, который принадлежит группе ресурсов ResourceGroup001, и сохраняет его в переменной с именем $Gateway Вторая команда обновляет параметры шлюза виртуальной сети Gateway01 с параметрами проверки подлинности AAD: aadTenantUri, aadAudienceId, aadIssuerUri для VpnClient.</span><span class="sxs-lookup"><span data-stu-id="d5abe-123">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway Gateway01 with the AAD authentication configurations params:aadTenantUri, aadAudienceId, aadIssuerUri for VpnClient.</span></span>
<span data-ttu-id="d5abe-124">Третья команда удаляет конфигурацию проверки подлинности AAD из VpnClient шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5abe-124">The third command removes the AAD authentication configuration from VpnClient of virtual network gateway.</span></span>

## <span data-ttu-id="d5abe-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5abe-125">PARAMETERS</span></span>

### <span data-ttu-id="d5abe-126">-AadAudienceId</span><span class="sxs-lookup"><span data-stu-id="d5abe-126">-AadAudienceId</span></span>
<span data-ttu-id="d5abe-127">Режим проверки подлинности AAD P2S: AadAudienceId.</span><span class="sxs-lookup"><span data-stu-id="d5abe-127">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="d5abe-128">-AadIssuerUri</span><span class="sxs-lookup"><span data-stu-id="d5abe-128">-AadIssuerUri</span></span>
<span data-ttu-id="d5abe-129">Режим проверки подлинности AAD P2S: AadIssuerUri.</span><span class="sxs-lookup"><span data-stu-id="d5abe-129">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="d5abe-130">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="d5abe-130">-AadTenantUri</span></span>
<span data-ttu-id="d5abe-131">Режим проверки подлинности AAD P2S: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="d5abe-131">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="d5abe-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5abe-132">-AsJob</span></span>
<span data-ttu-id="d5abe-133">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d5abe-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5abe-134">-ASN</span><span class="sxs-lookup"><span data-stu-id="d5abe-134">-Asn</span></span>
<span data-ttu-id="d5abe-135">Задает номер автономной системы шлюза виртуальной сети (ASN), который используется для настройки сеансов BGP в туннелях IPsec.</span><span class="sxs-lookup"><span data-stu-id="d5abe-135">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="d5abe-136">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="d5abe-136">-CustomRoute</span></span>
<span data-ttu-id="d5abe-137">Пользовательские маршруты AddressPool, указанные клиентом</span><span class="sxs-lookup"><span data-stu-id="d5abe-137">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="d5abe-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5abe-138">-DefaultProfile</span></span>
<span data-ttu-id="d5abe-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5abe-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5abe-140">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d5abe-140">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="d5abe-141">Отключение активного активного компонента.</span><span class="sxs-lookup"><span data-stu-id="d5abe-141">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="d5abe-142">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d5abe-142">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="d5abe-143">Включает функцию активный активный компонент.</span><span class="sxs-lookup"><span data-stu-id="d5abe-143">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="d5abe-144">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d5abe-144">-GatewayDefaultSite</span></span>
<span data-ttu-id="d5abe-145">Указывает сайт по умолчанию, который будет использоваться для принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="d5abe-145">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="d5abe-146">Если указан сайт по умолчанию, весь Интернет-трафик от виртуальной частной сети (VPN) шлюза пересылается на этот сайт.</span><span class="sxs-lookup"><span data-stu-id="d5abe-146">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="d5abe-147">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="d5abe-147">-GatewaySku</span></span>
<span data-ttu-id="d5abe-148">Задает единицу хранения (SKU) шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5abe-148">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="d5abe-149">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d5abe-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d5abe-150">Базового</span><span class="sxs-lookup"><span data-stu-id="d5abe-150">Basic</span></span>
- <span data-ttu-id="d5abe-151">Стандартная</span><span class="sxs-lookup"><span data-stu-id="d5abe-151">Standard</span></span>
- <span data-ttu-id="d5abe-152">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="d5abe-152">HighPerformance</span></span>
- <span data-ttu-id="d5abe-153">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="d5abe-153">VpnGw1</span></span>
- <span data-ttu-id="d5abe-154">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="d5abe-154">VpnGw2</span></span>
- <span data-ttu-id="d5abe-155">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="d5abe-155">VpnGw3</span></span>
- <span data-ttu-id="d5abe-156">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d5abe-156">VpnGw1AZ</span></span>
- <span data-ttu-id="d5abe-157">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d5abe-157">VpnGw2AZ</span></span>
- <span data-ttu-id="d5abe-158">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d5abe-158">VpnGw3AZ</span></span>
- <span data-ttu-id="d5abe-159">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="d5abe-159">ErGw1AZ</span></span>
- <span data-ttu-id="d5abe-160">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="d5abe-160">ErGw2AZ</span></span>
- <span data-ttu-id="d5abe-161">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="d5abe-161">ErGw3AZ</span></span>

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

### <span data-ttu-id="d5abe-162">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d5abe-162">-PeerWeight</span></span>
<span data-ttu-id="d5abe-163">Указывает вес, добавленный в маршруты, полученные по протоколу BGP из этого шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5abe-163">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="d5abe-164">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d5abe-164">-RadiusServerAddress</span></span>
<span data-ttu-id="d5abe-165">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="d5abe-165">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="d5abe-166">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d5abe-166">-RadiusServerSecret</span></span>
<span data-ttu-id="d5abe-167">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="d5abe-167">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="d5abe-168">-RemoveAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="d5abe-168">-RemoveAadAuthentication</span></span>
<span data-ttu-id="d5abe-169">Пометка для удаления проверки подлинности AAD для клиента P2S из шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5abe-169">Flag to remove AAD authentication for P2S client from virtual network gateway.</span></span>

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

### <span data-ttu-id="d5abe-170">-Тег</span><span class="sxs-lookup"><span data-stu-id="d5abe-170">-Tag</span></span>
<span data-ttu-id="d5abe-171">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5abe-171">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d5abe-172">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-172">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d5abe-173">Указывает объект шлюза виртуальной сети, для которого изменяются базовые изменения.</span><span class="sxs-lookup"><span data-stu-id="d5abe-173">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="d5abe-174">Вы можете использовать командлет Get-AzVirtualNetworkGateway, чтобы получить объект шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5abe-174">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="d5abe-175">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d5abe-175">-VpnClientAddressPool</span></span>
<span data-ttu-id="d5abe-176">Указывает адресное пространство, используемое этим командлетом для выделения IP-адресов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="d5abe-176">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="d5abe-177">Это не должно перекрываться с помощью виртуальной сети или локальных диапазонов.</span><span class="sxs-lookup"><span data-stu-id="d5abe-177">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="d5abe-178">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d5abe-178">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="d5abe-179">Список политик IPSec для протоколов туннелирования VPN-клиента P2S.</span><span class="sxs-lookup"><span data-stu-id="d5abe-179">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d5abe-180">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="d5abe-180">-VpnClientProtocol</span></span>
<span data-ttu-id="d5abe-181">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="d5abe-181">A list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="d5abe-182">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="d5abe-182">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="d5abe-183">Указывает список отозванных сертификатов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="d5abe-183">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="d5abe-184">VPN-клиент, выступающий сертификат, совпадающий с одним из них, удаляется.</span><span class="sxs-lookup"><span data-stu-id="d5abe-184">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="d5abe-185">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="d5abe-185">-VpnClientRootCertificates</span></span>
<span data-ttu-id="d5abe-186">Указывает список корневых сертификатов VPN-клиентов, используемых для проверки подлинности клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="d5abe-186">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="d5abe-187">Подключение VPN-клиентов должно представлять сертификаты, созданные на основе одного из этих корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d5abe-187">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="d5abe-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5abe-188">-Confirm</span></span>
<span data-ttu-id="d5abe-189">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d5abe-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5abe-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5abe-190">-WhatIf</span></span>
<span data-ttu-id="d5abe-191">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d5abe-191">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5abe-192">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d5abe-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5abe-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5abe-193">CommonParameters</span></span>
<span data-ttu-id="d5abe-194">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5abe-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5abe-195">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5abe-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5abe-196">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5abe-196">INPUTS</span></span>

### <span data-ttu-id="d5abe-197">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-197">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d5abe-198">System. String</span><span class="sxs-lookup"><span data-stu-id="d5abe-198">System.String</span></span>

### <span data-ttu-id="d5abe-199">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-199">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="d5abe-200">System. String []</span><span class="sxs-lookup"><span data-stu-id="d5abe-200">System.String[]</span></span>

### <span data-ttu-id="d5abe-201">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="d5abe-201">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="d5abe-202">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="d5abe-202">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="d5abe-203">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="d5abe-203">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="d5abe-204">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="d5abe-204">System.UInt32</span></span>

### <span data-ttu-id="d5abe-205">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d5abe-205">System.Int32</span></span>

### <span data-ttu-id="d5abe-206">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d5abe-206">System.Security.SecureString</span></span>

## <span data-ttu-id="d5abe-207">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5abe-207">OUTPUTS</span></span>

### <span data-ttu-id="d5abe-208">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-208">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d5abe-209">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5abe-209">NOTES</span></span>
* <span data-ttu-id="d5abe-210">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="d5abe-210">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d5abe-211">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5abe-211">RELATED LINKS</span></span>

[<span data-ttu-id="d5abe-212">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-212">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d5abe-213">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-213">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d5abe-214">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-214">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d5abe-215">Сброс — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-215">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d5abe-216">Изменить размер — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5abe-216">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
