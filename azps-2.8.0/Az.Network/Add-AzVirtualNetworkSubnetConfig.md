---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fea7f3f3d24595cdddd9635e73e3073efe5cb867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903053"
---
# <span data-ttu-id="15a02-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15a02-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="15a02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15a02-102">SYNOPSIS</span></span>
<span data-ttu-id="15a02-103">Добавляет конфигурацию подсети в виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="15a02-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="15a02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15a02-104">SYNTAX</span></span>

### <span data-ttu-id="15a02-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15a02-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15a02-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="15a02-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15a02-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15a02-107">DESCRIPTION</span></span>
<span data-ttu-id="15a02-108">Командлет **Add-AzVirtualNetworkSubnetConfig** добавляет конфигурацию подсети в существующую виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="15a02-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="15a02-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15a02-109">EXAMPLES</span></span>

### <span data-ttu-id="15a02-110">1: Добавление подсети в существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="15a02-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="15a02-111">В этом примере сначала создается группа ресурсов в качестве контейнера ресурсов, которые необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="15a02-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="15a02-112">Затем он создает конфигурацию подсети и использует ее для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="15a02-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="15a02-113">Затем Add-AzVirtualNetworkSubnetConfig используется для добавления подсети в представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="15a02-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="15a02-114">Команда Set-AzVirtualNetwork обновляет существующую виртуальную сеть, используя новую подсеть.</span><span class="sxs-lookup"><span data-stu-id="15a02-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="15a02-115">2. Добавление делегирования для подсети, добавленной в существующую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="15a02-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="15a02-116">В этом примере сначала получается Существующая виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="15a02-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="15a02-117">Затем он создает объект делегирования в памяти.</span><span class="sxs-lookup"><span data-stu-id="15a02-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="15a02-118">Наконец, она создает новую подсеть с таким делегированием, которая добавляется в виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="15a02-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="15a02-119">После этого измененная конфигурация будет отправлена на сервер.</span><span class="sxs-lookup"><span data-stu-id="15a02-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="15a02-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15a02-120">PARAMETERS</span></span>

### <span data-ttu-id="15a02-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="15a02-121">-AddressPrefix</span></span>
<span data-ttu-id="15a02-122">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="15a02-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="15a02-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a02-123">-DefaultProfile</span></span>
<span data-ttu-id="15a02-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15a02-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15a02-125">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="15a02-125">-Delegation</span></span>
<span data-ttu-id="15a02-126">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="15a02-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="15a02-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15a02-127">-InputObject</span></span>
<span data-ttu-id="15a02-128">Определяет шлюз NAT, связанный с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="15a02-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="15a02-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15a02-129">-Name</span></span>
<span data-ttu-id="15a02-130">Указывает имя конфигурации подсети, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="15a02-130">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="15a02-131">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="15a02-131">-NetworkSecurityGroup</span></span>
<span data-ttu-id="15a02-132">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="15a02-132">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="15a02-133">Этот командлет добавляет конфигурацию подсети виртуальной сети к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="15a02-133">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="15a02-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="15a02-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="15a02-135">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="15a02-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="15a02-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="15a02-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="15a02-137">Настройте, чтобы включить или отключить применение политик сети в частной конечной точке в подсети.</span><span class="sxs-lookup"><span data-stu-id="15a02-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="15a02-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="15a02-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="15a02-139">Настройте, чтобы включить или отключить применение сетевых политик в службе частной ссылки в подсети.</span><span class="sxs-lookup"><span data-stu-id="15a02-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="15a02-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15a02-140">-ResourceId</span></span>
<span data-ttu-id="15a02-141">Указывает идентификатор ресурса шлюза NAT, связанного с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="15a02-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="15a02-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="15a02-142">-RouteTable</span></span>
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

### <span data-ttu-id="15a02-143">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="15a02-143">-RouteTableId</span></span>
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

### <span data-ttu-id="15a02-144">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="15a02-144">-ServiceEndpoint</span></span>
<span data-ttu-id="15a02-145">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="15a02-145">Service Endpoint Value</span></span>

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

### <span data-ttu-id="15a02-146">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="15a02-146">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="15a02-147">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="15a02-147">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="15a02-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15a02-148">-VirtualNetwork</span></span>
<span data-ttu-id="15a02-149">Указывает объект **VirtualNetwork** , в который нужно добавить конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="15a02-149">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="15a02-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a02-150">CommonParameters</span></span>
<span data-ttu-id="15a02-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15a02-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a02-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15a02-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a02-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15a02-153">INPUTS</span></span>

### <span data-ttu-id="15a02-154">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15a02-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="15a02-155">System. String</span><span class="sxs-lookup"><span data-stu-id="15a02-155">System.String</span></span>

### <span data-ttu-id="15a02-156">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="15a02-156">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="15a02-157">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="15a02-157">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="15a02-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="15a02-158">System.String[]</span></span>

### <span data-ttu-id="15a02-159">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="15a02-159">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="15a02-160">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="15a02-160">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="15a02-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15a02-161">OUTPUTS</span></span>

### <span data-ttu-id="15a02-162">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15a02-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="15a02-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="15a02-163">NOTES</span></span>

## <span data-ttu-id="15a02-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15a02-164">RELATED LINKS</span></span>

[<span data-ttu-id="15a02-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15a02-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="15a02-166">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15a02-166">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="15a02-167">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15a02-167">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="15a02-168">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="15a02-168">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
