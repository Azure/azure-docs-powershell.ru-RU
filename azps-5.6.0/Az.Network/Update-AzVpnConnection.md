---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnConnection.md
ms.openlocfilehash: 3de80ca92f86ab969b9d44ffc9f63871486d969a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951464"
---
# <span data-ttu-id="154c3-101">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="154c3-101">Update-AzVpnConnection</span></span>

## <span data-ttu-id="154c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="154c3-102">SYNOPSIS</span></span>
<span data-ttu-id="154c3-103">Обновляет VPN-подключение.</span><span class="sxs-lookup"><span data-stu-id="154c3-103">Updates a VPN connection.</span></span>

## <span data-ttu-id="154c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="154c3-104">SYNTAX</span></span>

### <span data-ttu-id="154c3-105">ByVpnConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="154c3-105">ByVpnConnectionName (Default)</span></span>
```
Update-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>]
 [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="154c3-106">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="154c3-106">ByVpnConnectionResourceId</span></span>
```
Update-AzVpnConnection -ResourceId <String> [-SharedKey <SecureString>] [-ConnectionBandwidthInMbps <UInt32>]
 [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>]
 [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="154c3-107">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="154c3-107">ByVpnConnectionObject</span></span>
```
Update-AzVpnConnection -InputObject <PSVpnConnection> [-SharedKey <SecureString>]
 [-ConnectionBandwidthInMbps <UInt32>] [-IpSecPolicy <PSIpsecPolicy>] [-EnableBgp <Boolean>]
 [-UseLocalAzureIpAddress <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-VpnSiteLinkConnection <PSVpnSiteLinkConnection[]>] [-EnableInternetSecurity <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="154c3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="154c3-108">DESCRIPTION</span></span>
<span data-ttu-id="154c3-109">С **помощью cmdlet Update-AzVpnConnection** обновляется VPN-подключение.</span><span class="sxs-lookup"><span data-stu-id="154c3-109">The **Update-AzVpnConnection** cmdlet updates a VPN connection.</span></span>  
<span data-ttu-id="154c3-110">VPN-подключение создает подключение IPsec, которое подключает VPN-шлюз к удаленной ветви клиента, представленной в Azure как VPN-сайт.</span><span class="sxs-lookup"><span data-stu-id="154c3-110">VPN connection creates an IPsec connection that connects a VPN gateway to a remote customer branch represented in Azure as a VPN site.</span></span>

## <span data-ttu-id="154c3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="154c3-111">EXAMPLES</span></span>

### <span data-ttu-id="154c3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="154c3-112">Example 1</span></span>

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

<span data-ttu-id="154c3-113">Выше будет создание группы ресурсов, виртуальной WAN, виртуальной сети, виртуального концентратора и VPNSite в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="154c3-113">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="154c3-114">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="154c3-114">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="154c3-115">Созданный шлюз подключается к VPNSite с помощью команды New-AzVpnConnection входа.</span><span class="sxs-lookup"><span data-stu-id="154c3-115">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="154c3-116">Соединение будет обновлено с использованием команды Set-AzVpnConnection IpSecPolicy.</span><span class="sxs-lookup"><span data-stu-id="154c3-116">The connection is then updated to have a new IpSecPolicy by using the Set-AzVpnConnection command.</span></span>

### <span data-ttu-id="154c3-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="154c3-117">Example 2</span></span>

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

<span data-ttu-id="154c3-118">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор и VPNSite в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="154c3-118">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="154c3-119">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="154c3-119">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="154c3-120">Созданный шлюз подключается к VPNSite с помощью команды New-AzVpnConnection входа.</span><span class="sxs-lookup"><span data-stu-id="154c3-120">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="154c3-121">Соединение будет обновлено, чтобы получить новый общий ключ с помощью конструкции безопасной строки.</span><span class="sxs-lookup"><span data-stu-id="154c3-121">The connection is then updated to have a new shared key using the secure string construct.</span></span>

## <span data-ttu-id="154c3-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="154c3-122">PARAMETERS</span></span>

### <span data-ttu-id="154c3-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="154c3-123">-AsJob</span></span>
<span data-ttu-id="154c3-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="154c3-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="154c3-125">-ConnectionBandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="154c3-125">-ConnectionBandwidthInMbps</span></span>
<span data-ttu-id="154c3-126">Пропускная способность, которая должна обрабатываться этим подключением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="154c3-126">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="154c3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154c3-127">-DefaultProfile</span></span>
<span data-ttu-id="154c3-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="154c3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="154c3-129">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="154c3-129">-EnableBgp</span></span>
<span data-ttu-id="154c3-130">Включить BGP для этого подключения</span><span class="sxs-lookup"><span data-stu-id="154c3-130">Enable BGP for this connection</span></span>

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

### <span data-ttu-id="154c3-131">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="154c3-131">-EnableInternetSecurity</span></span>
<span data-ttu-id="154c3-132">Включить безопасность Интернета для этого подключения</span><span class="sxs-lookup"><span data-stu-id="154c3-132">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="154c3-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="154c3-133">-InputObject</span></span>
<span data-ttu-id="154c3-134">Объект VpnConnection, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="154c3-134">The VpnConnection object to update.</span></span>

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

### <span data-ttu-id="154c3-135">-IpSecPolicy</span><span class="sxs-lookup"><span data-stu-id="154c3-135">-IpSecPolicy</span></span>
<span data-ttu-id="154c3-136">Пропускная способность, которая должна обрабатываться этим подключением в Мбит/с.</span><span class="sxs-lookup"><span data-stu-id="154c3-136">The bandwidth that needs to be handled by this connection in mbps.</span></span>

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

### <span data-ttu-id="154c3-137">-Name</span><span class="sxs-lookup"><span data-stu-id="154c3-137">-Name</span></span>
<span data-ttu-id="154c3-138">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="154c3-138">The resource name.</span></span>

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

### <span data-ttu-id="154c3-139">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="154c3-139">-ParentResourceName</span></span>
<span data-ttu-id="154c3-140">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="154c3-140">The parent resource name.</span></span>

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

### <span data-ttu-id="154c3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="154c3-141">-ResourceGroupName</span></span>
<span data-ttu-id="154c3-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="154c3-142">The resource group name.</span></span>

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

### <span data-ttu-id="154c3-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="154c3-143">-ResourceId</span></span>
<span data-ttu-id="154c3-144">ИД ресурса объекта VpnConnection, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="154c3-144">The resource id of the VpnConnection object to delete.</span></span>

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

### <span data-ttu-id="154c3-145">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="154c3-145">-RoutingConfiguration</span></span>
<span data-ttu-id="154c3-146">Настройка маршрутиации для этого подключения</span><span class="sxs-lookup"><span data-stu-id="154c3-146">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="154c3-147">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="154c3-147">-SharedKey</span></span>
<span data-ttu-id="154c3-148">Общий ключ, необходимый для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="154c3-148">The shared key required to set this connection up.</span></span>

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

### <span data-ttu-id="154c3-149">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="154c3-149">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="154c3-150">Используйте локальный IP-адрес Azure в качестве источника при иниции подключения.</span><span class="sxs-lookup"><span data-stu-id="154c3-150">Use local azure ip address as source address while initiating connection.</span></span>

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

### <span data-ttu-id="154c3-151">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="154c3-151">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="154c3-152">Для этого подключения используйте селекторы трафика на основе политики.</span><span class="sxs-lookup"><span data-stu-id="154c3-152">Use policy based traffic selectors for this connection.</span></span>

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

### <span data-ttu-id="154c3-153">-VpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="154c3-153">-VpnSiteLinkConnection</span></span>
<span data-ttu-id="154c3-154">Список vpnSiteLinkConnections, необходимых для этого VPNConnection.</span><span class="sxs-lookup"><span data-stu-id="154c3-154">The list of VpnSiteLinkConnections that this VpnConnection needs to have.</span></span>

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

### <span data-ttu-id="154c3-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="154c3-155">-Confirm</span></span>
<span data-ttu-id="154c3-156">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="154c3-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="154c3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="154c3-157">-WhatIf</span></span>
<span data-ttu-id="154c3-158">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="154c3-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="154c3-159">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="154c3-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="154c3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154c3-160">CommonParameters</span></span>
<span data-ttu-id="154c3-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="154c3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154c3-162">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="154c3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154c3-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="154c3-163">INPUTS</span></span>

### <span data-ttu-id="154c3-164">System.String</span><span class="sxs-lookup"><span data-stu-id="154c3-164">System.String</span></span>

### <span data-ttu-id="154c3-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="154c3-165">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="154c3-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="154c3-166">OUTPUTS</span></span>

### <span data-ttu-id="154c3-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="154c3-167">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="154c3-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="154c3-168">NOTES</span></span>

## <span data-ttu-id="154c3-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="154c3-169">RELATED LINKS</span></span>

[<span data-ttu-id="154c3-170">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="154c3-170">Get-AzVpnConnection</span></span>](./Get-AzVpnConnection.md)

[<span data-ttu-id="154c3-171">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="154c3-171">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="154c3-172">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="154c3-172">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="154c3-173">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="154c3-173">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
