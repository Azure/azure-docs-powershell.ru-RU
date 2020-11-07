---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 9b8ee02cbe28784ff1fd5789881dd62add62d674
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730261"
---
# <span data-ttu-id="99f9c-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="99f9c-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="99f9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="99f9c-103">Создание шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="99f9c-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="99f9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99f9c-104">SYNTAX</span></span>

### <span data-ttu-id="99f9c-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99f9c-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f9c-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="99f9c-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99f9c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99f9c-107">DESCRIPTION</span></span>
<span data-ttu-id="99f9c-108">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="99f9c-108">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="99f9c-109">Командлет **New-AzVirtualNetworkGateway** создает объект шлюза в Azure на основе имени, имени группы ресурсов, расположения и IP-конфигурации, а также типа шлюза и VPN-типа.</span><span class="sxs-lookup"><span data-stu-id="99f9c-109">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="99f9c-110">Вы также можете присвоить имя SKU Gateway.</span><span class="sxs-lookup"><span data-stu-id="99f9c-110">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="99f9c-111">Если этот шлюз используется для подключений между сайтами, необходимо также включить пул адресов VPN-клиента, из которого будут назначаться адреса для подключения клиентов и корневой сертификат VPN-клиента, который используется для проверки подлинности VPN-клиентов, подключающихся к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="99f9c-111">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="99f9c-112">Вы также можете включить другие функции, такие как BGP и Active-Active.</span><span class="sxs-lookup"><span data-stu-id="99f9c-112">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="99f9c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99f9c-113">EXAMPLES</span></span>

### <span data-ttu-id="99f9c-114">1: Создание шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="99f9c-114">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="99f9c-115">В описанном выше примере будет создана группа ресурсов, запрос общедоступного IP-адреса, создание виртуальной сети и подсети и создание шлюза виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="99f9c-115">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="99f9c-116">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Великобритания" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", тип шлюза "VPN", тип VPN "RouteBased" и SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="99f9c-116">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="99f9c-117">2. Создание шлюза виртуальной сети с внешней конфигурацией RADIUS</span><span class="sxs-lookup"><span data-stu-id="99f9c-117">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="99f9c-118">В описанном выше примере будет создана группа ресурсов, запрос общедоступного IP-адреса, создание виртуальной сети и подсети и создание шлюза виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="99f9c-118">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="99f9c-119">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Великобритания" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", тип шлюза "VPN", тип VPN "RouteBased" и SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="99f9c-119">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="99f9c-120">Кроме того, он добавляет внешний RADIUS-сервер с адресом "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="99f9c-120">It also adds an external radius server with address "TestRadiusServer"</span></span>

### <span data-ttu-id="99f9c-121">1: Создание шлюза виртуальной сети с параметрами P2S</span><span class="sxs-lookup"><span data-stu-id="99f9c-121">1: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="99f9c-122">В описанном выше примере создается группа ресурсов, запрашивается общедоступный IP-адрес, создается виртуальная сеть и подсеть и создается шлюз виртуальных сетей с параметрами P2S, например VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, VpnClientIpsecPolicy и. в Azure.</span><span class="sxs-lookup"><span data-stu-id="99f9c-122">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="99f9c-123">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Великобритания" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", тип шлюза "VPN", тип VPN "RouteBased" и SKU "VpnGw1".</span><span class="sxs-lookup"><span data-stu-id="99f9c-123">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="99f9c-124">Параметры VPN будут заданы для шлюза, например VpnProtocol Set as Ikev2, VpnClientAddressPool как "201.169.0.0/16", VpnClientRootCertificate задается как отправленный один: clientRootCertName и настраиваемая политика IPSec для VPN, переданная в объект: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="99f9c-124">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  

## <span data-ttu-id="99f9c-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99f9c-125">PARAMETERS</span></span>

### <span data-ttu-id="99f9c-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99f9c-126">-AsJob</span></span>
<span data-ttu-id="99f9c-127">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="99f9c-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99f9c-128">-ASN</span><span class="sxs-lookup"><span data-stu-id="99f9c-128">-Asn</span></span>

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

### <span data-ttu-id="99f9c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f9c-129">-DefaultProfile</span></span>
<span data-ttu-id="99f9c-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99f9c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99f9c-131">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="99f9c-131">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="99f9c-132">Включает функцию активный активный компонент.</span><span class="sxs-lookup"><span data-stu-id="99f9c-132">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="99f9c-133">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="99f9c-133">-EnableBgp</span></span>

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

