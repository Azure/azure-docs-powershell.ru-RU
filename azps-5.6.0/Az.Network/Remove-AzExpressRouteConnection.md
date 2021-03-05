---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 3e9bd0022215f353388e19edb4f5cc6944acbb2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993793"
---
# <span data-ttu-id="edcdb-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="edcdb-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="edcdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edcdb-102">SYNOPSIS</span></span>
<span data-ttu-id="edcdb-103">Удаляет ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="edcdb-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="edcdb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="edcdb-104">SYNTAX</span></span>

### <span data-ttu-id="edcdb-105">ByExpressRouteConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="edcdb-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edcdb-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="edcdb-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edcdb-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="edcdb-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edcdb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edcdb-108">DESCRIPTION</span></span>
<span data-ttu-id="edcdb-109">Удаляет ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="edcdb-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="edcdb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="edcdb-110">EXAMPLES</span></span>

### <span data-ttu-id="edcdb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="edcdb-111">Example 1</span></span>
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
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="edcdb-112">Выше будет создать группу ресурсов, виртуальную сеть, виртуальную сеть, виртуальный концентратор на западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="edcdb-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="edcdb-113">После этого в виртуальном центре будет создан шлюз ExpressRoute с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="edcdb-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="edcdb-114">Созданный шлюз подключается к expressRouteSite с помощью команды New-AzExpressRouteConnection входа.</span><span class="sxs-lookup"><span data-stu-id="edcdb-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="edcdb-115">Затем соединение удаляется с использованием имени подключения.</span><span class="sxs-lookup"><span data-stu-id="edcdb-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="edcdb-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="edcdb-116">Example 2</span></span>

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
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="edcdb-117">То же, что и в примере 1, но теперь соединение, используемого в качестве канала Get-AzExpressRouteConnection, удаляется с помощью канала "Get-AzExpressRouteConnection".</span><span class="sxs-lookup"><span data-stu-id="edcdb-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="edcdb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edcdb-118">PARAMETERS</span></span>

### <span data-ttu-id="edcdb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edcdb-119">-DefaultProfile</span></span>
<span data-ttu-id="edcdb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edcdb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edcdb-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="edcdb-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="edcdb-122">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="edcdb-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdb-123">-Force</span><span class="sxs-lookup"><span data-stu-id="edcdb-123">-Force</span></span>
<span data-ttu-id="edcdb-124">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="edcdb-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edcdb-125">-InputObject</span></span>
<span data-ttu-id="edcdb-126">Объект ExpressRouteConnection, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="edcdb-126">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edcdb-127">-Name</span><span class="sxs-lookup"><span data-stu-id="edcdb-127">-Name</span></span>
<span data-ttu-id="edcdb-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="edcdb-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edcdb-129">-PassThru</span></span>
<span data-ttu-id="edcdb-130">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="edcdb-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="edcdb-131">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="edcdb-131">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edcdb-132">-ResourceGroupName</span></span>
<span data-ttu-id="edcdb-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="edcdb-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edcdb-134">-ResourceId</span></span>
<span data-ttu-id="edcdb-135">ИД ресурса объекта ExpressRouteConnection, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="edcdb-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edcdb-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edcdb-136">-Confirm</span></span>
<span data-ttu-id="edcdb-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edcdb-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edcdb-138">-WhatIf</span></span>
<span data-ttu-id="edcdb-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edcdb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edcdb-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="edcdb-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcdb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edcdb-141">CommonParameters</span></span>
<span data-ttu-id="edcdb-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edcdb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edcdb-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edcdb-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edcdb-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edcdb-144">INPUTS</span></span>

### <span data-ttu-id="edcdb-145">System.String</span><span class="sxs-lookup"><span data-stu-id="edcdb-145">System.String</span></span>

### <span data-ttu-id="edcdb-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="edcdb-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="edcdb-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="edcdb-147">OUTPUTS</span></span>

### <span data-ttu-id="edcdb-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="edcdb-148">System.Boolean</span></span>

## <span data-ttu-id="edcdb-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="edcdb-149">NOTES</span></span>

## <span data-ttu-id="edcdb-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edcdb-150">RELATED LINKS</span></span>
