---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 16f73c81c13740037131e47d03945d475db12ee9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909593"
---
# <span data-ttu-id="57353-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57353-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="57353-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57353-102">SYNOPSIS</span></span>
<span data-ttu-id="57353-103">Создание конфигурации подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="57353-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="57353-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57353-104">SYNTAX</span></span>

### <span data-ttu-id="57353-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57353-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57353-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="57353-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57353-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57353-107">DESCRIPTION</span></span>
<span data-ttu-id="57353-108">Командлет **New-AzVirtualNetworkSubnetConfig** создает конфигурацию подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="57353-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="57353-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57353-109">EXAMPLES</span></span>

### <span data-ttu-id="57353-110">1. Создайте виртуальную сеть с двумя подсетями и группой безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="57353-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

<span data-ttu-id="57353-111">В этом примере создается две новые конфигурации подсети с помощью командлета New-AzVirtualSubnetConfig, а затем они используются для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="57353-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="57353-112">Шаблон New-AzVirtualSubnetConfig только создает представление подсети в памяти.</span><span class="sxs-lookup"><span data-stu-id="57353-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="57353-113">В этом примере frontendSubnet имеет CIDR 10.0.1.0/24 и ссылается на сетевую группу безопасности, разрешающую доступ к RDP.</span><span class="sxs-lookup"><span data-stu-id="57353-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="57353-114">BackendSubnet имеет CIDR 10.0.2.0/24 и ссылается на одну и ту же группу безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="57353-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="57353-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57353-115">PARAMETERS</span></span>

### <span data-ttu-id="57353-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="57353-116">-AddressPrefix</span></span>
<span data-ttu-id="57353-117">Указывает диапазон IP-адресов для конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="57353-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="57353-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57353-118">-DefaultProfile</span></span>
<span data-ttu-id="57353-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57353-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57353-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="57353-120">-Name</span></span>
<span data-ttu-id="57353-121">Указывает имя конфигурации подсети, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="57353-121">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="57353-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="57353-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="57353-123">Указывает объект NetworkSecurityGroup.</span><span class="sxs-lookup"><span data-stu-id="57353-123">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="57353-124">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="57353-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="57353-125">Указывает идентификатор сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="57353-125">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="57353-126">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="57353-126">-RouteTable</span></span>
<span data-ttu-id="57353-127">Указывает таблицу маршрутов, связанную с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="57353-127">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="57353-128">-RouteTableId</span><span class="sxs-lookup"><span data-stu-id="57353-128">-RouteTableId</span></span>
<span data-ttu-id="57353-129">Указывает идентификатор таблицы маршрутов, связанной с конфигурацией подсети.</span><span class="sxs-lookup"><span data-stu-id="57353-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="57353-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="57353-130">-ServiceEndpoint</span></span>
<span data-ttu-id="57353-131">Значение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="57353-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="57353-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57353-132">CommonParameters</span></span>
<span data-ttu-id="57353-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57353-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57353-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57353-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57353-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57353-135">INPUTS</span></span>

## <span data-ttu-id="57353-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57353-136">OUTPUTS</span></span>

### <span data-ttu-id="57353-137">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="57353-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="57353-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="57353-138">NOTES</span></span>

## <span data-ttu-id="57353-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57353-139">RELATED LINKS</span></span>

[<span data-ttu-id="57353-140">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57353-140">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="57353-141">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57353-141">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="57353-142">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57353-142">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="57353-143">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="57353-143">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


