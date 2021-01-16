---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fe6c67c39ef3d14ec1b1e4200b4fad09aa7d2a24
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519870"
---
# <span data-ttu-id="a9b19-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9b19-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a9b19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9b19-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b19-103">Обновляет конфигурацию подсети для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="a9b19-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a9b19-104">SYNTAX</span></span>

### <span data-ttu-id="a9b19-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9b19-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9b19-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9b19-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9b19-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9b19-107">DESCRIPTION</span></span>
<span data-ttu-id="a9b19-108">Командлет **Set-AzVirtualNetworkSubnetConfig** обновляет конфигурацию подсети для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="a9b19-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a9b19-109">EXAMPLES</span></span>

### <span data-ttu-id="a9b19-110">1. Изменение префикса адреса подсети</span><span class="sxs-lookup"><span data-stu-id="a9b19-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="a9b19-111">В этом примере создается виртуальная сеть с одной подсетей.</span><span class="sxs-lookup"><span data-stu-id="a9b19-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="a9b19-112">Затем вызывается Set-AzVirtualNetworkSubnetConfig для изменения адресной префикса подсети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="a9b19-113">Это влияет только на представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="a9b19-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="a9b19-114">Set-AzVirtualNetwork называется изменением виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b19-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="a9b19-115">2. Добавление группы безопасности сети в подсеть</span><span class="sxs-lookup"><span data-stu-id="a9b19-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="a9b19-116">В этом примере создается группа ресурсов с одной виртуальной сетью, содержащей только одну подсеть.</span><span class="sxs-lookup"><span data-stu-id="a9b19-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="a9b19-117">Затем она создает группу безопасности сети с правилом, разрешаемой для трафика RDP.</span><span class="sxs-lookup"><span data-stu-id="a9b19-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="a9b19-118">Этот Set-AzVirtualNetworkSubnetConfig используется для изменения представления подсети переднего компьютера в памяти таким образом, чтобы оно указывает на созданную группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="a9b19-119">Затем Set-AzVirtualNetwork, чтобы вернуть измененное состояние в службу.</span><span class="sxs-lookup"><span data-stu-id="a9b19-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="a9b19-120">3. Вложите шлюз NAT в подсеть</span><span class="sxs-lookup"><span data-stu-id="a9b19-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="a9b19-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9b19-121">PARAMETERS</span></span>

### <span data-ttu-id="a9b19-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a9b19-122">-AddressPrefix</span></span>
<span data-ttu-id="a9b19-123">Диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="a9b19-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b19-124">-DefaultProfile</span></span>
<span data-ttu-id="a9b19-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b19-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9b19-126">-Delegation</span><span class="sxs-lookup"><span data-stu-id="a9b19-126">-Delegation</span></span>
<span data-ttu-id="a9b19-127">Список служб с разрешением на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="a9b19-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9b19-128">-InputObject</span></span>
<span data-ttu-id="a9b19-129">Указывает шлюз NAT, связанный с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="a9b19-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="a9b19-130">-IpAllocation</span></span>
<span data-ttu-id="a9b19-131">IpAllocations для подсети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-131">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="a9b19-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a9b19-132">-Name</span></span>
<span data-ttu-id="a9b19-133">Указывает имя конфигурации подсети, настроенной этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9b19-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="a9b19-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a9b19-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a9b19-135">Объект **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="a9b19-135">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="a9b19-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a9b19-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a9b19-137">Определяет ИД группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="a9b19-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="a9b19-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="a9b19-139">Настройте или отключаете применение сетевых политик на закрытой конечной точке в подсети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="a9b19-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="a9b19-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="a9b19-141">Настройте возможность или отключение применения сетевых политик в службе частных ссылок в подсети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="a9b19-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9b19-142">-ResourceId</span></span>
<span data-ttu-id="a9b19-143">Определяет ИД ресурса шлюза NAT, связанного с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="a9b19-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a9b19-144">-RouteTable</span></span>
<span data-ttu-id="a9b19-145">Определяет объект таблицы маршрутов, связанный с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-145">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="a9b19-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="a9b19-146">-RouteTableId</span></span>
<span data-ttu-id="a9b19-147">Определяет ИД объекта таблицы маршрутов, связанного с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="a9b19-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a9b19-148">-ServiceEndpoint</span></span>
<span data-ttu-id="a9b19-149">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="a9b19-149">Service Endpoint Value</span></span>

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

### <span data-ttu-id="a9b19-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a9b19-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a9b19-151">Политики конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="a9b19-151">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="a9b19-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a9b19-152">-VirtualNetwork</span></span>
<span data-ttu-id="a9b19-153">Объект **VirtualNetwork,** который содержит конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="a9b19-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="a9b19-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b19-154">CommonParameters</span></span>
<span data-ttu-id="a9b19-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9b19-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b19-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9b19-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b19-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9b19-157">INPUTS</span></span>

### <span data-ttu-id="a9b19-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a9b19-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="a9b19-159">System.String</span><span class="sxs-lookup"><span data-stu-id="a9b19-159">System.String</span></span>

### <span data-ttu-id="a9b19-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a9b19-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="a9b19-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="a9b19-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="a9b19-162">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a9b19-162">System.String[]</span></span>

### <span data-ttu-id="a9b19-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="a9b19-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="a9b19-164">Microsoft.Azure.Commands.Network.Models.PSD[]</span><span class="sxs-lookup"><span data-stu-id="a9b19-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="a9b19-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a9b19-165">OUTPUTS</span></span>

### <span data-ttu-id="a9b19-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a9b19-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a9b19-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a9b19-167">NOTES</span></span>

## <span data-ttu-id="a9b19-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9b19-168">RELATED LINKS</span></span>

[<span data-ttu-id="a9b19-169">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9b19-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a9b19-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9b19-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a9b19-171">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9b19-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a9b19-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a9b19-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
