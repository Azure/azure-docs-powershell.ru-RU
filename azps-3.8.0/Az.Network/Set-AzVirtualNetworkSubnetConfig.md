---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1ef34f3770d4eba273a679de2914184c3bf411a9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065124"
---
# <span data-ttu-id="952c8-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="952c8-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="952c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="952c8-102">SYNOPSIS</span></span>
<span data-ttu-id="952c8-103">Обновляет конфигурацию подсети для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="952c8-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="952c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="952c8-104">SYNTAX</span></span>

### <span data-ttu-id="952c8-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="952c8-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="952c8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="952c8-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="952c8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="952c8-107">DESCRIPTION</span></span>
<span data-ttu-id="952c8-108">Командлет **Set-AzVirtualNetworkSubnetConfig** обновляет конфигурацию подсети для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="952c8-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="952c8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="952c8-109">EXAMPLES</span></span>

### <span data-ttu-id="952c8-110">1: изменение префикса адреса подсети</span><span class="sxs-lookup"><span data-stu-id="952c8-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="952c8-111">В этом примере создается виртуальная сеть с одной подсетью.</span><span class="sxs-lookup"><span data-stu-id="952c8-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="952c8-112">Затем вызывает Set-AzVirtualNetworkSubnetConfig, чтобы изменить AddressPrefix подсети.</span><span class="sxs-lookup"><span data-stu-id="952c8-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="952c8-113">Это влияет только на представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="952c8-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="952c8-114">Set-AzVirtualNetwork вызывается, чтобы изменить виртуальную сеть в Azure.</span><span class="sxs-lookup"><span data-stu-id="952c8-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="952c8-115">2. Добавьте сетевую группу безопасности в подсеть.</span><span class="sxs-lookup"><span data-stu-id="952c8-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="952c8-116">В этом примере создается группа ресурсов с одной виртуальной сетью, которая содержит только одну подсеть.</span><span class="sxs-lookup"><span data-stu-id="952c8-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="952c8-117">Затем он создает сетевую группу безопасности с правилом разрешения для трафика RDP.</span><span class="sxs-lookup"><span data-stu-id="952c8-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="952c8-118">Командлет Set-AzVirtualNetworkSubnetConfig используется для изменения представления в памяти подсети с интерфейсом, чтобы она указывала на только что созданную сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="952c8-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="952c8-119">Затем вызывается командлет Set-AzVirtualNetwork, чтобы записать измененное состояние обратно в службу.</span><span class="sxs-lookup"><span data-stu-id="952c8-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="952c8-120">3. Подключи шлюз NAT к подсети</span><span class="sxs-lookup"><span data-stu-id="952c8-120">3: Attach a Nat Gateway to a subnet</span></span>
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

## <span data-ttu-id="952c8-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="952c8-121">PARAMETERS</span></span>

### <span data-ttu-id="952c8-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="952c8-122">-AddressPrefix</span></span>
<span data-ttu-id="952c8-123">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="952c8-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="952c8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952c8-124">-DefaultProfile</span></span>
<span data-ttu-id="952c8-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="952c8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="952c8-126">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="952c8-126">-Delegation</span></span>
<span data-ttu-id="952c8-127">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="952c8-127">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="952c8-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="952c8-128">-InputObject</span></span>
<span data-ttu-id="952c8-129">Определяет шлюз NAT, связанный с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="952c8-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="952c8-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="952c8-130">-Name</span></span>
<span data-ttu-id="952c8-131">Указывает имя конфигурации подсети, которая настраивается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="952c8-131">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="952c8-132">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="952c8-132">-NetworkSecurityGroup</span></span>
<span data-ttu-id="952c8-133">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="952c8-133">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="952c8-134">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="952c8-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="952c8-135">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="952c8-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="952c8-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="952c8-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="952c8-137">Настройте, чтобы включить или отключить применение политик сети в частной конечной точке в подсети.</span><span class="sxs-lookup"><span data-stu-id="952c8-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="952c8-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="952c8-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="952c8-139">Настройте, чтобы включить или отключить применение сетевых политик в службе частной ссылки в подсети.</span><span class="sxs-lookup"><span data-stu-id="952c8-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="952c8-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="952c8-140">-ResourceId</span></span>
<span data-ttu-id="952c8-141">Указывает идентификатор ресурса шлюза NAT, связанного с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="952c8-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="952c8-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="952c8-142">-RouteTable</span></span>
<span data-ttu-id="952c8-143">Указывает объект таблицы маршрутов, связанный с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="952c8-143">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="952c8-144">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="952c8-144">-RouteTableId</span></span>
<span data-ttu-id="952c8-145">Указывает идентификатор объекта таблицы маршрутов, связанного с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="952c8-145">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="952c8-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="952c8-146">-ServiceEndpoint</span></span>
<span data-ttu-id="952c8-147">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="952c8-147">Service Endpoint Value</span></span>

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

### <span data-ttu-id="952c8-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="952c8-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="952c8-149">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="952c8-149">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="952c8-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="952c8-150">-VirtualNetwork</span></span>
<span data-ttu-id="952c8-151">Указывает объект **VirtualNetwork** , который содержит конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="952c8-151">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="952c8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952c8-152">CommonParameters</span></span>
<span data-ttu-id="952c8-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="952c8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952c8-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="952c8-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952c8-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="952c8-155">INPUTS</span></span>

### <span data-ttu-id="952c8-156">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="952c8-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="952c8-157">System. String</span><span class="sxs-lookup"><span data-stu-id="952c8-157">System.String</span></span>

### <span data-ttu-id="952c8-158">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="952c8-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="952c8-159">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="952c8-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="952c8-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="952c8-160">System.String[]</span></span>

### <span data-ttu-id="952c8-161">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="952c8-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="952c8-162">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="952c8-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="952c8-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="952c8-163">OUTPUTS</span></span>

### <span data-ttu-id="952c8-164">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="952c8-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="952c8-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="952c8-165">NOTES</span></span>

## <span data-ttu-id="952c8-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="952c8-166">RELATED LINKS</span></span>

[<span data-ttu-id="952c8-167">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="952c8-167">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="952c8-168">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="952c8-168">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="952c8-169">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="952c8-169">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="952c8-170">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="952c8-170">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
