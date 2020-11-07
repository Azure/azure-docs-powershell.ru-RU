---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1df94cc14191fcb95e271bf5fef6b1a09fa77060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730682"
---
# <span data-ttu-id="dee7a-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dee7a-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="dee7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dee7a-102">SYNOPSIS</span></span>
<span data-ttu-id="dee7a-103">Добавляет конфигурацию подсети в виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="dee7a-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="dee7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dee7a-104">SYNTAX</span></span>

### <span data-ttu-id="dee7a-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dee7a-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dee7a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dee7a-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee7a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dee7a-107">DESCRIPTION</span></span>
<span data-ttu-id="dee7a-108">Командлет **Add-AzVirtualNetworkSubnetConfig** добавляет конфигурацию подсети в существующую виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="dee7a-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="dee7a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dee7a-109">EXAMPLES</span></span>

### <span data-ttu-id="dee7a-110">1: Добавление подсети в существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="dee7a-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="dee7a-111">В этом примере сначала создается группа ресурсов в качестве контейнера ресурсов, которые необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="dee7a-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="dee7a-112">Затем он создает конфигурацию подсети и использует ее для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dee7a-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="dee7a-113">Затем Add-AzVirtualNetworkSubnetConfig используется для добавления подсети в представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="dee7a-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="dee7a-114">Команда Set-AzVirtualNetwork обновляет существующую виртуальную сеть, используя новую подсеть.</span><span class="sxs-lookup"><span data-stu-id="dee7a-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="dee7a-115">2. Добавление делегирования для подсети, добавленной в существующую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="dee7a-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="dee7a-116">В этом примере сначала получается Существующая виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="dee7a-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="dee7a-117">Затем он создает объект делегирования в памяти.</span><span class="sxs-lookup"><span data-stu-id="dee7a-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="dee7a-118">Наконец, она создает новую подсеть с таким делегированием, которая добавляется в виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="dee7a-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="dee7a-119">После этого измененная конфигурация будет отправлена на сервер.</span><span class="sxs-lookup"><span data-stu-id="dee7a-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="dee7a-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dee7a-120">PARAMETERS</span></span>

### <span data-ttu-id="dee7a-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dee7a-121">-AddressPrefix</span></span>
<span data-ttu-id="dee7a-122">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="dee7a-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="dee7a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee7a-123">-DefaultProfile</span></span>
<span data-ttu-id="dee7a-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dee7a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dee7a-125">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="dee7a-125">-Delegation</span></span>
<span data-ttu-id="dee7a-126">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="dee7a-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="dee7a-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dee7a-127">-Name</span></span>
<span data-ttu-id="dee7a-128">Указывает имя конфигурации подсети, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="dee7a-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="dee7a-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dee7a-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="dee7a-130">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="dee7a-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="dee7a-131">Этот командлет добавляет конфигурацию подсети виртуальной сети к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="dee7a-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="dee7a-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="dee7a-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="dee7a-133">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="dee7a-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="dee7a-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="dee7a-134">-RouteTable</span></span>
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

### <span data-ttu-id="dee7a-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="dee7a-135">-RouteTableId</span></span>
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

### <span data-ttu-id="dee7a-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="dee7a-136">-ServiceEndpoint</span></span>
<span data-ttu-id="dee7a-137">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="dee7a-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="dee7a-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dee7a-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="dee7a-139">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="dee7a-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="dee7a-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dee7a-140">-VirtualNetwork</span></span>
<span data-ttu-id="dee7a-141">Указывает объект **VirtualNetwork** , в который нужно добавить конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="dee7a-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="dee7a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee7a-142">CommonParameters</span></span>
<span data-ttu-id="dee7a-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dee7a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee7a-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee7a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee7a-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dee7a-145">INPUTS</span></span>

### <span data-ttu-id="dee7a-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dee7a-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="dee7a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="dee7a-147">System.String</span></span>

### <span data-ttu-id="dee7a-148">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dee7a-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="dee7a-149">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dee7a-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="dee7a-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="dee7a-150">System.String[]</span></span>

### <span data-ttu-id="dee7a-151">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="dee7a-151">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="dee7a-152">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="dee7a-152">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="dee7a-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dee7a-153">OUTPUTS</span></span>

### <span data-ttu-id="dee7a-154">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dee7a-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="dee7a-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="dee7a-155">NOTES</span></span>

## <span data-ttu-id="dee7a-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dee7a-156">RELATED LINKS</span></span>

[<span data-ttu-id="dee7a-157">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dee7a-157">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dee7a-158">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dee7a-158">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dee7a-159">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dee7a-159">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dee7a-160">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dee7a-160">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
