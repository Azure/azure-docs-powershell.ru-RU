---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409919"
---
# <span data-ttu-id="a6634-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a6634-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="a6634-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6634-102">SYNOPSIS</span></span>
<span data-ttu-id="a6634-103">Возвращает виртуальный сетевой пиринг.</span><span class="sxs-lookup"><span data-stu-id="a6634-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="a6634-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6634-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6634-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6634-105">DESCRIPTION</span></span>
<span data-ttu-id="a6634-106">Командлет **Get-AzVirtualNetworkPeering** получает виртуальный пиринг сети.</span><span class="sxs-lookup"><span data-stu-id="a6634-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="a6634-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6634-107">EXAMPLES</span></span>

### <span data-ttu-id="a6634-108">Пример 1. Просмотр пиринга между двумя виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="a6634-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="a6634-109">Пример 2. Получить все пиринги в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="a6634-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="a6634-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6634-110">PARAMETERS</span></span>

### <span data-ttu-id="a6634-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6634-111">-DefaultProfile</span></span>
<span data-ttu-id="a6634-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6634-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6634-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a6634-113">-Name</span></span>
<span data-ttu-id="a6634-114">Указывает имя виртуального сетевого пиринга.</span><span class="sxs-lookup"><span data-stu-id="a6634-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a6634-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6634-115">-ResourceGroupName</span></span>
<span data-ttu-id="a6634-116">Имя группы ресурсов, к которой принадлежит виртуальный сетевой пиринг.</span><span class="sxs-lookup"><span data-stu-id="a6634-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6634-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a6634-117">-VirtualNetworkName</span></span>
<span data-ttu-id="a6634-118">Указывает имя виртуальной сети, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6634-118">Specifies the virtual network name that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6634-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6634-119">CommonParameters</span></span>
<span data-ttu-id="a6634-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6634-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6634-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6634-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6634-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6634-122">INPUTS</span></span>

### <span data-ttu-id="a6634-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a6634-123">System.String</span></span>

## <span data-ttu-id="a6634-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6634-124">OUTPUTS</span></span>

### <span data-ttu-id="a6634-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a6634-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="a6634-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6634-126">NOTES</span></span>

## <span data-ttu-id="a6634-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6634-127">RELATED LINKS</span></span>

[<span data-ttu-id="a6634-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a6634-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="a6634-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a6634-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="a6634-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a6634-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)