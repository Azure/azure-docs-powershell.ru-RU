---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13901193-8C68-4969-ADCD-2E82EA714354
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkPeering.md
ms.openlocfilehash: 440c1395c30f396ff1ae2430828cac7aae675734
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910126"
---
# <span data-ttu-id="f99fc-101">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f99fc-101">Add-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="f99fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f99fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f99fc-103">Создает одноранговую сеть из двух виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="f99fc-103">Creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="f99fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f99fc-104">SYNTAX</span></span>

```
Add-AzVirtualNetworkPeering -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -RemoteVirtualNetworkId <String> [-BlockVirtualNetworkAccess] [-AllowForwardedTraffic] [-AllowGatewayTransit]
 [-UseRemoteGateways] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f99fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f99fc-105">DESCRIPTION</span></span>
<span data-ttu-id="f99fc-106">Командлет **Add-AzVirtualNetworkPeering** создает одноранговую сеть из двух виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="f99fc-106">The **Add-AzVirtualNetworkPeering** cmdlet creates a peering between two virtual networks.</span></span>

## <span data-ttu-id="f99fc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f99fc-107">EXAMPLES</span></span>

### <span data-ttu-id="f99fc-108">Пример 1: создание однорангового соединения между двумя виртуальными сетями в одном регионе</span><span class="sxs-lookup"><span data-stu-id="f99fc-108">Example 1: Create a peering between two virtual networks in the same region</span></span>
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
Add-AzVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="f99fc-109">Обратите внимание, что для одноранговой ссылки необходимо создать одноранговую ссылку из vnet1 в vnet2 и наоборот.</span><span class="sxs-lookup"><span data-stu-id="f99fc-109">Note that a peering link must be created from vnet1 to vnet2 and vice versa in order for peering to work.</span></span>

### <span data-ttu-id="f99fc-110">Пример 2: создание однорангового соединения между двумя виртуальными сетями в разных регионах</span><span class="sxs-lookup"><span data-stu-id="f99fc-110">Example 2: Create a peering between two virtual networks in different regions</span></span>
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
Add-AzVirtualNetworkPeering -Name myVnet1ToMyVnet2' -VirtualNetwork $vnet1 -RemoteVirtualNetworkId $vnet2.Id

# Peer VNet2 to VNet1.
Add-AzVirtualNetworkPeering -Name 'myVnet2ToMyVnet1' -VirtualNetwork $vnet2 -RemoteVirtualNetworkId $vnet1.Id
```

<span data-ttu-id="f99fc-111">Здесь "myVnet1" в США — это равноправный абонент с "myVnet2" в Канаде Central.</span><span class="sxs-lookup"><span data-stu-id="f99fc-111">Here 'myVnet1' in US West Central is peered with 'myVnet2' in Canada Central.</span></span>

## <span data-ttu-id="f99fc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f99fc-112">PARAMETERS</span></span>

### <span data-ttu-id="f99fc-113">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="f99fc-113">-AllowForwardedTraffic</span></span>
<span data-ttu-id="f99fc-114">Указывает на то, что этот командлет разрешает переадресованный трафик из виртуальных машин в удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f99fc-114">Indicates that this cmdlet allows the forwarded traffic from the virtual machines in the remote virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99fc-115">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="f99fc-115">-AllowGatewayTransit</span></span>
<span data-ttu-id="f99fc-116">Флаг, разрешающий gatewayLinks использовать в удаленной виртуальной сети для ссылки на эту виртуальную сеть</span><span class="sxs-lookup"><span data-stu-id="f99fc-116">Flag to allow gatewayLinks be used in remote virtual network's link to this virtual network</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: AlloowGatewayTransit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99fc-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f99fc-117">-AsJob</span></span>
<span data-ttu-id="f99fc-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f99fc-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99fc-119">-BlockVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="f99fc-119">-BlockVirtualNetworkAccess</span></span>
<span data-ttu-id="f99fc-120">Указывает на то, что этот командлет блокирует виртуальные машины в связанном пространстве виртуальной сети для доступа ко всем виртуальным машинам в локальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f99fc-120">Indicates that this cmdlet blocks the virtual machines in the linked virtual network space to access all the virtual machines in local virtual network space.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99fc-121">-DefaultProfile</span></span>
<span data-ttu-id="f99fc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f99fc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f99fc-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f99fc-123">-Name</span></span>
<span data-ttu-id="f99fc-124">Указывает имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f99fc-124">Specifies the name of the virtual network peering.</span></span>

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

### <span data-ttu-id="f99fc-125">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="f99fc-125">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="f99fc-126">Указывает идентификатор удаленной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f99fc-126">Specifies the ID of the remote virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f99fc-127">-UseRemoteGateways</span><span class="sxs-lookup"><span data-stu-id="f99fc-127">-UseRemoteGateways</span></span>
<span data-ttu-id="f99fc-128">Указывает на то, что этот командлет разрешает удаленные шлюзы в этой виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f99fc-128">Indicates that this cmdlet allows remote gateways on this virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99fc-129">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f99fc-129">-VirtualNetwork</span></span>
<span data-ttu-id="f99fc-130">Указывает родительскую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="f99fc-130">Specifies the parent virtual network.</span></span>

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

### <span data-ttu-id="f99fc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99fc-131">CommonParameters</span></span>
<span data-ttu-id="f99fc-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f99fc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99fc-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f99fc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99fc-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f99fc-134">INPUTS</span></span>

### <span data-ttu-id="f99fc-135">Подстрок</span><span class="sxs-lookup"><span data-stu-id="f99fc-135">String</span></span>
<span data-ttu-id="f99fc-136">Параметр "RemoteVirtualNetworkId" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f99fc-136">Parameter 'RemoteVirtualNetworkId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="f99fc-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f99fc-137">PSVirtualNetwork</span></span>
<span data-ttu-id="f99fc-138">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f99fc-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="f99fc-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f99fc-139">OUTPUTS</span></span>

### <span data-ttu-id="f99fc-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f99fc-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="f99fc-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f99fc-141">NOTES</span></span>

## <span data-ttu-id="f99fc-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f99fc-142">RELATED LINKS</span></span>

[<span data-ttu-id="f99fc-143">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f99fc-143">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="f99fc-144">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f99fc-144">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="f99fc-145">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f99fc-145">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="f99fc-146">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f99fc-146">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


