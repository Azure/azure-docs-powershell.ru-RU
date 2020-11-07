---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 01116d3a2ad2636776fe29a0e36e34568624f2c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910120"
---
# <span data-ttu-id="3e82c-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3e82c-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="3e82c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e82c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e82c-103">Добавляет конфигурацию подсети в виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="3e82c-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="3e82c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e82c-104">SYNTAX</span></span>

### <span data-ttu-id="3e82c-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e82c-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e82c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e82c-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e82c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e82c-107">DESCRIPTION</span></span>
<span data-ttu-id="3e82c-108">Командлет **Add-AzVirtualNetworkSubnetConfig** добавляет конфигурацию подсети в существующую виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="3e82c-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="3e82c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e82c-109">EXAMPLES</span></span>

### <span data-ttu-id="3e82c-110">1: Добавление подсети в существующую виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="3e82c-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="3e82c-111">В этом примере сначала создается группа ресурсов в качестве контейнера ресурсов, которые необходимо создать.</span><span class="sxs-lookup"><span data-stu-id="3e82c-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="3e82c-112">Затем он создает конфигурацию подсети и использует ее для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3e82c-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="3e82c-113">Затем Add-AzVirtualNetworkSubnetConfig используется для добавления подсети в представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="3e82c-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="3e82c-114">Команда Set-AzVirtualNetwork обновляет существующую виртуальную сеть, используя новую подсеть.</span><span class="sxs-lookup"><span data-stu-id="3e82c-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="3e82c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e82c-115">PARAMETERS</span></span>

### <span data-ttu-id="3e82c-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3e82c-116">-AddressPrefix</span></span>
<span data-ttu-id="3e82c-117">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="3e82c-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="3e82c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e82c-118">-DefaultProfile</span></span>
<span data-ttu-id="3e82c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e82c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e82c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e82c-120">-Name</span></span>
<span data-ttu-id="3e82c-121">Указывает имя конфигурации подсети, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="3e82c-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="3e82c-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3e82c-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3e82c-123">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="3e82c-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="3e82c-124">Этот командлет добавляет конфигурацию подсети виртуальной сети к объекту, указанному этим параметром.</span><span class="sxs-lookup"><span data-stu-id="3e82c-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e82c-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3e82c-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="3e82c-126">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="3e82c-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="3e82c-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="3e82c-127">-RouteTable</span></span>
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

### <span data-ttu-id="3e82c-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="3e82c-128">-RouteTableId</span></span>
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

### <span data-ttu-id="3e82c-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3e82c-129">-ServiceEndpoint</span></span>
<span data-ttu-id="3e82c-130">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="3e82c-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="3e82c-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3e82c-131">-VirtualNetwork</span></span>
<span data-ttu-id="3e82c-132">Указывает объект **VirtualNetwork** , в который нужно добавить конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="3e82c-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="3e82c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e82c-133">CommonParameters</span></span>
<span data-ttu-id="3e82c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e82c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e82c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e82c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e82c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e82c-136">INPUTS</span></span>

### <span data-ttu-id="3e82c-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3e82c-137">PSVirtualNetwork</span></span>
<span data-ttu-id="3e82c-138">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3e82c-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="3e82c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e82c-139">OUTPUTS</span></span>

### <span data-ttu-id="3e82c-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3e82c-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="3e82c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e82c-141">NOTES</span></span>

## <span data-ttu-id="3e82c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e82c-142">RELATED LINKS</span></span>

[<span data-ttu-id="3e82c-143">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3e82c-143">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3e82c-144">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3e82c-144">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3e82c-145">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3e82c-145">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="3e82c-146">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="3e82c-146">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


