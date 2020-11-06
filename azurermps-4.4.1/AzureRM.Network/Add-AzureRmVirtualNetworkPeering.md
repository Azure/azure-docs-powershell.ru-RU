---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 7a26e563c8416f31178855acb2d97f318001f8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567577"
---
# <span data-ttu-id="34c4a-101">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="34c4a-101">Add-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="34c4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="34c4a-103">Создает одноранговую сеть из двух виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="34c4a-103">Creates a peering between two virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34c4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34c4a-104">SYNTAX</span></span>

```
Add-AzureRmVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34c4a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="34c4a-106">Командлет **Add-AzureRmVirtualNetworkPeering** создает одноранговую сеть из двух виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="34c4a-106">The **Add-AzureRmVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="34c4a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34c4a-107">EXAMPLES</span></span>

### <span data-ttu-id="34c4a-108">Пример 1: создание однорангового соединения между двумя виртуальными сетями в одном регионе</span><span class="sxs-lookup"><span data-stu-id="34c4a-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'
$location='eastus'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location $location

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location $location

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location $location

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="34c4a-109">Обратите внимание, что для одноранговой ссылки необходимо создать одноранговую ссылку из vnet1 в vnet2 и наоборот.</span><span class="sxs-lookup"><span data-stu-id="34c4a-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="34c4a-110">Пример 2: создание однорангового соединения между двумя виртуальными сетями в разных регионах</span><span class="sxs-lookup"><span data-stu-id="34c4a-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
```
# Variables for common values used throughout the script.
$rgName='myResourceGroup'

# Create a resource group.
New-AzureRmResourceGroup -Name $rgName  -Location westcentralus

# Create virtual network 1.
$vnet1 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet1' -AddressPrefix '10.0.0.0/16' -Location westcentralus

# Create virtual network 2.
$vnet2 = New-AzureRmVirtualNetwork -ResourceGroupName $rgName -Name 'myVnet2' -AddressPrefix '10.1.0.0/16' -Location candacentral

# Peer VNet1 to VNet2.
Add-AzureRmVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzureRmVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="34c4a-111">Здесь "myVnet1" в США — это равноправный абонент с "myVnet2" в Канаде Central.</span><span class="sxs-lookup"><span data-stu-id="34c4a-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="34c4a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34c4a-112">PARAMETERS</span></span>

### <span data-ttu-id="34c4a-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="34c4a-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="34c4a-114">Указывает на то, что этот командлет разрешает переадресованный трафик из виртуальных машин в удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="34c4a-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

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

### <span data-ttu-id="34c4a-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="34c4a-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="34c4a-116">Флаг, разрешающий gatewayLinks использовать в удаленной виртуальной сети для ссылки на эту виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="34c4a-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c4a-117">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="34c4a-117">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="34c4a-118">Указывает на то, что этот командлет блокирует виртуальные машины в связанном пространстве виртуальной сети для доступа ко всем виртуальным машинам в локальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="34c4a-118">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

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

### <span data-ttu-id="34c4a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34c4a-119">-Name</span></span>
<span data-ttu-id="34c4a-120">Указывает имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="34c4a-120">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="34c4a-121">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="34c4a-121">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="34c4a-122">Указывает идентификатор удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="34c4a-122">Specifies the ID of the remote virtual network.</span></span>

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

### <span data-ttu-id="34c4a-123">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="34c4a-123">-UseRemoteGateways</span></span>
<span data-ttu-id="34c4a-124">Указывает на то, что этот командлет разрешает удаленные шлюзы в этой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="34c4a-124">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

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

### <span data-ttu-id="34c4a-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34c4a-125">-VirtualNetwork</span></span>
<span data-ttu-id="34c4a-126">Указывает родительскую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="34c4a-126">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="34c4a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c4a-127">-DefaultProfile</span></span>
<span data-ttu-id="34c4a-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34c4a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34c4a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c4a-129">CommonParameters</span></span>
<span data-ttu-id="34c4a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34c4a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c4a-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c4a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c4a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34c4a-132">INPUTS</span></span>

### <span data-ttu-id="34c4a-133">Подстрок</span><span class="sxs-lookup"><span data-stu-id="34c4a-133">String</span></span>
<span data-ttu-id="34c4a-134">Параметр "RemoteVirtualNetworkId" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="34c4a-134">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="34c4a-135">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34c4a-135">PSVirtualNetwork</span></span>
<span data-ttu-id="34c4a-136">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="34c4a-136">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="34c4a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34c4a-137">OUTPUTS</span></span>

### <span data-ttu-id="34c4a-138">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="34c4a-138">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="34c4a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="34c4a-139">NOTES</span></span>

## <span data-ttu-id="34c4a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34c4a-140">RELATED LINKS</span></span>

[<span data-ttu-id="34c4a-141">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="34c4a-141">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="34c4a-142">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="34c4a-142">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="34c4a-143">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="34c4a-143">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="34c4a-144">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="34c4a-144">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


