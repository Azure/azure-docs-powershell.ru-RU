---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c3d01639d428820578ffe8a319bddd591c007e00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410591"
---
# <span data-ttu-id="b7602-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7602-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b7602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7602-102">SYNOPSIS</span></span>
<span data-ttu-id="b7602-103">Добавляет конфигурацию подсети в виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b7602-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="b7602-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7602-104">SYNTAX</span></span>

### <span data-ttu-id="b7602-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7602-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7602-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7602-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7602-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7602-107">DESCRIPTION</span></span>
<span data-ttu-id="b7602-108">Командлет **Add-AzVirtualNetworkSubnetConfig** добавляет конфигурацию подсети в существующую виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="b7602-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="b7602-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7602-109">EXAMPLES</span></span>

### <span data-ttu-id="b7602-110">Пример 1. Добавление подсети в существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="b7602-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="b7602-111">В этом примере сначала создается группа ресурсов в качестве контейнера для создания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7602-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="b7602-112">Затем она создает конфигурацию подсети и использует ее для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b7602-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="b7602-113">Затем Add-AzVirtualNetworkSubnetConfig используется для добавления подсети в представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="b7602-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="b7602-114">Команда Set-AzVirtualNetwork обновляет существующую виртуальную сеть с помощью новой подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="b7602-115">Пример 2. Добавление делегирования в подсеть, добавляемую в существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="b7602-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="b7602-116">В этом примере сначала возвращается существующая vnet.</span><span class="sxs-lookup"><span data-stu-id="b7602-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="b7602-117">Затем в памяти создается объект делегирования.</span><span class="sxs-lookup"><span data-stu-id="b7602-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="b7602-118">Наконец, она создает новую подсеть с этим делегирования, добавленным в vnet.</span><span class="sxs-lookup"><span data-stu-id="b7602-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="b7602-119">Измененная конфигурация отправляется на сервер.</span><span class="sxs-lookup"><span data-stu-id="b7602-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="b7602-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7602-120">PARAMETERS</span></span>

### <span data-ttu-id="b7602-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b7602-121">-AddressPrefix</span></span>
<span data-ttu-id="b7602-122">Диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7602-123">-DefaultProfile</span></span>
<span data-ttu-id="b7602-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7602-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7602-125">-Delegation</span><span class="sxs-lookup"><span data-stu-id="b7602-125">-Delegation</span></span>
<span data-ttu-id="b7602-126">Список служб с разрешением на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7602-127">-InputObject</span></span>
<span data-ttu-id="b7602-128">Указывает шлюз NAT, связанный с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="b7602-129">-IpAllocation</span></span>
<span data-ttu-id="b7602-130">IpAllocations для подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-130">Specifies IpAllocations for a subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b7602-131">-Name</span></span>
<span data-ttu-id="b7602-132">Имя добавляемой конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-132">Specifies the name of the subnet configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7602-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b7602-134">Объект **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="b7602-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="b7602-135">Этот cmdlet добавляет конфигурацию виртуальной подсети сети к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="b7602-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b7602-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="b7602-137">Определяет ИД группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="b7602-137">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="b7602-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="b7602-139">Настройте или отключаете применение сетевых политик на закрытой конечной точке в подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="b7602-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="b7602-141">Настройте возможность или отключение применения сетевых политик в службе частных ссылок в подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7602-142">-ResourceId</span></span>
<span data-ttu-id="b7602-143">Определяет ИД ресурса шлюза NAT, связанного с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b7602-144">-RouteTable</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="b7602-145">-RouteTableId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b7602-146">-ServiceEndpoint</span></span>
<span data-ttu-id="b7602-147">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="b7602-147">Service Endpoint Value</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="b7602-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="b7602-149">Политики конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="b7602-149">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b7602-150">-VirtualNetwork</span></span>
<span data-ttu-id="b7602-151">Определяет объект **VirtualNetwork,** в который нужно добавить конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="b7602-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7602-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7602-152">CommonParameters</span></span>
<span data-ttu-id="b7602-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7602-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7602-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7602-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7602-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7602-155">INPUTS</span></span>

### <span data-ttu-id="b7602-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b7602-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="b7602-157">System.String</span><span class="sxs-lookup"><span data-stu-id="b7602-157">System.String</span></span>

### <span data-ttu-id="b7602-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7602-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="b7602-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b7602-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="b7602-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b7602-160">System.String[]</span></span>

### <span data-ttu-id="b7602-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="b7602-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="b7602-162">Microsoft.Azure.Commands.Network.Models.PSD[]</span><span class="sxs-lookup"><span data-stu-id="b7602-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="b7602-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7602-163">OUTPUTS</span></span>

### <span data-ttu-id="b7602-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b7602-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b7602-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7602-165">NOTES</span></span>

## <span data-ttu-id="b7602-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7602-166">RELATED LINKS</span></span>

[<span data-ttu-id="b7602-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7602-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b7602-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7602-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b7602-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7602-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b7602-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7602-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
