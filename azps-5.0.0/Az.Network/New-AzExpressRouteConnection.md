---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248538"
---
# <span data-ttu-id="dcbce-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="dcbce-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="dcbce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcbce-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbce-103">Создает подключение ExpressRoute, соединяющее шлюз ExpressRoute с локальной цепью ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcbce-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="dcbce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcbce-104">SYNTAX</span></span>

### <span data-ttu-id="dcbce-105">ByExpressRouteGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcbce-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcbce-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="dcbce-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcbce-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="dcbce-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcbce-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcbce-108">DESCRIPTION</span></span>
<span data-ttu-id="dcbce-109">Создает подключение ExpressRoute между одноранговым узлом BGP канала expressroute с помощью шлюза ExpressRoute внутри виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="dcbce-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="dcbce-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcbce-110">EXAMPLES</span></span>

### <span data-ttu-id="dcbce-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dcbce-111">Example 1</span></span>

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

<span data-ttu-id="dcbce-112">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор, а также канал ExpressRoute с частными соединениями в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="dcbce-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="dcbce-113">После создания шлюза он подключается к одноранговым каналам ExpressRoute с помощью команды New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="dcbce-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="dcbce-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcbce-114">PARAMETERS</span></span>

### <span data-ttu-id="dcbce-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dcbce-115">-AsJob</span></span>
<span data-ttu-id="dcbce-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dcbce-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dcbce-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="dcbce-117">-AuthorizationKey</span></span>
<span data-ttu-id="dcbce-118">Ключ, полученный от владельца канала ExpressRoute, для создания подключения с помощью шлюза в другой подписке.</span><span class="sxs-lookup"><span data-stu-id="dcbce-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

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

### <span data-ttu-id="dcbce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbce-119">-DefaultProfile</span></span>
<span data-ttu-id="dcbce-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcbce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcbce-121">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="dcbce-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="dcbce-122">Включите Интернет-безопасность для этого подключения к шлюзу ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="dcbce-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="dcbce-123">-ExpressRouteCircuitPeeringId</span><span class="sxs-lookup"><span data-stu-id="dcbce-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="dcbce-124">Идентификатор ресурса однорангового канала Express Route, на который будет создано это подключение к шлюзу Express Route.</span><span class="sxs-lookup"><span data-stu-id="dcbce-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

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

### <span data-ttu-id="dcbce-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="dcbce-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="dcbce-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcbce-126">The resource group name.</span></span>

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

### <span data-ttu-id="dcbce-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="dcbce-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="dcbce-128">Родительский ExpressRouteGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="dcbce-128">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="dcbce-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcbce-129">-Name</span></span>
<span data-ttu-id="dcbce-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="dcbce-130">The resource name.</span></span>

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

### <span data-ttu-id="dcbce-131">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dcbce-131">-ParentResourceId</span></span>
<span data-ttu-id="dcbce-132">Идентификатор ресурса родительского ExpressRouteGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="dcbce-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="dcbce-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcbce-133">-ResourceGroupName</span></span>
<span data-ttu-id="dcbce-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcbce-134">The resource group name.</span></span>

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

### <span data-ttu-id="dcbce-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcbce-135">-RoutingConfiguration</span></span>
<span data-ttu-id="dcbce-136">Настройка маршрутизации для этого подключения</span><span class="sxs-lookup"><span data-stu-id="dcbce-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="dcbce-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="dcbce-137">-RoutingWeight</span></span>
<span data-ttu-id="dcbce-138">Вес для маршрутизации пакетов, который должен быть назначен этому соединению.</span><span class="sxs-lookup"><span data-stu-id="dcbce-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

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

### <span data-ttu-id="dcbce-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcbce-139">-Confirm</span></span>
<span data-ttu-id="dcbce-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dcbce-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcbce-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcbce-141">-WhatIf</span></span>
<span data-ttu-id="dcbce-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dcbce-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcbce-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dcbce-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcbce-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbce-144">CommonParameters</span></span>
<span data-ttu-id="dcbce-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcbce-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbce-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcbce-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbce-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcbce-147">INPUTS</span></span>

### <span data-ttu-id="dcbce-148">Microsoft. Azure. Commands. Network. Models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="dcbce-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="dcbce-149">System. String</span><span class="sxs-lookup"><span data-stu-id="dcbce-149">System.String</span></span>

## <span data-ttu-id="dcbce-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcbce-150">OUTPUTS</span></span>

### <span data-ttu-id="dcbce-151">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="dcbce-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="dcbce-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcbce-152">NOTES</span></span>

## <span data-ttu-id="dcbce-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcbce-153">RELATED LINKS</span></span>

[<span data-ttu-id="dcbce-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="dcbce-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
