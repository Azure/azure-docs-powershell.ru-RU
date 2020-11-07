---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 9ad6d0ef43913bc7b182a37a9bca4b9cccae1918
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910998"
---
# <span data-ttu-id="e612a-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e612a-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="e612a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e612a-102">SYNOPSIS</span></span>
<span data-ttu-id="e612a-103">Настройка пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e612a-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="e612a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e612a-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e612a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e612a-105">DESCRIPTION</span></span>
<span data-ttu-id="e612a-106">Командлет **Set-AzVirtualNetworkPeering** настраивает пиринг виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="e612a-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="e612a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e612a-107">EXAMPLES</span></span>

### <span data-ttu-id="e612a-108">Пример 1: изменение конфигурации переадресованного трафика для пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e612a-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="e612a-109">Пример 2: изменение доступа к виртуальной сети для пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e612a-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="e612a-110">Пример 3: изменение конфигурации свойств транзита шлюза для пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e612a-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="e612a-111">Пример 4: использование удаленных шлюзов в одноранговом соединении виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e612a-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $LinkToVNet2
```

<span data-ttu-id="e612a-112">Изменив это свойство на $True, можно использовать шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e612a-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="e612a-113">Тем не менее, одноранговая сеть должна иметь настроенный шлюз и **AllowGatewayTransit** должен иметь значение $true.</span><span class="sxs-lookup"><span data-stu-id="e612a-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>

<span data-ttu-id="e612a-114">Это свойство нельзя использовать, если шлюз уже настроен.</span><span class="sxs-lookup"><span data-stu-id="e612a-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="e612a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e612a-115">PARAMETERS</span></span>

### <span data-ttu-id="e612a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e612a-116">-AsJob</span></span>
<span data-ttu-id="e612a-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e612a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e612a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e612a-118">-DefaultProfile</span></span>
<span data-ttu-id="e612a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e612a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e612a-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e612a-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="e612a-121">Указывает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e612a-121">Specifies the virtual network peering.</span></span>

```yaml
Type: PSVirtualNetworkPeering
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e612a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e612a-122">CommonParameters</span></span>
<span data-ttu-id="e612a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e612a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e612a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e612a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e612a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e612a-125">INPUTS</span></span>

### <span data-ttu-id="e612a-126">PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e612a-126">PSVirtualNetworkPeering</span></span>
<span data-ttu-id="e612a-127">Параметр "VirtualNetworkPeering" принимает значение типа "PSVirtualNetworkPeering" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e612a-127">Parameter 'VirtualNetworkPeering' accepts value of type 'PSVirtualNetworkPeering' from the pipeline</span></span>

## <span data-ttu-id="e612a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e612a-128">OUTPUTS</span></span>

### <span data-ttu-id="e612a-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e612a-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="e612a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e612a-130">NOTES</span></span>

## <span data-ttu-id="e612a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e612a-131">RELATED LINKS</span></span>

[<span data-ttu-id="e612a-132">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e612a-132">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e612a-133">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e612a-133">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e612a-134">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e612a-134">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)


