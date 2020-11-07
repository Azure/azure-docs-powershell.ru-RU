---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 75725505e7c5239f1b5dc8f05d4cdfe3cf2b4903
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909829"
---
# <span data-ttu-id="524c4-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="524c4-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="524c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="524c4-102">SYNOPSIS</span></span>
<span data-ttu-id="524c4-103">Возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="524c4-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="524c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="524c4-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="524c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="524c4-105">DESCRIPTION</span></span>
<span data-ttu-id="524c4-106">Командлет **Get-AzVirtualNetworkPeering** возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="524c4-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="524c4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="524c4-107">EXAMPLES</span></span>

### <span data-ttu-id="524c4-108">Пример 1: получение одноранговой сети между двумя виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="524c4-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="524c4-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="524c4-109">PARAMETERS</span></span>

### <span data-ttu-id="524c4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="524c4-110">-DefaultProfile</span></span>
<span data-ttu-id="524c4-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="524c4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="524c4-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="524c4-112">-Name</span></span>
<span data-ttu-id="524c4-113">Указывает имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="524c4-113">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="524c4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="524c4-114">-ResourceGroupName</span></span>
<span data-ttu-id="524c4-115">Указывает имя группы ресурсов, к которой относится пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="524c4-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="524c4-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="524c4-116">-VirtualNetworkName</span></span>
<span data-ttu-id="524c4-117">Указывает имя виртуальной сети, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="524c4-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="524c4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="524c4-118">CommonParameters</span></span>
<span data-ttu-id="524c4-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="524c4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="524c4-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="524c4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="524c4-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="524c4-121">INPUTS</span></span>

## <span data-ttu-id="524c4-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="524c4-122">OUTPUTS</span></span>

### <span data-ttu-id="524c4-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="524c4-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="524c4-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="524c4-124">NOTES</span></span>

## <span data-ttu-id="524c4-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="524c4-125">RELATED LINKS</span></span>

[<span data-ttu-id="524c4-126">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="524c4-126">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="524c4-127">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="524c4-127">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="524c4-128">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="524c4-128">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)


