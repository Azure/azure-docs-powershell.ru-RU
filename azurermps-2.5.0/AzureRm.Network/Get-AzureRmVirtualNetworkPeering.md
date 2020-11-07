---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: b5e3cf083f003a643639635c61ca8e3f13e16eaf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913816"
---
# <span data-ttu-id="ca9c9-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ca9c9-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="ca9c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9c9-103">Возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ca9c9-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca9c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca9c9-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca9c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9c9-106">Командлет **Get-AzureRmVirtualNetworkPeering** возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ca9c9-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="ca9c9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca9c9-107">EXAMPLES</span></span>

### <span data-ttu-id="ca9c9-108">Пример 1: получение одноранговой сети между двумя виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="ca9c9-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="ca9c9-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca9c9-109">PARAMETERS</span></span>

### <span data-ttu-id="ca9c9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9c9-110">-DefaultProfile</span></span>
<span data-ttu-id="ca9c9-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca9c9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca9c9-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca9c9-112">-Name</span></span>
<span data-ttu-id="ca9c9-113">Указывает имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ca9c9-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9c9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9c9-114">-ResourceGroupName</span></span>
<span data-ttu-id="ca9c9-115">Указывает имя группы ресурсов, к которой относится пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ca9c9-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9c9-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ca9c9-116">-VirtualNetworkName</span></span>
<span data-ttu-id="ca9c9-117">Указывает имя виртуальной сети, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ca9c9-117">Specifies the virtual network name that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9c9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9c9-118">CommonParameters</span></span>
<span data-ttu-id="ca9c9-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca9c9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9c9-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9c9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9c9-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca9c9-121">INPUTS</span></span>

## <span data-ttu-id="ca9c9-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca9c9-122">OUTPUTS</span></span>

### <span data-ttu-id="ca9c9-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ca9c9-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="ca9c9-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca9c9-124">NOTES</span></span>

## <span data-ttu-id="ca9c9-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca9c9-125">RELATED LINKS</span></span>

[<span data-ttu-id="ca9c9-126">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ca9c9-126">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="ca9c9-127">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ca9c9-127">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="ca9c9-128">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ca9c9-128">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


