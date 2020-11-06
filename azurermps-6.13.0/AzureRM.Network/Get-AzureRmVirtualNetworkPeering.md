---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 4b58561783fac3d0c068ec61821c9669a97e1542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566446"
---
# <span data-ttu-id="310ab-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="310ab-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="310ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="310ab-102">SYNOPSIS</span></span>
<span data-ttu-id="310ab-103">Возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="310ab-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="310ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="310ab-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="310ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="310ab-105">DESCRIPTION</span></span>
<span data-ttu-id="310ab-106">Командлет **Get-AzureRmVirtualNetworkPeering** возвращает пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="310ab-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="310ab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="310ab-107">EXAMPLES</span></span>

### <span data-ttu-id="310ab-108">Пример 1: получение одноранговой сети между двумя виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="310ab-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="310ab-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="310ab-109">PARAMETERS</span></span>

### <span data-ttu-id="310ab-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310ab-110">-DefaultProfile</span></span>
<span data-ttu-id="310ab-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="310ab-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="310ab-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="310ab-112">-Name</span></span>
<span data-ttu-id="310ab-113">Указывает имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="310ab-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="310ab-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310ab-114">-ResourceGroupName</span></span>
<span data-ttu-id="310ab-115">Указывает имя группы ресурсов, к которой относится пиринг виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="310ab-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="310ab-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="310ab-116">-VirtualNetworkName</span></span>
<span data-ttu-id="310ab-117">Указывает имя виртуальной сети, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="310ab-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="310ab-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310ab-118">CommonParameters</span></span>
<span data-ttu-id="310ab-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="310ab-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310ab-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="310ab-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310ab-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="310ab-121">INPUTS</span></span>

### <span data-ttu-id="310ab-122">System. String</span><span class="sxs-lookup"><span data-stu-id="310ab-122">System.String</span></span>

## <span data-ttu-id="310ab-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="310ab-123">OUTPUTS</span></span>

### <span data-ttu-id="310ab-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="310ab-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="310ab-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="310ab-125">NOTES</span></span>

## <span data-ttu-id="310ab-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="310ab-126">RELATED LINKS</span></span>

[<span data-ttu-id="310ab-127">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="310ab-127">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="310ab-128">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="310ab-128">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="310ab-129">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="310ab-129">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


