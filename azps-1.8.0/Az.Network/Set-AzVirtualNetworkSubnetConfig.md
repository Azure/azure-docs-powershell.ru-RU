---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4e0356f738bcc0abd52f0ec72c4c6766af8be550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729950"
---
# <span data-ttu-id="9383f-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9383f-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9383f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9383f-102">SYNOPSIS</span></span>
<span data-ttu-id="9383f-103">Обновляет конфигурацию подсети для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9383f-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="9383f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9383f-104">SYNTAX</span></span>

### <span data-ttu-id="9383f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9383f-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9383f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9383f-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9383f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9383f-107">DESCRIPTION</span></span>
<span data-ttu-id="9383f-108">Командлет **Set-AzVirtualNetworkSubnetConfig** обновляет конфигурацию подсети для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9383f-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="9383f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9383f-109">EXAMPLES</span></span>

### <span data-ttu-id="9383f-110">1: изменение префикса адреса подсети</span><span class="sxs-lookup"><span data-stu-id="9383f-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="9383f-111">В этом примере создается виртуальная сеть с одной подсетью.</span><span class="sxs-lookup"><span data-stu-id="9383f-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="9383f-112">Затем вызывает Set-AzVirtualNetworkSubnetConfig, чтобы изменить AddressPrefix подсети.</span><span class="sxs-lookup"><span data-stu-id="9383f-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="9383f-113">Это влияет только на представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="9383f-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9383f-114">Set-AzVirtualNetwork вызывается, чтобы изменить виртуальную сеть в Azure.</span><span class="sxs-lookup"><span data-stu-id="9383f-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="9383f-115">2. Добавьте сетевую группу безопасности в подсеть.</span><span class="sxs-lookup"><span data-stu-id="9383f-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="9383f-116">В этом примере создается группа ресурсов с одной виртуальной сетью, которая содержит только одну подсеть.</span><span class="sxs-lookup"><span data-stu-id="9383f-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="9383f-117">Затем он создает сетевую группу безопасности с правилом разрешения для трафика RDP.</span><span class="sxs-lookup"><span data-stu-id="9383f-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="9383f-118">Командлет Set-AzVirtualNetworkSubnetConfig используется для изменения представления в памяти подсети с интерфейсом, чтобы она указывала на только что созданную сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="9383f-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="9383f-119">Затем вызывается командлет Set-AzVirtualNetwork, чтобы записать измененное состояние обратно в службу.</span><span class="sxs-lookup"><span data-stu-id="9383f-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="9383f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9383f-120">PARAMETERS</span></span>

### <span data-ttu-id="9383f-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9383f-121">-AddressPrefix</span></span>
<span data-ttu-id="9383f-122">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="9383f-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="9383f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9383f-123">-DefaultProfile</span></span>
<span data-ttu-id="9383f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9383f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9383f-125">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="9383f-125">-Delegation</span></span>
<span data-ttu-id="9383f-126">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="9383f-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="9383f-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9383f-127">-Name</span></span>
<span data-ttu-id="9383f-128">Указывает имя конфигурации подсети, которая настраивается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9383f-128">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="9383f-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9383f-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9383f-130">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="9383f-130">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="9383f-131">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9383f-131">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="9383f-132">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="9383f-132">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="9383f-133">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="9383f-133">-RouteTable</span></span>
<span data-ttu-id="9383f-134">Указывает объект таблицы маршрутов, связанный с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="9383f-134">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="9383f-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="9383f-135">-RouteTableId</span></span>
<span data-ttu-id="9383f-136">Указывает идентификатор объекта таблицы маршрутов, связанного с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="9383f-136">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="9383f-137">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9383f-137">-ServiceEndpoint</span></span>
<span data-ttu-id="9383f-138">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="9383f-138">Service Endpoint Value</span></span>

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

### <span data-ttu-id="9383f-139">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9383f-139">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="9383f-140">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="9383f-140">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="9383f-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9383f-141">-VirtualNetwork</span></span>
<span data-ttu-id="9383f-142">Указывает объект **VirtualNetwork** , который содержит конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="9383f-142">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="9383f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9383f-143">CommonParameters</span></span>
<span data-ttu-id="9383f-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9383f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9383f-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9383f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9383f-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9383f-146">INPUTS</span></span>

### <span data-ttu-id="9383f-147">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9383f-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="9383f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="9383f-148">System.String</span></span>

### <span data-ttu-id="9383f-149">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9383f-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="9383f-150">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9383f-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="9383f-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="9383f-151">System.String[]</span></span>

### <span data-ttu-id="9383f-152">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="9383f-152">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="9383f-153">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="9383f-153">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="9383f-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9383f-154">OUTPUTS</span></span>

### <span data-ttu-id="9383f-155">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9383f-155">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9383f-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="9383f-156">NOTES</span></span>

## <span data-ttu-id="9383f-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9383f-157">RELATED LINKS</span></span>

[<span data-ttu-id="9383f-158">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9383f-158">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9383f-159">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9383f-159">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9383f-160">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9383f-160">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9383f-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9383f-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)
