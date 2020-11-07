---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: e2b4625536124cdb5352c97564cd4c2792dadb96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730467"
---
# <span data-ttu-id="1bdaf-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1bdaf-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="1bdaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1bdaf-102">SYNOPSIS</span></span>
<span data-ttu-id="1bdaf-103">Возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1bdaf-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="1bdaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1bdaf-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bdaf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bdaf-105">DESCRIPTION</span></span>
<span data-ttu-id="1bdaf-106">Командлет **Get-AzVirtualNetworkPeering** возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1bdaf-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="1bdaf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1bdaf-107">EXAMPLES</span></span>

### <span data-ttu-id="1bdaf-108">Пример 1: получение одноранговой сети между двумя виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="1bdaf-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="1bdaf-109">Пример 2: получение всех одноранговых элементов в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="1bdaf-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="1bdaf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1bdaf-110">PARAMETERS</span></span>

### <span data-ttu-id="1bdaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bdaf-111">-DefaultProfile</span></span>
<span data-ttu-id="1bdaf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1bdaf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bdaf-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1bdaf-113">-Name</span></span>
<span data-ttu-id="1bdaf-114">Указывает имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1bdaf-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="1bdaf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bdaf-115">-ResourceGroupName</span></span>
<span data-ttu-id="1bdaf-116">Указывает имя группы ресурсов, к которой относится пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1bdaf-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="1bdaf-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1bdaf-117">-VirtualNetworkName</span></span>
<span data-ttu-id="1bdaf-118">Указывает имя виртуальной сети, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1bdaf-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1bdaf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bdaf-119">CommonParameters</span></span>
<span data-ttu-id="1bdaf-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1bdaf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bdaf-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bdaf-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bdaf-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1bdaf-122">INPUTS</span></span>

### <span data-ttu-id="1bdaf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1bdaf-123">System.String</span></span>

## <span data-ttu-id="1bdaf-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bdaf-124">OUTPUTS</span></span>

### <span data-ttu-id="1bdaf-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1bdaf-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="1bdaf-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="1bdaf-126">NOTES</span></span>

## <span data-ttu-id="1bdaf-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bdaf-127">RELATED LINKS</span></span>

[<span data-ttu-id="1bdaf-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1bdaf-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="1bdaf-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1bdaf-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="1bdaf-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="1bdaf-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
