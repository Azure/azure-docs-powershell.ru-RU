---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1129b24c69dc362ea4d700be28a0823afa860885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734347"
---
# <span data-ttu-id="58fb8-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58fb8-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="58fb8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="58fb8-103">Добавляет конфигурацию подсети в виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="58fb8-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58fb8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58fb8-104">SYNTAX</span></span>

### <span data-ttu-id="58fb8-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58fb8-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58fb8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="58fb8-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58fb8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58fb8-107">DESCRIPTION</span></span>
<span data-ttu-id="58fb8-108">Командлет **Add-AzureRmVirtualNetworkSubnetConfig** добавляет конфигурацию подсети в существующую виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="58fb8-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="58fb8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58fb8-109">EXAMPLES</span></span>

### <span data-ttu-id="58fb8-110">1: Добавление подсети в существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="58fb8-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="58fb8-111">В этом примере сначала создается группа ресурсов в качестве контейнера ресурсов, которые необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="58fb8-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="58fb8-112">Затем он создает конфигурацию подсети и использует ее для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="58fb8-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="58fb8-113">Затем Add-AzureRmVirtualNetworkSubnetConfig используется для добавления подсети в представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="58fb8-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="58fb8-114">Команда Set-AzureRmVirtualNetwork обновляет существующую виртуальную сеть, используя новую подсеть.</span><span class="sxs-lookup"><span data-stu-id="58fb8-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="58fb8-115">2. Добавление делегирования для подсети, добавленной в существующую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="58fb8-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="58fb8-116">В этом примере сначала получается Существующая виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="58fb8-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="58fb8-117">Затем он создает объект делегирования в памяти.</span><span class="sxs-lookup"><span data-stu-id="58fb8-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="58fb8-118">Наконец, она создает новую подсеть с таким делегированием, которая добавляется в виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="58fb8-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="58fb8-119">После этого измененная конфигурация будет отправлена на сервер.</span><span class="sxs-lookup"><span data-stu-id="58fb8-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="58fb8-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58fb8-120">PARAMETERS</span></span>

### <span data-ttu-id="58fb8-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="58fb8-121">-AddressPrefix</span></span>
<span data-ttu-id="58fb8-122">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="58fb8-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fb8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58fb8-123">-DefaultProfile</span></span>
<span data-ttu-id="58fb8-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58fb8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fb8-125">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="58fb8-125">-Delegation</span></span>
<span data-ttu-id="58fb8-126">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="58fb8-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb8-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58fb8-127">-Name</span></span>
<span data-ttu-id="58fb8-128">Указывает имя конфигурации подсети, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="58fb8-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="58fb8-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58fb8-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="58fb8-130">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="58fb8-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="58fb8-131">Этот командлет добавляет конфигурацию подсети виртуальной сети к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="58fb8-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="58fb8-132">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="58fb8-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="58fb8-133">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="58fb8-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="58fb8-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="58fb8-134">-RouteTable</span></span>
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

### <span data-ttu-id="58fb8-135">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="58fb8-135">-RouteTableId</span></span>
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

### <span data-ttu-id="58fb8-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="58fb8-136">-ServiceEndpoint</span></span>
<span data-ttu-id="58fb8-137">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="58fb8-137">Service Endpoint Value</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb8-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="58fb8-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="58fb8-139">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="58fb8-139">Service Endpoint Policies</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fb8-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="58fb8-140">-VirtualNetwork</span></span>
<span data-ttu-id="58fb8-141">Указывает объект **VirtualNetwork** , в который нужно добавить конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="58fb8-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="58fb8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58fb8-142">CommonParameters</span></span>
<span data-ttu-id="58fb8-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58fb8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58fb8-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58fb8-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58fb8-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58fb8-145">INPUTS</span></span>

### <span data-ttu-id="58fb8-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="58fb8-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="58fb8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="58fb8-147">System.String</span></span>

### <span data-ttu-id="58fb8-148">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58fb8-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="58fb8-149">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="58fb8-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="58fb8-150">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="58fb8-150">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="58fb8-151">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="58fb8-151">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="58fb8-152">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="58fb8-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="58fb8-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58fb8-153">OUTPUTS</span></span>

### <span data-ttu-id="58fb8-154">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="58fb8-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="58fb8-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="58fb8-155">NOTES</span></span>

## <span data-ttu-id="58fb8-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58fb8-156">RELATED LINKS</span></span>

[<span data-ttu-id="58fb8-157">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58fb8-157">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="58fb8-158">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58fb8-158">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="58fb8-159">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58fb8-159">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="58fb8-160">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="58fb8-160">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


