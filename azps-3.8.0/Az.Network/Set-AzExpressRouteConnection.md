---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: 1e2156b955f4b7a98f6c8886ea538f77cee7fe34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065809"
---
# <span data-ttu-id="3d756-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="3d756-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="3d756-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d756-102">SYNOPSIS</span></span>
<span data-ttu-id="3d756-103">Обновляет подключение по протоколу Express Route, созданное между интерфейсом Express Route Gateway и одноранговым каналом канала Экспресс-маршрута.</span><span class="sxs-lookup"><span data-stu-id="3d756-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="3d756-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d756-104">SYNTAX</span></span>

### <span data-ttu-id="3d756-105">ByExpressRouteConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d756-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d756-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="3d756-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d756-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="3d756-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d756-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d756-108">DESCRIPTION</span></span>
<span data-ttu-id="3d756-109">Командлет **Set-AzExpressRouteConnection** обновляет подключение по протоколу Express Route, созданное между интерфейсом Express Route Gateway и одноранговым каналом связи Экспресс-маршрута.</span><span class="sxs-lookup"><span data-stu-id="3d756-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="3d756-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d756-110">EXAMPLES</span></span>

### <span data-ttu-id="3d756-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d756-111">Example 1</span></span>

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
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="3d756-112">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и ExpressRouteSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="3d756-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="3d756-113">Шлюз ExpressRoute будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="3d756-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="3d756-114">После создания шлюза он подключается к одноранговой стороне канала ExpressRoute с помощью команды New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="3d756-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="3d756-115">После этого соединение обновится, чтобы оно RoutingWeight с помощью команды "Set-AzExpressRouteConnection".</span><span class="sxs-lookup"><span data-stu-id="3d756-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="3d756-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d756-116">PARAMETERS</span></span>

### <span data-ttu-id="3d756-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d756-117">-AsJob</span></span>
<span data-ttu-id="3d756-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3d756-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d756-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="3d756-119">-AuthorizationKey</span></span>
<span data-ttu-id="3d756-120">Ключ проверки подлинности, который будет использоваться для создания подключения к шлюзу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="3d756-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="3d756-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d756-121">-DefaultProfile</span></span>
<span data-ttu-id="3d756-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d756-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d756-123">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="3d756-123">-EnableInternetSecurity</span></span>
<span data-ttu-id="3d756-124">Включите Интернет-безопасность для этого подключения к шлюзу ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="3d756-124">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="3d756-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="3d756-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="3d756-126">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="3d756-126">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d756-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d756-127">-InputObject</span></span>
<span data-ttu-id="3d756-128">Объект ExpressRouteConnection, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="3d756-128">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d756-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d756-129">-Name</span></span>
<span data-ttu-id="3d756-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3d756-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d756-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d756-131">-ResourceGroupName</span></span>
<span data-ttu-id="3d756-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d756-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d756-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d756-133">-ResourceId</span></span>
<span data-ttu-id="3d756-134">Идентификатор ресурса объекта ExpressRouteConnection, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3d756-134">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d756-135">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="3d756-135">-RoutingWeight</span></span>
<span data-ttu-id="3d756-136">Вес, который должен быть назначен этому соединению для маршрутизации пакетов.</span><span class="sxs-lookup"><span data-stu-id="3d756-136">The weight that needs to be assigned to this connection for packet routing.</span></span>

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

### <span data-ttu-id="3d756-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d756-137">-Confirm</span></span>
<span data-ttu-id="3d756-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d756-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d756-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d756-139">-WhatIf</span></span>
<span data-ttu-id="3d756-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d756-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d756-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d756-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d756-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d756-142">CommonParameters</span></span>
<span data-ttu-id="3d756-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d756-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d756-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d756-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d756-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d756-145">INPUTS</span></span>

### <span data-ttu-id="3d756-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3d756-146">System.String</span></span>

### <span data-ttu-id="3d756-147">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="3d756-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="3d756-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d756-148">OUTPUTS</span></span>

### <span data-ttu-id="3d756-149">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="3d756-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="3d756-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d756-150">NOTES</span></span>

## <span data-ttu-id="3d756-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d756-151">RELATED LINKS</span></span>
