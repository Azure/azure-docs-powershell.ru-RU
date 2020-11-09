---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnConnection.md
ms.openlocfilehash: 3b7bf41818ded2b866ea72a81ff1c17ccc365358
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244122"
---
# <span data-ttu-id="2d37e-101">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d37e-101">New-AzVpnConnection</span></span>

## <span data-ttu-id="2d37e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d37e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d37e-103">Создает подключение IPSec, которое подключает VpnGateway к удаленной ветви клиента, представленной в диспетчере ресурсов как VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2d37e-103">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="2d37e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d37e-104">SYNTAX</span></span>

### <span data-ttu-id="2d37e-105">ByVpnGatewayNameByVpnSiteObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d37e-105">ByVpnGatewayNameByVpnSiteObject (Default)</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -VpnSite <PSVpnSite> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress]
 [-UsePolicyBasedTrafficSelectors] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d37e-106">ByVpnGatewayNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="2d37e-106">ByVpnGatewayNameByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String> -VpnSiteId <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d37e-107">ByVpnGatewayObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="2d37e-107">ByVpnGatewayObjectByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSite <PSVpnSite>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-VpnConnectionProtocolType <String>] [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d37e-108">ByVpnGatewayObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="2d37e-108">ByVpnGatewayObjectByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentObject <PSVpnGateway> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d37e-109">ByVpnGatewayResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="2d37e-109">ByVpnGatewayResourceIdByVpnSiteObject</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSite <PSVpnSite> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d37e-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="2d37e-110">ByVpnGatewayResourceIdByVpnSiteResourceId</span></span>
```
New-AzVpnConnection -ParentResourceId <String> -Name <String> -VpnSiteId <String> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-VpnConnectionProtocolType <String>]
 [-EnableBgp] [-UseLocalAzureIpAddress] [-UsePolicyBasedTrafficSelectors]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d37e-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d37e-111">DESCRIPTION</span></span>
<span data-ttu-id="2d37e-112">Создает подключение IPSec, которое подключает VpnGateway к удаленной ветви клиента, представленной в диспетчере ресурсов как VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2d37e-112">Creates a IPSec connection that connects a VpnGateway to a remote customer branch represented in RM as a VpnSite.</span></span>

## <span data-ttu-id="2d37e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d37e-113">EXAMPLES</span></span>

### <span data-ttu-id="2d37e-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d37e-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -ConnectionBandwidth 20

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
RoutingConfiguration      : {
                                "AssociatedRouteTable": {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                }
                                "PropagatedRouteTables": {
                                    "Labels": [],
                                    "Ids": [
                                    {
                                    "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                                },
                                "VnetRoutes": {
                                    "StaticRoutes": []
                                }
                            }
```

<span data-ttu-id="2d37e-115">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d37e-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="2d37e-116">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2d37e-116">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="2d37e-117">После создания шлюза он подключается к VpnSite с помощью команды New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="2d37e-117">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

### <span data-ttu-id="2d37e-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2d37e-118">Example 2</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink1 = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSiteLink2 = New-AzVpnSiteLink -Name "testVpnSiteLink2" -IpAddress "15.25.35.55" -LinkProviderName "SomeTelecomProvider2" -LinkSpeedInMbps "100"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink1, $vpnSiteLink2)


PS C:\> $vpnSiteLinkConnection1 = New-AzVpnSiteLinkConnection -Name "testLinkConnection1" -VpnSiteLink $vpnSite.VpnSiteLinks[0] -ConnectionBandwidth 100
PS C:\> $vpnSiteLinkConnection2 = New-AzVpnSiteLinkConnection -Name "testLinkConnection2" -VpnSiteLink $vpnSite.VpnSiteLinks[1] -ConnectionBandwidth 10

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite -VpnSiteLinkConnection @($vpnSiteLinkConnection1, $vpnSiteLinkConnection2)
```

<span data-ttu-id="2d37e-119">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite с 1 VpnSiteLinks (Западная часть США) в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="2d37e-119">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>
<span data-ttu-id="2d37e-120">После этого на виртуальном концентраторе будет создан шлюз VPN.</span><span class="sxs-lookup"><span data-stu-id="2d37e-120">A VPN gateway will be created thereafter in the Virtual Hub.</span></span>
<span data-ttu-id="2d37e-121">После создания шлюза он подключается к VpnSite с помощью команды New-AzVpnConnection с 1 VpnSiteLinkConnections VpnSiteLink VpnSite.</span><span class="sxs-lookup"><span data-stu-id="2d37e-121">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command with 1 VpnSiteLinkConnections to the VpnSiteLink of the VpnSite.</span></span>

## <span data-ttu-id="2d37e-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d37e-122">PARAMETERS</span></span>

### <span data-ttu-id="2d37e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d37e-123">-AsJob</span></span>
<span data-ttu-id="2d37e-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2d37e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d37e-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="2d37e-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="2d37e-126">Пропускная способность, которая должна быть обработана этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="2d37e-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d37e-127">-DefaultProfile</span></span>
<span data-ttu-id="2d37e-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d37e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2d37e-129">-EnableBgp</span></span>
<span data-ttu-id="2d37e-130">Включение BGP для этого подключения</span><span class="sxs-lookup"><span data-stu-id="2d37e-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="2d37e-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2d37e-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="2d37e-132">Включить Интернет-безопасность для этого подключения</span><span class="sxs-lookup"><span data-stu-id="2d37e-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="2d37e-133">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="2d37e-133">-IpSecPolicy</span></span>
<span data-ttu-id="2d37e-134">Пропускная способность, которая должна быть обработана этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="2d37e-134">The bandwidth that needs to be handled by this connection in mbps.</span></span>

```yaml
Type: PSIpsecPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d37e-135">-Name</span></span>
<span data-ttu-id="2d37e-136">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d37e-136">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-137">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2d37e-137">-ParentObject</span></span>
<span data-ttu-id="2d37e-138">Родительский VpnGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="2d37e-138">The parent VpnGateway for this connection.</span></span>

```yaml
Type: PSVpnGateway
Parameter Sets: ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayObjectByVpnSiteResourceId
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-139">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2d37e-139">-ParentResourceId</span></span>
<span data-ttu-id="2d37e-140">Идентификатор ресурса родительского VpnGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="2d37e-140">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayResourceIdByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-141">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="2d37e-141">-ParentResourceName</span></span>
<span data-ttu-id="2d37e-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d37e-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d37e-143">-ResourceGroupName</span></span>
<span data-ttu-id="2d37e-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d37e-144">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d37e-145">-RoutingConfiguration</span></span>
<span data-ttu-id="2d37e-146">Настройка маршрутизации для этого подключения</span><span class="sxs-lookup"><span data-stu-id="2d37e-146">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="2d37e-147">-SharedKey</span></span>
<span data-ttu-id="2d37e-148">Общий ключ, необходимый для настройки этого подключения.</span><span class="sxs-lookup"><span data-stu-id="2d37e-148">The shared key required to set this connection up.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="2d37e-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="2d37e-150">Использовать локальный IP-адрес Azure в качестве исходного адреса при инициализации подключения.</span><span class="sxs-lookup"><span data-stu-id="2d37e-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="2d37e-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="2d37e-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="2d37e-152">Использование селекторов трафика на основе политики для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="2d37e-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="2d37e-153">-VpnConnectionProtocolType</span><span class="sxs-lookup"><span data-stu-id="2d37e-153">-VpnConnectionProtocolType</span></span>
<span data-ttu-id="2d37e-154">Протокол подключения к шлюзу: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="2d37e-154">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-155">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2d37e-155">-VpnSite</span></span>
<span data-ttu-id="2d37e-156">Удаленный сайт VPN, к которому подключено данное виртуальное сетевое подключение к этому концентратору.</span><span class="sxs-lookup"><span data-stu-id="2d37e-156">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVpnSite
Parameter Sets: ByVpnGatewayNameByVpnSiteObject, ByVpnGatewayObjectByVpnSiteObject, ByVpnGatewayResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-157">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="2d37e-157">-VpnSiteId</span></span>
<span data-ttu-id="2d37e-158">Удаленный сайт VPN, к которому подключено данное виртуальное сетевое подключение к этому концентратору.</span><span class="sxs-lookup"><span data-stu-id="2d37e-158">The remote vpn site to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnGatewayNameByVpnSiteResourceId, ByVpnGatewayObjectByVpnSiteResourceId, ByVpnGatewayResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-159">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2d37e-159">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="2d37e-160">Список VpnSiteLinkConnections, которые есть в этой VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="2d37e-160">The list of VpnSiteLinkConnections that this VpnConnection have.</span></span>

```yaml
Type: PSVpnSiteLinkConnection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d37e-161">-Confirm</span></span>
<span data-ttu-id="2d37e-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d37e-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d37e-163">-WhatIf</span></span>
<span data-ttu-id="2d37e-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d37e-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d37e-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d37e-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d37e-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d37e-166">CommonParameters</span></span>
<span data-ttu-id="2d37e-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d37e-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d37e-168">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d37e-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d37e-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d37e-169">INPUTS</span></span>

### <span data-ttu-id="2d37e-170">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2d37e-170">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="2d37e-171">System. String</span><span class="sxs-lookup"><span data-stu-id="2d37e-171">System.String</span></span>

## <span data-ttu-id="2d37e-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d37e-172">OUTPUTS</span></span>

### <span data-ttu-id="2d37e-173">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d37e-173">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="2d37e-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d37e-174">NOTES</span></span>

## <span data-ttu-id="2d37e-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d37e-175">RELATED LINKS</span></span>

[<span data-ttu-id="2d37e-176">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d37e-176">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="2d37e-177">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d37e-177">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="2d37e-178">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="2d37e-178">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="2d37e-179">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d37e-179">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)