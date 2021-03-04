---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 06DAD751-3A43-4EF6-94C5-AA7AC1A67FC8
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkPeering.md
ms.openlocfilehash: 1f24dd8cff058b49c9661da1d2f5f2ae927e1a0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952035"
---
# <span data-ttu-id="40a18-101">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="40a18-101">Set-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="40a18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40a18-102">SYNOPSIS</span></span>
<span data-ttu-id="40a18-103">Настраивает виртуальный пиринг сети.</span><span class="sxs-lookup"><span data-stu-id="40a18-103">Configures a virtual network peering.</span></span>

## <span data-ttu-id="40a18-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="40a18-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkPeering -VirtualNetworkPeering <PSVirtualNetworkPeering> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40a18-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40a18-105">DESCRIPTION</span></span>
<span data-ttu-id="40a18-106">Командлет **Set-AzVirtualNetworkPeering** настраивает виртуальный пиринг сети.</span><span class="sxs-lookup"><span data-stu-id="40a18-106">The **Set-AzVirtualNetworkPeering** cmdlet configures a virtual network peering.</span></span>

## <span data-ttu-id="40a18-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="40a18-107">EXAMPLES</span></span>

### <span data-ttu-id="40a18-108">Пример 1. Изменение конфигурации перенаправимого трафика виртуального сетевого пиринга</span><span class="sxs-lookup"><span data-stu-id="40a18-108">Example 1: Change forwarded traffic configuration of a virtual network peering</span></span>
```
# Get the virtual network peering you want to update information for
Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup" -Name "myVnet1ToMyVnet2"

# Change value of AllowForwardedTraffic property
$myVnet1ToMyVnet2.AllowForwardedTraffic = $True

# Update the peering with changes made
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1ToMyVnet2
```

### <span data-ttu-id="40a18-109">Пример 2. Изменение виртуального сетевого доступа к виртуальному пирингу сети</span><span class="sxs-lookup"><span data-stu-id="40a18-109">Example 2: Change virtual network access of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowVirtualNetworkAccess property
$myVnet1TomyVnet2.AllowVirtualNetworkAccess = $False

# Update virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="40a18-110">Пример 3. Изменение конфигурации свойств общественного транспорта шлюза для виртуального сетевого пиринга</span><span class="sxs-lookup"><span data-stu-id="40a18-110">Example 3: Change gateway transit property configuration of a virtual network peering</span></span>
```
# Get the virtual network peering
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "myResourceGroup" -Name "myVnet1TomyVnet2"

# Change AllowGatewayTransit property
$myVnet1TomyVnet2.AllowGatewayTransit = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

### <span data-ttu-id="40a18-111">Пример 4. Использование удаленных шлюзов в виртуальном сетевом пиринге</span><span class="sxs-lookup"><span data-stu-id="40a18-111">Example 4: Use remote gateways in virtual network peering</span></span>
```
# Get the virtual network peering 
$myVnet1TomyVnet2 = Get-AzVirtualNetworkPeering -VirtualNetworkName "myVnet1" -ResourceGroupName "ResourceGroup001" -Name "myVnet1TomyVnet2"

# Change the UseRemoteGateways property
$myVnet1TomyVnet2.UseRemoteGateways = $True

# Update the virtual network peering
Set-AzVirtualNetworkPeering -VirtualNetworkPeering $myVnet1TomyVnet2
```

<span data-ttu-id="40a18-112">Изменив это свойство на $True, можно использовать шлюз VNet вашего одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="40a18-112">By changing this property to $True, your peer's VNet gateway can be used.</span></span>
<span data-ttu-id="40a18-113">Однако для одноранговой сети VNet должен быть настроен шлюз, а значение **allowGatewayTransit** должно $True.</span><span class="sxs-lookup"><span data-stu-id="40a18-113">However, the peer VNet must have a gateway configured and **AllowGatewayTransit** must have a value of $True.</span></span>
<span data-ttu-id="40a18-114">Это свойство нельзя использовать, если шлюз уже настроен.</span><span class="sxs-lookup"><span data-stu-id="40a18-114">This property cannot be used if a gateway has already been configured.</span></span>

## <span data-ttu-id="40a18-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40a18-115">PARAMETERS</span></span>

### <span data-ttu-id="40a18-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40a18-116">-AsJob</span></span>
<span data-ttu-id="40a18-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="40a18-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40a18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a18-118">-DefaultProfile</span></span>
<span data-ttu-id="40a18-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40a18-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40a18-120">-VirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="40a18-120">-VirtualNetworkPeering</span></span>
<span data-ttu-id="40a18-121">Определяет виртуальный сетевой пиринг.</span><span class="sxs-lookup"><span data-stu-id="40a18-121">Specifies the virtual network peering.</span></span>

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

### <span data-ttu-id="40a18-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a18-122">CommonParameters</span></span>
<span data-ttu-id="40a18-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40a18-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a18-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40a18-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a18-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40a18-125">INPUTS</span></span>

### <span data-ttu-id="40a18-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="40a18-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="40a18-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40a18-127">OUTPUTS</span></span>

### <span data-ttu-id="40a18-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="40a18-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="40a18-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="40a18-129">NOTES</span></span>

## <span data-ttu-id="40a18-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40a18-130">RELATED LINKS</span></span>

[<span data-ttu-id="40a18-131">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="40a18-131">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="40a18-132">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="40a18-132">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="40a18-133">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="40a18-133">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)
