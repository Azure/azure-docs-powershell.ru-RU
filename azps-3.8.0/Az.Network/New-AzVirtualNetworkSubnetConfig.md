---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 144d04172f3169075a32c5e8111a90ff407532b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073229"
---
# <span data-ttu-id="44c0b-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44c0b-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="44c0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="44c0b-103">Создание конфигурации подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="44c0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44c0b-104">SYNTAX</span></span>

### <span data-ttu-id="44c0b-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44c0b-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44c0b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="44c0b-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44c0b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44c0b-107">DESCRIPTION</span></span>
<span data-ttu-id="44c0b-108">Командлет **New-AzVirtualNetworkSubnetConfig** создает конфигурацию подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="44c0b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44c0b-109">EXAMPLES</span></span>

### <span data-ttu-id="44c0b-110">1. Создайте виртуальную сеть с двумя подсетями и группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

<span data-ttu-id="44c0b-111">В этом примере создается две новые конфигурации подсети с помощью командлета New-AzVirtualSubnetConfig, а затем они используются для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="44c0b-112">Шаблон New-AzVirtualSubnetConfig только создает представление подсети в памяти.</span><span class="sxs-lookup"><span data-stu-id="44c0b-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="44c0b-113">В этом примере frontendSubnet имеет CIDR 10.0.1.0/24 и ссылается на сетевую группу безопасности, разрешающую доступ к RDP.</span><span class="sxs-lookup"><span data-stu-id="44c0b-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="44c0b-114">BackendSubnet имеет CIDR 10.0.2.0/24 и ссылается на одну и ту же группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="44c0b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44c0b-115">PARAMETERS</span></span>

### <span data-ttu-id="44c0b-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="44c0b-116">-AddressPrefix</span></span>
<span data-ttu-id="44c0b-117">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="44c0b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c0b-118">-DefaultProfile</span></span>
<span data-ttu-id="44c0b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44c0b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44c0b-120">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="44c0b-120">-Delegation</span></span>
<span data-ttu-id="44c0b-121">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="44c0b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44c0b-122">-InputObject</span></span>
<span data-ttu-id="44c0b-123">Указывает шлюз NAT, связанный с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="44c0b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44c0b-124">-Name</span></span>
<span data-ttu-id="44c0b-125">Указывает имя конфигурации подсети, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="44c0b-125">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="44c0b-126">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="44c0b-126">-NetworkSecurityGroup</span></span>
<span data-ttu-id="44c0b-127">Указывает объект NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="44c0b-127">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="44c0b-128">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="44c0b-128">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="44c0b-129">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="44c0b-129">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="44c0b-130">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="44c0b-130">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="44c0b-131">Настройте, чтобы включить или отключить применение политик сети в частной конечной точке в подсети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-131">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="44c0b-132">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="44c0b-132">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="44c0b-133">Настройте, чтобы включить или отключить применение сетевых политик в службе частной ссылки в подсети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-133">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="44c0b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44c0b-134">-ResourceId</span></span>
<span data-ttu-id="44c0b-135">Указывает идентификатор ресурса шлюза NAT, связанного с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-135">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="44c0b-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="44c0b-136">-RouteTable</span></span>
<span data-ttu-id="44c0b-137">Указывает таблицу маршрутов, связанную с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-137">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="44c0b-138">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="44c0b-138">-RouteTableId</span></span>
<span data-ttu-id="44c0b-139">Указывает идентификатор таблицы маршрутов, связанной с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="44c0b-139">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="44c0b-140">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="44c0b-140">-ServiceEndpoint</span></span>
<span data-ttu-id="44c0b-141">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="44c0b-141">Service Endpoint Value</span></span>

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

### <span data-ttu-id="44c0b-142">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="44c0b-142">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="44c0b-143">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="44c0b-143">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="44c0b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c0b-144">CommonParameters</span></span>
<span data-ttu-id="44c0b-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44c0b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c0b-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44c0b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c0b-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44c0b-147">INPUTS</span></span>

### <span data-ttu-id="44c0b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="44c0b-148">System.String</span></span>

### <span data-ttu-id="44c0b-149">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="44c0b-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="44c0b-150">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="44c0b-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="44c0b-151">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="44c0b-151">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="44c0b-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="44c0b-152">System.String[]</span></span>

### <span data-ttu-id="44c0b-153">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="44c0b-153">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="44c0b-154">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="44c0b-154">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="44c0b-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44c0b-155">OUTPUTS</span></span>

### <span data-ttu-id="44c0b-156">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="44c0b-156">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="44c0b-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="44c0b-157">NOTES</span></span>

## <span data-ttu-id="44c0b-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44c0b-158">RELATED LINKS</span></span>

[<span data-ttu-id="44c0b-159">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44c0b-159">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="44c0b-160">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44c0b-160">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="44c0b-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44c0b-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="44c0b-162">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="44c0b-162">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
