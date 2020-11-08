---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 37f3af46fd6a1c04eb4c793e67d32f9100aa5b60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244051"
---
# <span data-ttu-id="fa5d6-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fa5d6-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="fa5d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5d6-103">Обновляет VPN-подключение.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="fa5d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa5d6-104">SYNTAX</span></span>

### <span data-ttu-id="fa5d6-105">ByVpnConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa5d6-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa5d6-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="fa5d6-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa5d6-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="fa5d6-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa5d6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa5d6-108">DESCRIPTION</span></span>
<span data-ttu-id="fa5d6-109">Командлет **Update-AzVpnConnection** ОБНОВЛЯЕТ подключение VPN.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="fa5d6-110">VPN-подключение создает подключение IPsec, которое подключает VPN-шлюз к удаленной ветви клиента, представленной в Azure, в качестве VPN-сайта.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="fa5d6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa5d6-111">EXAMPLES</span></span>

### <span data-ttu-id="fa5d6-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa5d6-112">Example 1</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -IpSecPolicy $ipsecPolicy

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="fa5d6-113">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fa5d6-114">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fa5d6-115">После создания шлюза он подключается к VpnSite с помощью команды New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="fa5d6-116">После этого соединение обновится и появится новая IpSecPolicy с помощью команды Set-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="fa5d6-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fa5d6-117">Example 2</span></span>

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
PS C:\> $vpnConnection = New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> $Secure_String_Pwd = Read-Host -AsSecureString
PS C:\> Update-AzVpnConnection -InputObject $vpnConnection -SharedKey $Secure_String_Pwd

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy}
ConnectionBandwidth       : 20
EnableBgp                 : False
UseLocalAzureIpAddress    : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection
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

<span data-ttu-id="fa5d6-118">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и VpnSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="fa5d6-119">Шлюз VPN будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="fa5d6-120">После создания шлюза он подключается к VpnSite с помощью команды New-AzVpnConnection.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="fa5d6-121">После этого соединение обновится, чтобы создать общий ключ с помощью безопасной конструкции строки.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="fa5d6-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa5d6-122">PARAMETERS</span></span>

### <span data-ttu-id="fa5d6-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa5d6-123">-AsJob</span></span>
<span data-ttu-id="fa5d6-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fa5d6-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa5d6-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="fa5d6-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="fa5d6-126">Пропускная способность, которая должна быть обработана этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="fa5d6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5d6-127">-DefaultProfile</span></span>
<span data-ttu-id="fa5d6-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa5d6-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="fa5d6-129">-EnableBgp</span></span>
<span data-ttu-id="fa5d6-130">Включение BGP для этого подключения</span><span class="sxs-lookup"><span data-stu-id="fa5d6-130">Enable BGP for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d6-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="fa5d6-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="fa5d6-132">Включить Интернет-безопасность для этого подключения</span><span class="sxs-lookup"><span data-stu-id="fa5d6-132">Enable internet security for this connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d6-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa5d6-133">-InputObject</span></span>
<span data-ttu-id="fa5d6-134">Объект VpnConnection, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-134">The VpnConnection object to update.</span></span>

```yaml
Type: PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d6-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="fa5d6-135">-IpSecPolicy</span></span>
<span data-ttu-id="fa5d6-136">Пропускная способность, которая должна быть обработана этим соединением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="fa5d6-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fa5d6-137">-Name</span></span>
<span data-ttu-id="fa5d6-138">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d6-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="fa5d6-139">-ParentResourceName</span></span>
<span data-ttu-id="fa5d6-140">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-140">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa5d6-141">-ResourceGroupName</span></span>
<span data-ttu-id="fa5d6-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-142">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d6-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa5d6-143">-ResourceId</span></span>
<span data-ttu-id="fa5d6-144">Идентификатор ресурса объекта VpnConnection, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-144">The resource id of the VpnConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnConnectionResourceId
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d6-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="fa5d6-145">-RoutingConfiguration</span></span>
<span data-ttu-id="fa5d6-146">Настройка маршрутизации для этого подключения</span><span class="sxs-lookup"><span data-stu-id="fa5d6-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="fa5d6-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="fa5d6-147">-SharedKey</span></span>
<span data-ttu-id="fa5d6-148">Общий ключ, необходимый для настройки этого подключения.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="fa5d6-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="fa5d6-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="fa5d6-150">Использовать локальный IP-адрес Azure в качестве исходного адреса при инициализации подключения.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-150">Use local azure ip address as source address while initiating connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d6-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="fa5d6-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="fa5d6-152">Использование селекторов трафика на основе политики для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-152">Use policy based traffic selectors for this connection.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5d6-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="fa5d6-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="fa5d6-154">Список VpnSiteLinkConnections, который должен иметь этот VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="fa5d6-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa5d6-155">-Confirm</span></span>
<span data-ttu-id="fa5d6-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa5d6-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa5d6-157">-WhatIf</span></span>
<span data-ttu-id="fa5d6-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa5d6-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa5d6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5d6-160">CommonParameters</span></span>
<span data-ttu-id="fa5d6-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa5d6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5d6-162">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa5d6-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5d6-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa5d6-163">INPUTS</span></span>

### <span data-ttu-id="fa5d6-164">System. String</span><span class="sxs-lookup"><span data-stu-id="fa5d6-164">System.String</span></span>

### <span data-ttu-id="fa5d6-165">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fa5d6-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="fa5d6-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa5d6-166">OUTPUTS</span></span>

### <span data-ttu-id="fa5d6-167">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fa5d6-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="fa5d6-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa5d6-168">NOTES</span></span>

## <span data-ttu-id="fa5d6-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa5d6-169">RELATED LINKS</span></span>

[<span data-ttu-id="fa5d6-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fa5d6-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="fa5d6-171">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fa5d6-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="fa5d6-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fa5d6-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="fa5d6-173">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="fa5d6-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
