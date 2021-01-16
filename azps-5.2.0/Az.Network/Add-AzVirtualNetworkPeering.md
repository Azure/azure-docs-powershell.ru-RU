---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: a63f6c2bc57bfc4d1a82861c6b25bd5c8a6e1383
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410583"
---
# <span data-ttu-id="0e90b-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0e90b-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="0e90b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e90b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e90b-103">Создает пиринг между двумя виртуальными сетями.</span><span class="sxs-lookup"><span data-stu-id="0e90b-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="0e90b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0e90b-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork> -RemoteVirtualNetworkId <String>
 [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-UseRemoteGateways] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e90b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e90b-105">DESCRIPTION</span></span>
<span data-ttu-id="0e90b-106">Командлет **Add-AzVirtualNetworkPeering** создает пиринг между двумя виртуальными сетями.</span><span class="sxs-lookup"><span data-stu-id="0e90b-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="0e90b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0e90b-107">EXAMPLES</span></span>

### <span data-ttu-id="0e90b-108">Пример 1. Создание пиринга между двумя виртуальными сетями в одном регионе</span><span class="sxs-lookup"><span data-stu-id="0e90b-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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

<span data-ttu-id="0e90b-109">Обратите внимание на то, что для работы пиринга необходимо создать ссылку пиринга из vnet1 в vnet2 и наоборот.</span><span class="sxs-lookup"><span data-stu-id="0e90b-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="0e90b-110">Пример 2. Создание пиринга между двумя виртуальными сетями в разных регионах</span><span class="sxs-lookup"><span data-stu-id="0e90b-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location canadacentral

# Peer VNet1 to VNet2.
Add-AzVirtualNetworkPeering -Name 'myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="0e90b-111">Здесь myVnet1 в США West Central имеет одноранговую ссылку "myVnet2" в Центре Канады.</span><span class="sxs-lookup"><span data-stu-id="0e90b-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="0e90b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e90b-112">PARAMETERS</span></span>

### <span data-ttu-id="0e90b-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="0e90b-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="0e90b-114">Указывает на то, что этот cmdlet позволяет перенанощать трафик с виртуальных машин в удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0e90b-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="0e90b-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="0e90b-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="0e90b-116">Пометить, чтобы разрешить использовать ссылки шлюза в ссылке удаленной виртуальной сети на эту виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="0e90b-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

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

### <span data-ttu-id="0e90b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e90b-117">-AsJob</span></span>
<span data-ttu-id="0e90b-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0e90b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e90b-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0e90b-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="0e90b-120">Указывает на то, что этот cmdlet блокирует виртуальные машины в связанном виртуальном сетевом пространстве для доступа ко всем виртуальным машинам в локальном виртуальном сетевом пространстве.</span><span class="sxs-lookup"><span data-stu-id="0e90b-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="0e90b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e90b-121">-DefaultProfile</span></span>
<span data-ttu-id="0e90b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e90b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e90b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0e90b-123">-Name</span></span>
<span data-ttu-id="0e90b-124">Указывает имя виртуального сетевого пиринга.</span><span class="sxs-lookup"><span data-stu-id="0e90b-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="0e90b-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0e90b-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="0e90b-126">Определяет ИД удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0e90b-126">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="0e90b-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="0e90b-127">-UseRemoteGateways</span></span>
<span data-ttu-id="0e90b-128">Указывает на то, что этот cmdlet позволяет использовать удаленные шлюзы в этой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0e90b-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="0e90b-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0e90b-129">-VirtualNetwork</span></span>
<span data-ttu-id="0e90b-130">Указывает родительская виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="0e90b-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="0e90b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e90b-131">CommonParameters</span></span>
<span data-ttu-id="0e90b-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e90b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e90b-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e90b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e90b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e90b-134">INPUTS</span></span>

### <span data-ttu-id="0e90b-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0e90b-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="0e90b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0e90b-136">System.String</span></span>

## <span data-ttu-id="0e90b-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e90b-137">OUTPUTS</span></span>

### <span data-ttu-id="0e90b-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0e90b-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="0e90b-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0e90b-139">NOTES</span></span>

## <span data-ttu-id="0e90b-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e90b-140">RELATED LINKS</span></span>

[<span data-ttu-id="0e90b-141">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0e90b-141">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="0e90b-142">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0e90b-142">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0e90b-143">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0e90b-143">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="0e90b-144">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="0e90b-144">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
