---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 3089d3654e471bbf31eb81e42e4374525d84010d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974776"
---
# <span data-ttu-id="9f1f6-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="9f1f6-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="9f1f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f1f6-103">Создает подключение ExpressRoute, которое подключает шлюз ExpressRoute к локальному каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="9f1f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f1f6-104">SYNTAX</span></span>

### <span data-ttu-id="9f1f6-105">ByExpressRouteGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f1f6-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f1f6-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9f1f6-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f1f6-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9f1f6-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f1f6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f1f6-108">DESCRIPTION</span></span>
<span data-ttu-id="9f1f6-109">Создает подключение ExpressRoute между локальной схемой BGP expressRoute и шлюзом ExpressRoute внутри виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="9f1f6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f1f6-110">EXAMPLES</span></span>

### <span data-ttu-id="9f1f6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f1f6-111">Example 1</span></span>

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
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
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

<span data-ttu-id="9f1f6-112">Выше мы создадим группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор, шлюз ExpressRoute и канал ExpressRoute с частным пирингом в Западной центральной части США в группе ресурсов TestRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="9f1f6-113">Созданный шлюз подключается к пирингу каналов ExpressRoute с помощью команды New-AzExpressRouteConnection подключения.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="9f1f6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f1f6-114">PARAMETERS</span></span>

### <span data-ttu-id="9f1f6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f1f6-115">-AsJob</span></span>
<span data-ttu-id="9f1f6-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9f1f6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f1f6-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="9f1f6-117">-AuthorizationKey</span></span>
<span data-ttu-id="9f1f6-118">Ключ, полученный от владельца схемы ExpressRoute для создания подключения к шлюзу в другой подписке.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f1f6-119">-DefaultProfile</span></span>
<span data-ttu-id="9f1f6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f1f6-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="9f1f6-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="9f1f6-122">Включить безопасность Интернета для этого подключения шлюза ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="9f1f6-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="9f1f6-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="9f1f6-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="9f1f6-124">ИД ресурса пиринга express Route, к которому должно быть создано подключение шлюза Express Route.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1f6-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="9f1f6-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="9f1f6-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1f6-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9f1f6-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="9f1f6-128">Родительская компания ExpressRouteGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-128">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1f6-129">-Name</span><span class="sxs-lookup"><span data-stu-id="9f1f6-129">-Name</span></span>
<span data-ttu-id="9f1f6-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1f6-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9f1f6-131">-ParentResourceId</span></span>
<span data-ttu-id="9f1f6-132">ИД ресурса родительского ресурса ExpressRouteGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f1f6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f1f6-133">-ResourceGroupName</span></span>
<span data-ttu-id="9f1f6-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-134">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f1f6-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f1f6-135">-RoutingConfiguration</span></span>
<span data-ttu-id="9f1f6-136">Настройка маршрутиации для этого подключения</span><span class="sxs-lookup"><span data-stu-id="9f1f6-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="9f1f6-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="9f1f6-137">-RoutingWeight</span></span>
<span data-ttu-id="9f1f6-138">Вес для маршрутики пакетов, которая должна быть назначена этому подключению.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

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

### <span data-ttu-id="9f1f6-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f1f6-139">-Confirm</span></span>
<span data-ttu-id="9f1f6-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f1f6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f1f6-141">-WhatIf</span></span>
<span data-ttu-id="9f1f6-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f1f6-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f1f6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f1f6-144">CommonParameters</span></span>
<span data-ttu-id="9f1f6-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f1f6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f1f6-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f1f6-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f1f6-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f1f6-147">INPUTS</span></span>

### <span data-ttu-id="9f1f6-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="9f1f6-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="9f1f6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9f1f6-149">System.String</span></span>

## <span data-ttu-id="9f1f6-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f1f6-150">OUTPUTS</span></span>

### <span data-ttu-id="9f1f6-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="9f1f6-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="9f1f6-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f1f6-152">NOTES</span></span>

## <span data-ttu-id="9f1f6-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f1f6-153">RELATED LINKS</span></span>

[<span data-ttu-id="9f1f6-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f1f6-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
