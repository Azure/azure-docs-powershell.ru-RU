---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 836973c4b1d95445d905bb41f489c48136e12f6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730257"
---
# <span data-ttu-id="e49f4-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e49f4-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="e49f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e49f4-102">SYNOPSIS</span></span>
<span data-ttu-id="e49f4-103">Создание конфигурации подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e49f4-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="e49f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e49f4-104">SYNTAX</span></span>

### <span data-ttu-id="e49f4-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e49f4-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e49f4-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e49f4-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e49f4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e49f4-107">DESCRIPTION</span></span>
<span data-ttu-id="e49f4-108">Командлет **New-AzVirtualNetworkSubnetConfig** создает конфигурацию подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e49f4-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="e49f4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e49f4-109">EXAMPLES</span></span>

### <span data-ttu-id="e49f4-110">1. Создайте виртуальную сеть с двумя подсетями и группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="e49f4-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="e49f4-111">В этом примере создается две новые конфигурации подсети с помощью командлета New-AzVirtualSubnetConfig, а затем они используются для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e49f4-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="e49f4-112">Шаблон New-AzVirtualSubnetConfig только создает представление подсети в памяти.</span><span class="sxs-lookup"><span data-stu-id="e49f4-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="e49f4-113">В этом примере frontendSubnet имеет CIDR 10.0.1.0/24 и ссылается на сетевую группу безопасности, разрешающую доступ к RDP.</span><span class="sxs-lookup"><span data-stu-id="e49f4-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="e49f4-114">BackendSubnet имеет CIDR 10.0.2.0/24 и ссылается на одну и ту же группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="e49f4-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="e49f4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e49f4-115">PARAMETERS</span></span>

### <span data-ttu-id="e49f4-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e49f4-116">-AddressPrefix</span></span>
<span data-ttu-id="e49f4-117">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="e49f4-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="e49f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49f4-118">-DefaultProfile</span></span>
<span data-ttu-id="e49f4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e49f4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e49f4-120">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="e49f4-120">-Delegation</span></span>
<span data-ttu-id="e49f4-121">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="e49f4-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="e49f4-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e49f4-122">-Name</span></span>
<span data-ttu-id="e49f4-123">Указывает имя конфигурации подсети, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="e49f4-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="e49f4-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e49f4-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e49f4-125">Указывает объект NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="e49f4-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="e49f4-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e49f4-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e49f4-127">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="e49f4-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="e49f4-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e49f4-128">-RouteTable</span></span>
<span data-ttu-id="e49f4-129">Указывает таблицу маршрутов, связанную с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="e49f4-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e49f4-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="e49f4-130">-RouteTableId</span></span>
<span data-ttu-id="e49f4-131">Указывает идентификатор таблицы маршрутов, связанной с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="e49f4-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="e49f4-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e49f4-132">-ServiceEndpoint</span></span>
<span data-ttu-id="e49f4-133">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="e49f4-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="e49f4-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e49f4-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e49f4-135">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="e49f4-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="e49f4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49f4-136">CommonParameters</span></span>
<span data-ttu-id="e49f4-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e49f4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49f4-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e49f4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49f4-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e49f4-139">INPUTS</span></span>

### <span data-ttu-id="e49f4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e49f4-140">System.String</span></span>

### <span data-ttu-id="e49f4-141">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e49f4-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="e49f4-142">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="e49f4-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="e49f4-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="e49f4-143">System.String[]</span></span>

### <span data-ttu-id="e49f4-144">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="e49f4-144">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="e49f4-145">Microsoft.Azure.Commands.Network.Models.PSDelegation []</span><span class="sxs-lookup"><span data-stu-id="e49f4-145">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="e49f4-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e49f4-146">OUTPUTS</span></span>

### <span data-ttu-id="e49f4-147">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e49f4-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="e49f4-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="e49f4-148">NOTES</span></span>

## <span data-ttu-id="e49f4-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e49f4-149">RELATED LINKS</span></span>

[<span data-ttu-id="e49f4-150">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e49f4-150">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e49f4-151">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e49f4-151">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e49f4-152">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e49f4-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e49f4-153">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e49f4-153">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
