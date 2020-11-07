---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: 9f1f4f916ea0756ebf034c12e1e9f92f3cd3c865
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915241"
---
# <span data-ttu-id="886bd-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="886bd-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="886bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="886bd-102">SYNOPSIS</span></span>
<span data-ttu-id="886bd-103">Добавляет конфигурацию подсети в виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="886bd-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="886bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="886bd-104">SYNTAX</span></span>

### <span data-ttu-id="886bd-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="886bd-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="886bd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="886bd-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="886bd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="886bd-107">DESCRIPTION</span></span>
<span data-ttu-id="886bd-108">Командлет **Add-AzureRmVirtualNetworkSubnetConfig** добавляет конфигурацию подсети в существующую виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="886bd-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="886bd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="886bd-109">EXAMPLES</span></span>

### <span data-ttu-id="886bd-110">1: Добавление подсети в существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="886bd-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="886bd-111">В этом примере сначала создается группа ресурсов в качестве контейнера ресурсов, которые необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="886bd-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="886bd-112">Затем он создает конфигурацию подсети и использует ее для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="886bd-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="886bd-113">Затем Add-AzureRmVirtualNetworkSubnetConfig используется для добавления подсети в представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="886bd-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="886bd-114">Команда Set-AzureRmVirtualNetwork обновляет существующую виртуальную сеть, используя новую подсеть.</span><span class="sxs-lookup"><span data-stu-id="886bd-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="886bd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="886bd-115">PARAMETERS</span></span>

### <span data-ttu-id="886bd-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="886bd-116">-AddressPrefix</span></span>
<span data-ttu-id="886bd-117">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="886bd-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="886bd-118">-DefaultProfile</span></span>
<span data-ttu-id="886bd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="886bd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886bd-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="886bd-120">-Name</span></span>
<span data-ttu-id="886bd-121">Указывает имя конфигурации подсети, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="886bd-121">Specifies the name of the subnet configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="886bd-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="886bd-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="886bd-123">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="886bd-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="886bd-124">Этот командлет добавляет конфигурацию подсети виртуальной сети к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="886bd-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="886bd-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="886bd-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="886bd-126">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="886bd-126">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="886bd-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="886bd-127">-RouteTable</span></span>
```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="886bd-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="886bd-128">-RouteTableId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="886bd-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="886bd-129">-ServiceEndpoint</span></span>
<span data-ttu-id="886bd-130">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="886bd-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="886bd-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="886bd-131">-VirtualNetwork</span></span>
<span data-ttu-id="886bd-132">Указывает объект **VirtualNetwork** , в который нужно добавить конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="886bd-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="886bd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="886bd-133">CommonParameters</span></span>
<span data-ttu-id="886bd-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="886bd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="886bd-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="886bd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="886bd-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="886bd-136">INPUTS</span></span>

### <span data-ttu-id="886bd-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="886bd-137">PSVirtualNetwork</span></span>
<span data-ttu-id="886bd-138">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="886bd-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="886bd-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="886bd-139">OUTPUTS</span></span>

### <span data-ttu-id="886bd-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="886bd-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="886bd-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="886bd-141">NOTES</span></span>

## <span data-ttu-id="886bd-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="886bd-142">RELATED LINKS</span></span>

[<span data-ttu-id="886bd-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="886bd-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="886bd-144">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="886bd-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="886bd-145">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="886bd-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="886bd-146">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="886bd-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


