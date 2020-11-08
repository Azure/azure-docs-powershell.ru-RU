---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: c3d01639d428820578ffe8a319bddd591c007e00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248377"
---
# <span data-ttu-id="508ec-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="508ec-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="508ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="508ec-102">SYNOPSIS</span></span>
<span data-ttu-id="508ec-103">Добавляет конфигурацию подсети в виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="508ec-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="508ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="508ec-104">SYNTAX</span></span>

### <span data-ttu-id="508ec-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="508ec-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="508ec-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="508ec-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="508ec-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="508ec-107">DESCRIPTION</span></span>
<span data-ttu-id="508ec-108">Командлет **Add-AzVirtualNetworkSubnetConfig** добавляет конфигурацию подсети в существующую виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="508ec-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="508ec-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="508ec-109">EXAMPLES</span></span>

### <span data-ttu-id="508ec-110">Пример 1: Добавление подсети в существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="508ec-110">Example 1: Add a subnet to an existing virtual network</span></span>
```powershell
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="508ec-111">В этом примере сначала создается группа ресурсов в качестве контейнера ресурсов, которые необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="508ec-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="508ec-112">Затем он создает конфигурацию подсети и использует ее для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="508ec-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="508ec-113">Затем Add-AzVirtualNetworkSubnetConfig используется для добавления подсети в представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="508ec-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="508ec-114">Команда Set-AzVirtualNetwork обновляет существующую виртуальную сеть, используя новую подсеть.</span><span class="sxs-lookup"><span data-stu-id="508ec-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="508ec-115">Пример 2: Добавление делегирования для подсети, добавленной в существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="508ec-115">Example 2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="508ec-116">В этом примере сначала получается Существующая виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="508ec-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="508ec-117">Затем он создает объект делегирования в памяти.</span><span class="sxs-lookup"><span data-stu-id="508ec-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="508ec-118">Наконец, она создает новую подсеть с таким делегированием, которая добавляется в виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="508ec-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="508ec-119">После этого измененная конфигурация будет отправлена на сервер.</span><span class="sxs-lookup"><span data-stu-id="508ec-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="508ec-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="508ec-120">PARAMETERS</span></span>

### <span data-ttu-id="508ec-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="508ec-121">-AddressPrefix</span></span>
<span data-ttu-id="508ec-122">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="508ec-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="508ec-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="508ec-123">-DefaultProfile</span></span>
<span data-ttu-id="508ec-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="508ec-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="508ec-125">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="508ec-125">-Delegation</span></span>
<span data-ttu-id="508ec-126">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="508ec-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="508ec-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="508ec-127">-InputObject</span></span>
<span data-ttu-id="508ec-128">Определяет шлюз NAT, связанный с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="508ec-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="508ec-129">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="508ec-129">-IpAllocation</span></span>
<span data-ttu-id="508ec-130">Указывает IpAllocations для подсети.</span><span class="sxs-lookup"><span data-stu-id="508ec-130">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="508ec-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="508ec-131">-Name</span></span>
<span data-ttu-id="508ec-132">Указывает имя конфигурации подсети, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="508ec-132">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="508ec-133">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="508ec-133">-NetworkSecurityGroup</span></span>
<span data-ttu-id="508ec-134">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="508ec-134">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="508ec-135">Этот командлет добавляет конфигурацию подсети виртуальной сети к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="508ec-135">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="508ec-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="508ec-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="508ec-137">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="508ec-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="508ec-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="508ec-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="508ec-139">Настройте, чтобы включить или отключить применение политик сети в частной конечной точке в подсети.</span><span class="sxs-lookup"><span data-stu-id="508ec-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="508ec-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="508ec-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="508ec-141">Настройте, чтобы включить или отключить применение сетевых политик в службе частной ссылки в подсети.</span><span class="sxs-lookup"><span data-stu-id="508ec-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="508ec-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="508ec-142">-ResourceId</span></span>
<span data-ttu-id="508ec-143">Указывает идентификатор ресурса шлюза NAT, связанного с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="508ec-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="508ec-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="508ec-144">-RouteTable</span></span>
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

### <span data-ttu-id="508ec-145">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="508ec-145">-RouteTableId</span></span>
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

### <span data-ttu-id="508ec-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="508ec-146">-ServiceEndpoint</span></span>
<span data-ttu-id="508ec-147">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="508ec-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="508ec-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="508ec-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="508ec-149">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="508ec-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="508ec-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="508ec-150">-VirtualNetwork</span></span>
<span data-ttu-id="508ec-151">Указывает объект **VirtualNetwork** , в который нужно добавить конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="508ec-151">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="508ec-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="508ec-152">CommonParameters</span></span>
<span data-ttu-id="508ec-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="508ec-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="508ec-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="508ec-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="508ec-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="508ec-155">INPUTS</span></span>

### <span data-ttu-id="508ec-156">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="508ec-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="508ec-157">System. String</span><span class="sxs-lookup"><span data-stu-id="508ec-157">System.String</span></span>

### <span data-ttu-id="508ec-158">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="508ec-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="508ec-159">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="508ec-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="508ec-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="508ec-160">System.String[]</span></span>

### <span data-ttu-id="508ec-161">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="508ec-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="508ec-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="508ec-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="508ec-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="508ec-163">OUTPUTS</span></span>

### <span data-ttu-id="508ec-164">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="508ec-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="508ec-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="508ec-165">NOTES</span></span>

## <span data-ttu-id="508ec-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="508ec-166">RELATED LINKS</span></span>

[<span data-ttu-id="508ec-167">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="508ec-167">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="508ec-168">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="508ec-168">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="508ec-169">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="508ec-169">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="508ec-170">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="508ec-170">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
