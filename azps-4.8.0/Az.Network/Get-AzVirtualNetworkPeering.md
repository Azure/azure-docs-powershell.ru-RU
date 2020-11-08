---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236068"
---
# <span data-ttu-id="e215a-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e215a-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="e215a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e215a-102">SYNOPSIS</span></span>
<span data-ttu-id="e215a-103">Возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e215a-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="e215a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e215a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e215a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e215a-105">DESCRIPTION</span></span>
<span data-ttu-id="e215a-106">Командлет **Get-AzVirtualNetworkPeering** возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e215a-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="e215a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e215a-107">EXAMPLES</span></span>

### <span data-ttu-id="e215a-108">Пример 1: получение одноранговой сети между двумя виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="e215a-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="e215a-109">Пример 2: получение всех одноранговых элементов в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e215a-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e215a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e215a-110">PARAMETERS</span></span>

### <span data-ttu-id="e215a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e215a-111">-DefaultProfile</span></span>
<span data-ttu-id="e215a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e215a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e215a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e215a-113">-Name</span></span>
<span data-ttu-id="e215a-114">Указывает имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e215a-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="e215a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e215a-115">-ResourceGroupName</span></span>
<span data-ttu-id="e215a-116">Указывает имя группы ресурсов, к которой относится пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e215a-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="e215a-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e215a-117">-VirtualNetworkName</span></span>
<span data-ttu-id="e215a-118">Указывает имя виртуальной сети, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e215a-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e215a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e215a-119">CommonParameters</span></span>
<span data-ttu-id="e215a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e215a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e215a-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e215a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e215a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e215a-122">INPUTS</span></span>

### <span data-ttu-id="e215a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e215a-123">System.String</span></span>

## <span data-ttu-id="e215a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e215a-124">OUTPUTS</span></span>

### <span data-ttu-id="e215a-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e215a-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="e215a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e215a-126">NOTES</span></span>

## <span data-ttu-id="e215a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e215a-127">RELATED LINKS</span></span>

[<span data-ttu-id="e215a-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e215a-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e215a-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e215a-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e215a-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e215a-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
