---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 01b8c32af3edc6c10070bdbd61c7f84fa055af23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730589"
---
# <span data-ttu-id="e5cbc-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e5cbc-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="e5cbc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="e5cbc-103">Получает подключение ExpressRoute по имени или список всех подключений ExpressRoute, подключенных к ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="e5cbc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5cbc-104">SYNTAX</span></span>

### <span data-ttu-id="e5cbc-105">ByExpressRouteGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5cbc-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5cbc-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e5cbc-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5cbc-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e5cbc-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5cbc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5cbc-108">DESCRIPTION</span></span>
<span data-ttu-id="e5cbc-109">Получает подключение ExpressRoute по имени или список всех подключений ExpressRoute, подключенных к ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="e5cbc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5cbc-110">EXAMPLES</span></span>

### <span data-ttu-id="e5cbc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5cbc-111">Example 1</span></span>

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
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="e5cbc-112">В описанном выше примере вы создадите группу ресурсов, виртуальную ГЛОБАЛЬную сеть, виртуальную сетевую службу, виртуальный концентратор и ExpressRouteSite в области "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e5cbc-113">Шлюз ExpressRoute будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e5cbc-114">После создания шлюза он подключается к локальной цепи ExpressRoute с помощью команды New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="e5cbc-115">Затем он получает подключение, используя имя подключения.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="e5cbc-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5cbc-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
```

<span data-ttu-id="e5cbc-117">Эта команда будет получать все подключения в ExpressRoute "testExpressRoutegw", которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="e5cbc-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="e5cbc-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5cbc-118">PARAMETERS</span></span>

### <span data-ttu-id="e5cbc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5cbc-119">-DefaultProfile</span></span>
<span data-ttu-id="e5cbc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5cbc-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="e5cbc-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="e5cbc-122">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-122">The parent resource name.</span></span>

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

### <span data-ttu-id="e5cbc-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e5cbc-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="e5cbc-124">Родительский ExpressRouteGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-124">The parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="e5cbc-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5cbc-125">-Name</span></span>
<span data-ttu-id="e5cbc-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-126">The resource name.</span></span>

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

### <span data-ttu-id="e5cbc-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e5cbc-127">-ParentResourceId</span></span>
<span data-ttu-id="e5cbc-128">Идентификатор ресурса родительского ExpressRouteGateway для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

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

### <span data-ttu-id="e5cbc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5cbc-129">-ResourceGroupName</span></span>
<span data-ttu-id="e5cbc-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-130">The resource group name.</span></span>

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

### <span data-ttu-id="e5cbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5cbc-131">CommonParameters</span></span>
<span data-ttu-id="e5cbc-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5cbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5cbc-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5cbc-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5cbc-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5cbc-134">INPUTS</span></span>

### <span data-ttu-id="e5cbc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e5cbc-135">System.String</span></span>

## <span data-ttu-id="e5cbc-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5cbc-136">OUTPUTS</span></span>

### <span data-ttu-id="e5cbc-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e5cbc-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="e5cbc-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5cbc-138">NOTES</span></span>

## <span data-ttu-id="e5cbc-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5cbc-139">RELATED LINKS</span></span>
