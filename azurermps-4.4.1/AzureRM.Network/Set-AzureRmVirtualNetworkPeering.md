---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: aaaca86109331543d8e1b292e0e04ea7b5cbb5f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559612"
---
# <span data-ttu-id="ec614-101">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ec614-101">Set-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="ec614-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec614-102">SYNOPSIS</span></span>
<span data-ttu-id="ec614-103">Настройка пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ec614-103">Configures a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec614-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec614-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec614-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec614-105">DESCRIPTION</span></span>
<span data-ttu-id="ec614-106">Командлет **Set-AzureRmVirtualNetworkPeering** настраивает пиринг виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="ec614-106">The **Set-AzureRmVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="ec614-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec614-107">EXAMPLES</span></span>

### <span data-ttu-id="ec614-108">Пример 1: изменение конфигурации переадресованного трафика для пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ec614-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="ec614-109">Пример 2: изменение доступа к виртуальной сети для пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ec614-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="ec614-110">Пример 3: изменение конфигурации свойств транзита шлюза для пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ec614-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="ec614-111">Пример 4: использование удаленных шлюзов в одноранговом соединении виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ec614-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzureRmVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzureRmVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="ec614-112">Изменив это свойство на $True, можно использовать шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ec614-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="ec614-113">Тем не менее, одноранговая сеть должна иметь настроенный шлюз и **AllowGatewayTransit** должен иметь значение $true.</span><span class="sxs-lookup"><span data-stu-id="ec614-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="ec614-114">Это свойство нельзя использовать, если шлюз уже настроен.</span><span class="sxs-lookup"><span data-stu-id="ec614-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="ec614-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec614-115">PARAMETERS</span></span>

### <span data-ttu-id="ec614-116">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ec614-116">-VirtualNetworkPeering</span></span>
<span data-ttu-id="ec614-117">Указывает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ec614-117">Specifies the virtual network peering.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec614-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec614-118">-DefaultProfile</span></span>
<span data-ttu-id="ec614-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec614-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec614-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec614-120">CommonParameters</span></span>
<span data-ttu-id="ec614-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec614-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec614-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec614-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec614-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec614-123">INPUTS</span></span>

### <span data-ttu-id="ec614-124">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ec614-124">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="ec614-125">Параметр "VirtualNetworkPeering" принимает значение типа "PSVirtualNetworkPeering" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ec614-125">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="ec614-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec614-126">OUTPUTS</span></span>

### <span data-ttu-id="ec614-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ec614-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="ec614-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec614-128">NOTES</span></span>

## <span data-ttu-id="ec614-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec614-129">RELATED LINKS</span></span>

[<span data-ttu-id="ec614-130">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ec614-130">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="ec614-131">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ec614-131">Get-AzureRmVirtualNetworkPeering</span></span>](./Get-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="ec614-132">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ec614-132">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)


