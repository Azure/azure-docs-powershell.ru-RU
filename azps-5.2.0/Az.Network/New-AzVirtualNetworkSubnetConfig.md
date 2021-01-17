---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7afedb15ea5e7b5e2968dbb425a662f7de7e2ac1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412324"
---
# <span data-ttu-id="60bad-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="60bad-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="60bad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60bad-102">SYNOPSIS</span></span>
<span data-ttu-id="60bad-103">Создает конфигурацию виртуальной подсети сети.</span><span class="sxs-lookup"><span data-stu-id="60bad-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="60bad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60bad-104">SYNTAX</span></span>

### <span data-ttu-id="60bad-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60bad-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60bad-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="60bad-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-IpAllocation <PSIpAllocation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60bad-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60bad-107">DESCRIPTION</span></span>
<span data-ttu-id="60bad-108">**Командлет New-AzVirtualNetworkSubnetConfig** создает конфигурацию виртуальной подсети сети.</span><span class="sxs-lookup"><span data-stu-id="60bad-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="60bad-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60bad-109">EXAMPLES</span></span>

### <span data-ttu-id="60bad-110">Пример 1. Создание виртуальной сети с двумя подсетями и группой безопасности сети</span><span class="sxs-lookup"><span data-stu-id="60bad-110">Example 1: Create a virtual network with two subnets and a network security group</span></span>
```powershell
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

<span data-ttu-id="60bad-111">В этом примере создаются две конфигурации подсети с New-AzVirtualSubnetConfig и используется для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="60bad-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="60bad-112">Шаблон New-AzVirtualSubnetConfig создает только представление подсети в памяти.</span><span class="sxs-lookup"><span data-stu-id="60bad-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="60bad-113">В этом примере frontendSubnet имеет CIDR 10.0.1.0/24 и ссылается на группу безопасности сети, которая обеспечивает доступ RDP.</span><span class="sxs-lookup"><span data-stu-id="60bad-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="60bad-114">В backendSubnet есть CIDR 10.0.2.0/24 и она ссылается на ту же группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="60bad-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="60bad-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60bad-115">PARAMETERS</span></span>

### <span data-ttu-id="60bad-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="60bad-116">-AddressPrefix</span></span>
<span data-ttu-id="60bad-117">Диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="60bad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60bad-118">-DefaultProfile</span></span>
<span data-ttu-id="60bad-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60bad-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60bad-120">-Delegation</span><span class="sxs-lookup"><span data-stu-id="60bad-120">-Delegation</span></span>
<span data-ttu-id="60bad-121">Список служб с разрешением на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="60bad-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60bad-122">-InputObject</span></span>
<span data-ttu-id="60bad-123">Указывает шлюз NAT, связанный с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="60bad-124">-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="60bad-124">-IpAllocation</span></span>
<span data-ttu-id="60bad-125">IpAllocations для подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-125">Specifies IpAllocations for a subnet.</span></span>

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

### <span data-ttu-id="60bad-126">-Name</span><span class="sxs-lookup"><span data-stu-id="60bad-126">-Name</span></span>
<span data-ttu-id="60bad-127">Имя создаемой конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-127">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="60bad-128">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="60bad-128">-NetworkSecurityGroup</span></span>
<span data-ttu-id="60bad-129">Объект NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="60bad-129">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="60bad-130">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="60bad-130">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="60bad-131">Определяет ИД группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="60bad-131">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="60bad-132">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="60bad-132">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="60bad-133">Настройте или отключаете применение сетевых политик на закрытой конечной точке в подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-133">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="60bad-134">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="60bad-134">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="60bad-135">Настройте возможность или отключение применения сетевых политик в службе частных ссылок в подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-135">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="60bad-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60bad-136">-ResourceId</span></span>
<span data-ttu-id="60bad-137">Определяет ИД ресурса шлюза NAT, связанного с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-137">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="60bad-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="60bad-138">-RouteTable</span></span>
<span data-ttu-id="60bad-139">Указывает таблицу маршрутов, связанную с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-139">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="60bad-140">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="60bad-140">-RouteTableId</span></span>
<span data-ttu-id="60bad-141">Определяет ИД таблицы маршрутов, связанной с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="60bad-141">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="60bad-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="60bad-142">-ServiceEndpoint</span></span>
<span data-ttu-id="60bad-143">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="60bad-143">Service Endpoint Value</span></span>

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

### <span data-ttu-id="60bad-144">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="60bad-144">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="60bad-145">Политики конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="60bad-145">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="60bad-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60bad-146">CommonParameters</span></span>
<span data-ttu-id="60bad-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60bad-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60bad-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60bad-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60bad-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60bad-149">INPUTS</span></span>

### <span data-ttu-id="60bad-150">System.String</span><span class="sxs-lookup"><span data-stu-id="60bad-150">System.String</span></span>

### <span data-ttu-id="60bad-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="60bad-151">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="60bad-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="60bad-152">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="60bad-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="60bad-153">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="60bad-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="60bad-154">System.String[]</span></span>

### <span data-ttu-id="60bad-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span><span class="sxs-lookup"><span data-stu-id="60bad-155">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="60bad-156">Microsoft.Azure.Commands.Network.Models.PSD[]</span><span class="sxs-lookup"><span data-stu-id="60bad-156">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="60bad-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60bad-157">OUTPUTS</span></span>

### <span data-ttu-id="60bad-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="60bad-158">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="60bad-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60bad-159">NOTES</span></span>

## <span data-ttu-id="60bad-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60bad-160">RELATED LINKS</span></span>

[<span data-ttu-id="60bad-161">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="60bad-161">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="60bad-162">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="60bad-162">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="60bad-163">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="60bad-163">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="60bad-164">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="60bad-164">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
