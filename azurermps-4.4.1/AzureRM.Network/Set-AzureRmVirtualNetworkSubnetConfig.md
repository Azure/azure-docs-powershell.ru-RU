---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 179bfced7b73113899f525940114abb342e61f8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734258"
---
# <span data-ttu-id="a7293-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a7293-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a7293-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7293-102">SYNOPSIS</span></span>
<span data-ttu-id="a7293-103">Настраивает состояние цели для конфигурации подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a7293-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7293-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7293-104">SYNTAX</span></span>

### <span data-ttu-id="a7293-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7293-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7293-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7293-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7293-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7293-107">DESCRIPTION</span></span>
<span data-ttu-id="a7293-108">Командлет **Set-AzureRmVirtualNetworkSubnetConfig** настраивает состояние цели для конфигурации подсети в виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="a7293-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="a7293-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7293-109">EXAMPLES</span></span>

### <span data-ttu-id="a7293-110">1: изменение префикса адреса подсети</span><span class="sxs-lookup"><span data-stu-id="a7293-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="a7293-111">В этом примере создается виртуальная сеть с одной подсетью.</span><span class="sxs-lookup"><span data-stu-id="a7293-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="a7293-112">Затем вызывает Set-AzureRmVirtualNetworkSubnetConfig, чтобы изменить AddressPrefix подсети.</span><span class="sxs-lookup"><span data-stu-id="a7293-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="a7293-113">Это влияет только на представление виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="a7293-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="a7293-114">Set-AzureRmVirtualNetwork вызывается, чтобы изменить виртуальную сеть в Azure.</span><span class="sxs-lookup"><span data-stu-id="a7293-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="a7293-115">2. Добавьте сетевую группу безопасности в подсеть.</span><span class="sxs-lookup"><span data-stu-id="a7293-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="a7293-116">В этом примере создается группа ресурсов с одной виртуальной сетью, которая содержит только одну подсеть.</span><span class="sxs-lookup"><span data-stu-id="a7293-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="a7293-117">Затем он создает сетевую группу безопасности с правилом разрешения для трафика RDP.</span><span class="sxs-lookup"><span data-stu-id="a7293-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="a7293-118">Командлет Set-AzureRmVirtualNetworkSubnetConfig используется для изменения представления в памяти подсети с интерфейсом, чтобы она указывала на только что созданную сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="a7293-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="a7293-119">Затем вызывается командлет Set-AzureRmVirtualNetwork, чтобы записать измененное состояние обратно в службу.</span><span class="sxs-lookup"><span data-stu-id="a7293-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="a7293-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7293-120">PARAMETERS</span></span>

### <span data-ttu-id="a7293-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a7293-121">-AddressPrefix</span></span>
<span data-ttu-id="a7293-122">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="a7293-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="a7293-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7293-123">-Name</span></span>
<span data-ttu-id="a7293-124">Указывает имя конфигурации подсети, которая настраивается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a7293-124">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="a7293-125">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a7293-125">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a7293-126">Указывает объект **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="a7293-126">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="a7293-127">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a7293-127">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="a7293-128">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="a7293-128">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="a7293-129">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="a7293-129">-RouteTable</span></span>
<span data-ttu-id="a7293-130">Указывает объект таблицы маршрутов, связанный с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="a7293-130">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="a7293-131">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="a7293-131">-RouteTableId</span></span>
<span data-ttu-id="a7293-132">Указывает идентификатор объекта таблицы маршрутов, связанного с группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="a7293-132">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="a7293-133">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7293-133">-ServiceEndpoint</span></span>
<span data-ttu-id="a7293-134">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="a7293-134">Service Endpoint Value</span></span>

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

### <span data-ttu-id="a7293-135">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a7293-135">-VirtualNetwork</span></span>
<span data-ttu-id="a7293-136">Указывает объект **VirtualNetwork** , который содержит конфигурацию подсети.</span><span class="sxs-lookup"><span data-stu-id="a7293-136">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="a7293-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7293-137">-DefaultProfile</span></span>
<span data-ttu-id="a7293-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7293-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7293-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7293-139">CommonParameters</span></span>
<span data-ttu-id="a7293-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7293-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7293-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7293-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7293-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7293-142">INPUTS</span></span>

### <span data-ttu-id="a7293-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a7293-143">PSVirtualNetwork</span></span>
<span data-ttu-id="a7293-144">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a7293-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="a7293-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7293-145">OUTPUTS</span></span>

### <span data-ttu-id="a7293-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a7293-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a7293-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7293-147">NOTES</span></span>

## <span data-ttu-id="a7293-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7293-148">RELATED LINKS</span></span>

[<span data-ttu-id="a7293-149">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a7293-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a7293-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a7293-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a7293-151">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a7293-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a7293-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a7293-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


