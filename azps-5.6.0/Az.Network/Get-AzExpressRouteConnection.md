---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 4665e67b64baa87273c365137cc2247e86efd2c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991024"
---
# <span data-ttu-id="75e2e-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="75e2e-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="75e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="75e2e-103">Подключение ExpressRoute по имени или список всех подключений ExpressRoute, подключенных к ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="75e2e-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="75e2e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75e2e-104">SYNTAX</span></span>

### <span data-ttu-id="75e2e-105">ByExpressRouteGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75e2e-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75e2e-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="75e2e-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75e2e-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="75e2e-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75e2e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75e2e-108">DESCRIPTION</span></span>
<span data-ttu-id="75e2e-109">Подключение ExpressRoute по имени или список всех подключений ExpressRoute, подключенных к ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="75e2e-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="75e2e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75e2e-110">EXAMPLES</span></span>

### <span data-ttu-id="75e2e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75e2e-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
EnableInternetSecurity             : False
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="75e2e-112">Выше будет создание группы ресурсов, виртуальной WAN, виртуальной сети, виртуального концентратора и expressRouteSite в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="75e2e-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="75e2e-113">После этого в виртуальном центре будет создан шлюз ExpressRoute с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="75e2e-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="75e2e-114">Созданный шлюз подключается к локальному каналу ExpressRoute с помощью команды New-AzExpressRouteConnection управления.</span><span class="sxs-lookup"><span data-stu-id="75e2e-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="75e2e-115">Затем подключение получается с использованием имени подключения.</span><span class="sxs-lookup"><span data-stu-id="75e2e-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="75e2e-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75e2e-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1
EnableInternetSecurity             : False
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
EnableInternetSecurity             : False
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="75e2e-117">Эта команда получит все подключения в ExpressRoute "testExpressRoutegw", которые начинаются с "test"</span><span class="sxs-lookup"><span data-stu-id="75e2e-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="75e2e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75e2e-118">PARAMETERS</span></span>

### <span data-ttu-id="75e2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e2e-119">-DefaultProfile</span></span>
<span data-ttu-id="75e2e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75e2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75e2e-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="75e2e-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="75e2e-122">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="75e2e-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75e2e-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="75e2e-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="75e2e-124">Родительская компания ExpressRouteGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="75e2e-124">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75e2e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="75e2e-125">-Name</span></span>
<span data-ttu-id="75e2e-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="75e2e-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="75e2e-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="75e2e-127">-ParentResourceId</span></span>
<span data-ttu-id="75e2e-128">ИД ресурса родительского ресурса ExpressRouteGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="75e2e-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75e2e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75e2e-129">-ResourceGroupName</span></span>
<span data-ttu-id="75e2e-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75e2e-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75e2e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e2e-131">CommonParameters</span></span>
<span data-ttu-id="75e2e-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e2e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e2e-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75e2e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e2e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75e2e-134">INPUTS</span></span>

### <span data-ttu-id="75e2e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="75e2e-135">System.String</span></span>

## <span data-ttu-id="75e2e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75e2e-136">OUTPUTS</span></span>

### <span data-ttu-id="75e2e-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="75e2e-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="75e2e-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75e2e-138">NOTES</span></span>

## <span data-ttu-id="75e2e-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75e2e-139">RELATED LINKS</span></span>