### <span data-ttu-id="99f9c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="99f9c-134">-Force</span></span>
<span data-ttu-id="99f9c-135">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="99f9c-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99f9c-136">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="99f9c-136">-GatewayDefaultSite</span></span>

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

### <span data-ttu-id="99f9c-137">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="99f9c-137">-GatewaySku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99f9c-138">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="99f9c-138">-GatewayType</span></span>

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

### <span data-ttu-id="99f9c-139">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="99f9c-139">-IpConfigurations</span></span>

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

### <span data-ttu-id="99f9c-140">-Location</span><span class="sxs-lookup"><span data-stu-id="99f9c-140">-Location</span></span>

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

### <span data-ttu-id="99f9c-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99f9c-141">-Name</span></span>

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

### <span data-ttu-id="99f9c-142">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="99f9c-142">-PeerWeight</span></span>

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

### <span data-ttu-id="99f9c-143">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="99f9c-143">-RadiusServerAddress</span></span>
<span data-ttu-id="99f9c-144">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="99f9c-144">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="99f9c-145">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="99f9c-145">-RadiusServerSecret</span></span>
<span data-ttu-id="99f9c-146">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="99f9c-146">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="99f9c-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f9c-147">-ResourceGroupName</span></span>

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

### <span data-ttu-id="99f9c-148">-Тег</span><span class="sxs-lookup"><span data-stu-id="99f9c-148">-Tag</span></span>
<span data-ttu-id="99f9c-149">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="99f9c-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="99f9c-150">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="99f9c-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="99f9c-151">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="99f9c-151">-VpnClientAddressPool</span></span>

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

### <span data-ttu-id="99f9c-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="99f9c-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="99f9c-153">Список политик IPSec для протоколов туннелирования VPN-клиента P2S.</span><span class="sxs-lookup"><span data-stu-id="99f9c-153">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="99f9c-154">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="99f9c-154">-VpnClientProtocol</span></span>
<span data-ttu-id="99f9c-155">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="99f9c-155">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="99f9c-156">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="99f9c-156">-VpnClientRevokedCertificates</span></span>

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

### <span data-ttu-id="99f9c-157">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="99f9c-157">-VpnClientRootCertificates</span></span>

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

### <span data-ttu-id="99f9c-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="99f9c-158">-VpnType</span></span>

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

### <span data-ttu-id="99f9c-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99f9c-159">-Confirm</span></span>
<span data-ttu-id="99f9c-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="99f9c-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f9c-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f9c-161">-WhatIf</span></span>
<span data-ttu-id="99f9c-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="99f9c-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f9c-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="99f9c-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f9c-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f9c-164">CommonParameters</span></span>
<span data-ttu-id="99f9c-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99f9c-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f9c-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f9c-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f9c-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99f9c-167">INPUTS</span></span>

### <span data-ttu-id="99f9c-168">System. String</span><span class="sxs-lookup"><span data-stu-id="99f9c-168">System.String</span></span>

### <span data-ttu-id="99f9c-169">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="99f9c-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="99f9c-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99f9c-170">System.Boolean</span></span>

### <span data-ttu-id="99f9c-171">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="99f9c-171">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="99f9c-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="99f9c-172">System.String[]</span></span>

### <span data-ttu-id="99f9c-173">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="99f9c-173">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="99f9c-174">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="99f9c-174">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="99f9c-175">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="99f9c-175">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="99f9c-176">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="99f9c-176">System.UInt32</span></span>

### <span data-ttu-id="99f9c-177">System. Int32</span><span class="sxs-lookup"><span data-stu-id="99f9c-177">System.Int32</span></span>

### <span data-ttu-id="99f9c-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="99f9c-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="99f9c-179">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="99f9c-179">System.Security.SecureString</span></span>

## <span data-ttu-id="99f9c-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99f9c-180">OUTPUTS</span></span>

### <span data-ttu-id="99f9c-181">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="99f9c-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="99f9c-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="99f9c-182">NOTES</span></span>

## <span data-ttu-id="99f9c-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99f9c-183">RELATED LINKS</span></span>

[<span data-ttu-id="99f9c-184">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="99f9c-184">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="99f9c-185">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="99f9c-185">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="99f9c-186">Сброс — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="99f9c-186">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="99f9c-187">Изменить размер — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="99f9c-187">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="99f9c-188">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="99f9c-188">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
