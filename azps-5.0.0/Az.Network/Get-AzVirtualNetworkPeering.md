---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316112"
---
# <span data-ttu-id="cebeb-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cebeb-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="cebeb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cebeb-102">SYNOPSIS</span></span>
<span data-ttu-id="cebeb-103">Возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cebeb-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="cebeb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cebeb-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cebeb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cebeb-105">DESCRIPTION</span></span>
<span data-ttu-id="cebeb-106">Командлет **Get-AzVirtualNetworkPeering** возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cebeb-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="cebeb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cebeb-107">EXAMPLES</span></span>

### <span data-ttu-id="cebeb-108">Пример 1: получение одноранговой сети между двумя виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="cebeb-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="cebeb-109">Пример 2: получение всех одноранговых элементов в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="cebeb-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="cebeb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cebeb-110">PARAMETERS</span></span>

### <span data-ttu-id="cebeb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebeb-111">-DefaultProfile</span></span>
<span data-ttu-id="cebeb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cebeb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cebeb-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cebeb-113">-Name</span></span>
<span data-ttu-id="cebeb-114">Указывает имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cebeb-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="cebeb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cebeb-115">-ResourceGroupName</span></span>
<span data-ttu-id="cebeb-116">Указывает имя группы ресурсов, к которой относится пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cebeb-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="cebeb-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="cebeb-117">-VirtualNetworkName</span></span>
<span data-ttu-id="cebeb-118">Указывает имя виртуальной сети, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cebeb-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cebeb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebeb-119">CommonParameters</span></span>
<span data-ttu-id="cebeb-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cebeb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebeb-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cebeb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebeb-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cebeb-122">INPUTS</span></span>

### <span data-ttu-id="cebeb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cebeb-123">System.String</span></span>

## <span data-ttu-id="cebeb-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cebeb-124">OUTPUTS</span></span>

### <span data-ttu-id="cebeb-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cebeb-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="cebeb-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="cebeb-126">NOTES</span></span>

## <span data-ttu-id="cebeb-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cebeb-127">RELATED LINKS</span></span>

[<span data-ttu-id="cebeb-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cebeb-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="cebeb-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cebeb-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="cebeb-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="cebeb-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
