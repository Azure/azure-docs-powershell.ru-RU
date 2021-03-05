---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnConnection.md
ms.openlocfilehash: 51a4d6e2325685b81c01ce58c667412e209a8074
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964216"
---
# <span data-ttu-id="75f9a-101">Get-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="75f9a-101">Get-AzVpnConnection</span></span>

## <span data-ttu-id="75f9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="75f9a-103">Vpn-подключение по имени или список всех VPN-подключений, подключенных к VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="75f9a-103">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="75f9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75f9a-104">SYNTAX</span></span>

### <span data-ttu-id="75f9a-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75f9a-105">ByVpnGatewayName (Default)</span></span>
```
Get-AzVpnConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75f9a-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="75f9a-106">ByVpnGatewayObject</span></span>
```
Get-AzVpnConnection -ParentObject <PSVpnGateway> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75f9a-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="75f9a-107">ByVpnGatewayResourceId</span></span>
```
Get-AzVpnConnection -ParentResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75f9a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75f9a-108">DESCRIPTION</span></span>
<span data-ttu-id="75f9a-109">Vpn-подключение по имени или список всех VPN-подключений, подключенных к VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="75f9a-109">Gets a vpn connection by name or lists all vpn connections connected to a VpnGateway.</span></span>

## <span data-ttu-id="75f9a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75f9a-110">EXAMPLES</span></span>

### <span data-ttu-id="75f9a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75f9a-111">Example 1</span></span>

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

PS C:\> New-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite
PS C:\> Get-AzVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection"

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
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

<span data-ttu-id="75f9a-112">Выше будет создание группы ресурсов, виртуальной WAN, виртуальной сети, виртуального концентратора и VPNSite в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="75f9a-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="75f9a-113">После этого в виртуальном центре будет создан VPN-шлюз с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="75f9a-113">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="75f9a-114">Созданный шлюз подключается к VPNSite с помощью команды New-AzVpnConnection входа.</span><span class="sxs-lookup"><span data-stu-id="75f9a-114">Once the gateway has been created, it is connected to the VpnSite using the New-AzVpnConnection command.</span></span>

<span data-ttu-id="75f9a-115">Затем подключение получается с использованием имени подключения.</span><span class="sxs-lookup"><span data-stu-id="75f9a-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="75f9a-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75f9a-116">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnConnection -ResourceGroupName ps9361 -ParentResourceName testvpngw -Name test*

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection1
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

RemoteVpnSite             : Microsoft.Azure.Commands.Network.Models.PSResourceId
SharedKey                 :
VpnConnectionProtocolType : IKEv2
ConnectionStatus          :
EgressBytesTransferred    : 0
IngressBytesTransferred   : 0
IpsecPolicies             : {}
ConnectionBandwidth       : 20
EnableBgp                 : False
ProvisioningState         : testConnection
Name                      : ps9709
Etag                      : W/"xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Id                        : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/vpnGateways/testvpngw/vpnConnections/testConnection2
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

<span data-ttu-id="75f9a-117">Этот cmdlet получает все подключения, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="75f9a-117">This cmdlet gets all connections that start with "test".</span></span>

## <span data-ttu-id="75f9a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75f9a-118">PARAMETERS</span></span>

### <span data-ttu-id="75f9a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f9a-119">-DefaultProfile</span></span>
<span data-ttu-id="75f9a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75f9a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75f9a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="75f9a-121">-Name</span></span>
<span data-ttu-id="75f9a-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="75f9a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f9a-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="75f9a-123">-ParentObject</span></span>
<span data-ttu-id="75f9a-124">Родительская vpnGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="75f9a-124">The parent VpnGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: ParentVpnGateway, VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75f9a-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="75f9a-125">-ParentResourceId</span></span>
<span data-ttu-id="75f9a-126">ИД ресурса родительского VPNGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="75f9a-126">The resource id of the parent VpnGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ParentVpnGatewayId, VpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75f9a-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="75f9a-127">-ParentResourceName</span></span>
<span data-ttu-id="75f9a-128">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="75f9a-128">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f9a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f9a-129">-ResourceGroupName</span></span>
<span data-ttu-id="75f9a-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75f9a-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f9a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f9a-131">CommonParameters</span></span>
<span data-ttu-id="75f9a-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f9a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f9a-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75f9a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f9a-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75f9a-134">INPUTS</span></span>

### <span data-ttu-id="75f9a-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="75f9a-135">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="75f9a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="75f9a-136">System.String</span></span>

## <span data-ttu-id="75f9a-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75f9a-137">OUTPUTS</span></span>

### <span data-ttu-id="75f9a-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="75f9a-138">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

## <span data-ttu-id="75f9a-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75f9a-139">NOTES</span></span>

## <span data-ttu-id="75f9a-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75f9a-140">RELATED LINKS</span></span>

[<span data-ttu-id="75f9a-141">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="75f9a-141">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="75f9a-142">Remove-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="75f9a-142">Remove-AzVpnConnection</span></span>](./Remove-AzVpnConnection.md)

[<span data-ttu-id="75f9a-143">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="75f9a-143">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)
