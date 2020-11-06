---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 6f0a18211ae7c9d2fe8ffcb9c653de9952691e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567440"
---
# <span data-ttu-id="40c44-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40c44-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="40c44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40c44-102">SYNOPSIS</span></span>
<span data-ttu-id="40c44-103">Создание шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="40c44-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40c44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40c44-104">SYNTAX</span></span>

### <span data-ttu-id="40c44-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40c44-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40c44-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="40c44-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40c44-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="40c44-107">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40c44-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40c44-108">DESCRIPTION</span></span>
<span data-ttu-id="40c44-109">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="40c44-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="40c44-110">Командлет **New-AzureRmVirtualNetworkGateway** создает объект шлюза в Azure на основе имени, имени группы ресурсов, расположения и IP-конфигурации, а также типа шлюза и VPN-типа.</span><span class="sxs-lookup"><span data-stu-id="40c44-110">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="40c44-111">Вы также можете присвоить имя SKU Gateway.</span><span class="sxs-lookup"><span data-stu-id="40c44-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="40c44-112">Если этот шлюз используется для подключений между сайтами, необходимо также включить пул адресов VPN-клиента, из которого будут назначаться адреса для подключения клиентов и корневой сертификат VPN-клиента, который используется для проверки подлинности VPN-клиентов, подключающихся к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="40c44-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="40c44-113">Вы также можете включить другие функции, такие как BGP и Active-Active.</span><span class="sxs-lookup"><span data-stu-id="40c44-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="40c44-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40c44-114">EXAMPLES</span></span>

### <span data-ttu-id="40c44-115">1: Создание шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="40c44-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="40c44-116">В описанном выше примере будет создана группа ресурсов, запрос общедоступного IP-адреса, создание виртуальной сети и подсети и создание шлюза виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="40c44-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="40c44-117">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Великобритания" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", тип шлюза "VPN", тип VPN "RouteBased" и SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="40c44-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="40c44-118">2. Создание шлюза виртуальной сети с внешней конфигурацией RADIUS</span><span class="sxs-lookup"><span data-stu-id="40c44-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="40c44-119">В описанном выше примере будет создана группа ресурсов, запрос общедоступного IP-адреса, создание виртуальной сети и подсети и создание шлюза виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="40c44-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="40c44-120">Шлюз будет называться "myNGW" в группе ресурсов "vnet-шлюз" в расположении "Великобритания" с ранее созданными конфигурациями IP, сохраненными в переменной "ngwIPConfig", тип шлюза "VPN", тип VPN "RouteBased" и SKU "Basic".</span><span class="sxs-lookup"><span data-stu-id="40c44-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="40c44-121">Кроме того, он добавляет внешний RADIUS-сервер с адресом "TestRadiusServer".</span><span class="sxs-lookup"><span data-stu-id="40c44-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="40c44-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40c44-122">PARAMETERS</span></span>

### <span data-ttu-id="40c44-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40c44-123">-AsJob</span></span>
<span data-ttu-id="40c44-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="40c44-124">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-125">-ASN</span><span class="sxs-lookup"><span data-stu-id="40c44-125">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c44-126">-DefaultProfile</span></span>
<span data-ttu-id="40c44-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40c44-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-128">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="40c44-128">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="40c44-129">Включает функцию активный активный компонент.</span><span class="sxs-lookup"><span data-stu-id="40c44-129">Enables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-130">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="40c44-130">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-131">-Force</span><span class="sxs-lookup"><span data-stu-id="40c44-131">-Force</span></span>
<span data-ttu-id="40c44-132">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="40c44-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-133">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="40c44-133">-GatewayDefaultSite</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-134">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="40c44-134">-GatewaySku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-135">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="40c44-135">-GatewayType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-136">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="40c44-136">-IpConfigurations</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-137">-Location</span><span class="sxs-lookup"><span data-stu-id="40c44-137">-Location</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40c44-138">-Name</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-139">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="40c44-139">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-140">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="40c44-140">-RadiusServerAddress</span></span>
<span data-ttu-id="40c44-141">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="40c44-141">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="40c44-142">-RadiusServerSecret</span></span>
<span data-ttu-id="40c44-143">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="40c44-143">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40c44-144">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-145">-Тег</span><span class="sxs-lookup"><span data-stu-id="40c44-145">-Tag</span></span>
<span data-ttu-id="40c44-146">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="40c44-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="40c44-147">Например:</span><span class="sxs-lookup"><span data-stu-id="40c44-147">For example:</span></span>

<span data-ttu-id="40c44-148">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="40c44-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-149">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="40c44-149">-VpnClientAddressPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-150">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="40c44-150">-VpnClientProtocol</span></span>
<span data-ttu-id="40c44-151">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="40c44-151">The list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-152">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="40c44-152">-VpnClientRevokedCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-153">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="40c44-153">-VpnClientRootCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-154">-VpnType</span><span class="sxs-lookup"><span data-stu-id="40c44-154">-VpnType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40c44-155">-Confirm</span></span>
<span data-ttu-id="40c44-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40c44-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40c44-157">-WhatIf</span></span>
<span data-ttu-id="40c44-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40c44-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40c44-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40c44-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c44-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c44-160">CommonParameters</span></span>
<span data-ttu-id="40c44-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40c44-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c44-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40c44-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c44-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40c44-163">INPUTS</span></span>

### <span data-ttu-id="40c44-164">Ничего</span><span class="sxs-lookup"><span data-stu-id="40c44-164">None</span></span>
<span data-ttu-id="40c44-165">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="40c44-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40c44-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40c44-166">OUTPUTS</span></span>

### <span data-ttu-id="40c44-167">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40c44-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="40c44-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="40c44-168">NOTES</span></span>

## <span data-ttu-id="40c44-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40c44-169">RELATED LINKS</span></span>

[<span data-ttu-id="40c44-170">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40c44-170">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="40c44-171">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40c44-171">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="40c44-172">Сброс — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40c44-172">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="40c44-173">Изменить размер — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40c44-173">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="40c44-174">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="40c44-174">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
