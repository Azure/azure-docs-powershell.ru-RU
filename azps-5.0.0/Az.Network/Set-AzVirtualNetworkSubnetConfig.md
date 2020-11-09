---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: fe6c67c39ef3d14ec1b1e4200b4fad09aa7d2a24
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316592"
---
# <span data-ttu-id="5de5f-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5de5f-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5de5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5de5f-102">SYNOPSIS</span></span>
<span data-ttu-id="5de5f-103">Обновляет конфигурацию подсети для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="5de5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5de5f-104">SYNTAX</span></span>

### <span data-ttu-id="5de5f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5de5f-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5de5f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5de5f-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5de5f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5de5f-107">DESCRIPTION</span></span>
<span data-ttu-id="5de5f-108">Командлет **Set-AzVirtualNetworkSubnetConfig** обновляет конфигурацию подсети для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="5de5f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5de5f-109">EXAMPLES</span></span>

### <span data-ttu-id="5de5f-110">1: изменение префикса адреса подсети</span><span class="sxs-lookup"><span data-stu-id="5de5f-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="5de5f-111">В этом примере создается виртуальная сеть с одной подсетью.</span><span class="sxs-lookup"><span data-stu-id="5de5f-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="5de5f-112">Затем вызывает Set-AzVirtualNetworkSubnetConfig, чтобы изменить AddressPrefix подсети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="5de5f-113">Это влияет только на представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="5de5f-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="5de5f-114">Set-AzVirtualNetwork вызывается, чтобы изменить виртуальную сеть в Azure.</span><span class="sxs-lookup"><span data-stu-id="5de5f-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="5de5f-115">2. Добавьте сетевую группу безопасности в подсеть.</span><span class="sxs-lookup"><span data-stu-id="5de5f-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="5de5f-116">В этом примере создается группа ресурсов с одной виртуальной сетью, которая содержит только одну подсеть.</span><span class="sxs-lookup"><span data-stu-id="5de5f-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="5de5f-117">Затем он создает сетевую группу безопасности с правилом разрешения для трафика RDP.</span><span class="sxs-lookup"><span data-stu-id="5de5f-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="5de5f-118">Командлет Set-AzVirtualNetworkSubnetConfig используется для изменения представления в памяти подсети с интерфейсом, чтобы она указывала на только что созданную сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="5de5f-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="5de5f-119">Затем вызывается командлет Set-AzVirtualNetwork, чтобы записать измененное состояние обратно в службу.</span><span class="sxs-lookup"><span data-stu-id="5de5f-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="5de5f-120">3. Подключи шлюз NAT к подсети</span><span class="sxs-lookup"><span data-stu-id="5de5f-120">3: Attach a Nat Gateway to a subnet</span></span>
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

## <span data-ttu-id="5de5f-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5de5f-121">PARAMETERS</span></span>

### <span data-ttu-id="5de5f-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5de5f-122">-AddressPrefix</span></span>
<span data-ttu-id="5de5f-123">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="5de5f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de5f-124">-DefaultProfile</span></span>
<span data-ttu-id="5de5f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5de5f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5de5f-126">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="5de5f-126">-Delegation</span></span>
<span data-ttu-id="5de5f-127">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="5de5f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5de5f-128">-InputObject</span></span>
<span data-ttu-id="5de5f-129">Определяет шлюз NAT, связанный с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="5de5f-130">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="5de5f-130">-IpAllocation</span></span>
<span data-ttu-id="5de5f-131">Указывает IpAllocations для подсети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-131">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="5de5f-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5de5f-132">-Name</span></span>
<span data-ttu-id="5de5f-133">Указывает имя конфигурации подсети, которая настраивается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5de5f-133">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="5de5f-134">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5de5f-134">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5de5f-135">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="5de5f-135">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="5de5f-136">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="5de5f-136">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="5de5f-137">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="5de5f-137">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="5de5f-138">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="5de5f-138">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="5de5f-139">Настройте, чтобы включить или отключить применение политик сети в частной конечной точке в подсети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-139">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="5de5f-140">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="5de5f-140">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="5de5f-141">Настройте, чтобы включить или отключить применение сетевых политик в службе частной ссылки в подсети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-141">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="5de5f-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5de5f-142">-ResourceId</span></span>
<span data-ttu-id="5de5f-143">Указывает идентификатор ресурса шлюза NAT, связанного с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-143">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="5de5f-144">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="5de5f-144">-RouteTable</span></span>
<span data-ttu-id="5de5f-145">Указывает объект таблицы маршрутов, связанный с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-145">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="5de5f-146">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="5de5f-146">-RouteTableId</span></span>
<span data-ttu-id="5de5f-147">Указывает идентификатор объекта таблицы маршрутов, связанного с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-147">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="5de5f-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5de5f-148">-ServiceEndpoint</span></span>
<span data-ttu-id="5de5f-149">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="5de5f-149">Service Endpoint Value</span></span>

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

### <span data-ttu-id="5de5f-150">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5de5f-150">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="5de5f-151">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="5de5f-151">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="5de5f-152">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5de5f-152">-VirtualNetwork</span></span>
<span data-ttu-id="5de5f-153">Указывает объект **VirtualNetwork** , который содержит конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="5de5f-153">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="5de5f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de5f-154">CommonParameters</span></span>
<span data-ttu-id="5de5f-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5de5f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de5f-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5de5f-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de5f-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5de5f-157">INPUTS</span></span>

### <span data-ttu-id="5de5f-158">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5de5f-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="5de5f-159">System. String</span><span class="sxs-lookup"><span data-stu-id="5de5f-159">System.String</span></span>

### <span data-ttu-id="5de5f-160">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5de5f-160">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="5de5f-161">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5de5f-161">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="5de5f-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="5de5f-162">System.String[]</span></span>

### <span data-ttu-id="5de5f-163">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="5de5f-163">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="5de5f-164">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="5de5f-164">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="5de5f-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5de5f-165">OUTPUTS</span></span>

### <span data-ttu-id="5de5f-166">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5de5f-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5de5f-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="5de5f-167">NOTES</span></span>

## <span data-ttu-id="5de5f-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5de5f-168">RELATED LINKS</span></span>

[<span data-ttu-id="5de5f-169">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5de5f-169">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5de5f-170">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5de5f-170">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5de5f-171">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5de5f-171">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5de5f-172">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5de5f-172">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
