---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 37202e0e852f0171ce48c2c3d61d13151b05148c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560880"
---
# <span data-ttu-id="57bfd-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57bfd-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="57bfd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="57bfd-103">Создание конфигурации подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="57bfd-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57bfd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57bfd-104">SYNTAX</span></span>

### <span data-ttu-id="57bfd-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57bfd-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57bfd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="57bfd-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57bfd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57bfd-107">DESCRIPTION</span></span>
<span data-ttu-id="57bfd-108">Командлет **New-AzureRmVirtualNetworkSubnetConfig** создает конфигурацию подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="57bfd-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="57bfd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57bfd-109">EXAMPLES</span></span>

### <span data-ttu-id="57bfd-110">1. Создайте виртуальную сеть с двумя подсетями и группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="57bfd-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="57bfd-111">В этом примере создается две новые конфигурации подсети с помощью командлета New-AzureRmVirtualSubnetConfig, а затем они используются для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="57bfd-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="57bfd-112">Шаблон New-AzureRmVirtualSubnetConfig только создает представление подсети в памяти.</span><span class="sxs-lookup"><span data-stu-id="57bfd-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="57bfd-113">В этом примере frontendSubnet имеет CIDR 10.0.1.0/24 и ссылается на сетевую группу безопасности, разрешающую доступ к RDP.</span><span class="sxs-lookup"><span data-stu-id="57bfd-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="57bfd-114">BackendSubnet имеет CIDR 10.0.2.0/24 и ссылается на одну и ту же группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="57bfd-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="57bfd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57bfd-115">PARAMETERS</span></span>

### <span data-ttu-id="57bfd-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57bfd-116">-AddressPrefix</span></span>
<span data-ttu-id="57bfd-117">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="57bfd-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="57bfd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57bfd-118">-DefaultProfile</span></span>
<span data-ttu-id="57bfd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57bfd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57bfd-120">-Делегирование</span><span class="sxs-lookup"><span data-stu-id="57bfd-120">-Delegation</span></span>
<span data-ttu-id="57bfd-121">Список служб, у которых есть разрешение на выполнение операций в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="57bfd-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="57bfd-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="57bfd-122">-Name</span></span>
<span data-ttu-id="57bfd-123">Указывает имя конфигурации подсети, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="57bfd-123">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="57bfd-124">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57bfd-124">-NetworkSecurityGroup</span></span>
<span data-ttu-id="57bfd-125">Указывает объект NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="57bfd-125">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="57bfd-126">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="57bfd-126">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="57bfd-127">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="57bfd-127">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="57bfd-128">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="57bfd-128">-RouteTable</span></span>
<span data-ttu-id="57bfd-129">Указывает таблицу маршрутов, связанную с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="57bfd-129">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="57bfd-130">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="57bfd-130">-RouteTableId</span></span>
<span data-ttu-id="57bfd-131">Указывает идентификатор таблицы маршрутов, связанной с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="57bfd-131">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="57bfd-132">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="57bfd-132">-ServiceEndpoint</span></span>
<span data-ttu-id="57bfd-133">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="57bfd-133">Service Endpoint Value</span></span>

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

### <span data-ttu-id="57bfd-134">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57bfd-134">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="57bfd-135">Политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="57bfd-135">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="57bfd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57bfd-136">CommonParameters</span></span>
<span data-ttu-id="57bfd-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57bfd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57bfd-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57bfd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57bfd-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57bfd-139">INPUTS</span></span>

### <span data-ttu-id="57bfd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="57bfd-140">System.String</span></span>

### <span data-ttu-id="57bfd-141">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57bfd-141">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="57bfd-142">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="57bfd-142">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="57bfd-143">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="57bfd-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="57bfd-144">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="57bfd-144">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="57bfd-145">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="57bfd-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="57bfd-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57bfd-146">OUTPUTS</span></span>

### <span data-ttu-id="57bfd-147">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="57bfd-147">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="57bfd-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="57bfd-148">NOTES</span></span>

## <span data-ttu-id="57bfd-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57bfd-149">RELATED LINKS</span></span>

[<span data-ttu-id="57bfd-150">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57bfd-150">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="57bfd-151">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57bfd-151">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="57bfd-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57bfd-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="57bfd-153">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57bfd-153">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


