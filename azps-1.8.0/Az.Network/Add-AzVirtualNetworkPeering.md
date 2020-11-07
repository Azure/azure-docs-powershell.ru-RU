---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3e4457945e6dfc003c2031d292556e90a7c245ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730686"
---
# <span data-ttu-id="5dfe5-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5dfe5-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="5dfe5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5dfe5-102">SYNOPSIS</span></span>
<span data-ttu-id="5dfe5-103">Создает одноранговую сеть из двух виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="5dfe5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5dfe5-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dfe5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dfe5-105">DESCRIPTION</span></span>
<span data-ttu-id="5dfe5-106">Командлет **Add-AzVirtualNetworkPeering** создает одноранговую сеть из двух виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="5dfe5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5dfe5-107">EXAMPLES</span></span>

### <span data-ttu-id="5dfe5-108">Пример 1: создание однорангового соединения между двумя виртуальными сетями в одном регионе</span><span class="sxs-lookup"><span data-stu-id="5dfe5-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="5dfe5-109">Обратите внимание, что для одноранговой ссылки необходимо создать одноранговую ссылку из vnet1 в vnet2 и наоборот.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="5dfe5-110">Пример 2: создание однорангового соединения между двумя виртуальными сетями в разных регионах</span><span class="sxs-lookup"><span data-stu-id="5dfe5-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="5dfe5-111">Здесь "myVnet1" в США — это равноправный абонент с "myVnet2" в Канаде Central.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="5dfe5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5dfe5-112">PARAMETERS</span></span>

### <span data-ttu-id="5dfe5-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="5dfe5-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="5dfe5-114">Указывает на то, что этот командлет разрешает переадресованный трафик из виртуальных машин в удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfe5-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="5dfe5-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="5dfe5-116">Флаг, разрешающий gatewayLinks использовать в удаленной виртуальной сети для ссылки на эту виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="5dfe5-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfe5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5dfe5-117">-AsJob</span></span>
<span data-ttu-id="5dfe5-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5dfe5-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfe5-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5dfe5-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="5dfe5-120">Указывает на то, что этот командлет блокирует виртуальные машины в связанном пространстве виртуальной сети для доступа ко всем виртуальным машинам в локальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfe5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dfe5-121">-DefaultProfile</span></span>
<span data-ttu-id="5dfe5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dfe5-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5dfe5-123">-Name</span></span>
<span data-ttu-id="5dfe5-124">Указывает имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="5dfe5-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5dfe5-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="5dfe5-126">Указывает идентификатор удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfe5-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="5dfe5-127">-UseRemoteGateways</span></span>
<span data-ttu-id="5dfe5-128">Указывает на то, что этот командлет разрешает удаленные шлюзы в этой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfe5-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5dfe5-129">-VirtualNetwork</span></span>
<span data-ttu-id="5dfe5-130">Указывает родительскую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="5dfe5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dfe5-131">CommonParameters</span></span>
<span data-ttu-id="5dfe5-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5dfe5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dfe5-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dfe5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dfe5-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5dfe5-134">INPUTS</span></span>

### <span data-ttu-id="5dfe5-135">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5dfe5-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="5dfe5-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5dfe5-136">System.String</span></span>

## <span data-ttu-id="5dfe5-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dfe5-137">OUTPUTS</span></span>

### <span data-ttu-id="5dfe5-138">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5dfe5-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="5dfe5-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5dfe5-139">NOTES</span></span>

## <span data-ttu-id="5dfe5-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dfe5-140">RELATED LINKS</span></span>

[<span data-ttu-id="5dfe5-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5dfe5-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="5dfe5-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5dfe5-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="5dfe5-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5dfe5-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="5dfe5-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5dfe5-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
