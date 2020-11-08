---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: cf662dcd74182776131a5b7cfe3df3d86d20c14b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065832"
---
# <span data-ttu-id="c8411-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="c8411-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="c8411-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8411-102">SYNOPSIS</span></span>
<span data-ttu-id="c8411-103">Возвращает VirtualRouter одноранговый элемент в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c8411-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>


## <span data-ttu-id="c8411-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8411-104">SYNTAX</span></span>

### <span data-ttu-id="c8411-105">VirtualRouterPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8411-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8411-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8411-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8411-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8411-107">DESCRIPTION</span></span>
<span data-ttu-id="c8411-108">Командлет **Get-AzVirtualRouterPeer** получает одноранговый элемент в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c8411-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="c8411-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8411-109">EXAMPLES</span></span>

### <span data-ttu-id="c8411-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8411-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -RouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="c8411-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c8411-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="c8411-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8411-112">PARAMETERS</span></span>

### <span data-ttu-id="c8411-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8411-113">-DefaultProfile</span></span>
<span data-ttu-id="c8411-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8411-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8411-115">-Одноранговое</span><span class="sxs-lookup"><span data-stu-id="c8411-115">-PeerName</span></span>
<span data-ttu-id="c8411-116">Имя узла виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="c8411-116">The name of the virtual router peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8411-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8411-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8411-118">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="c8411-118">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8411-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8411-119">-ResourceId</span></span>
<span data-ttu-id="c8411-120">ResourceId виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="c8411-120">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8411-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="c8411-121">-VirtualRouterName</span></span>
<span data-ttu-id="c8411-122">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="c8411-122">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8411-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8411-123">CommonParameters</span></span>
<span data-ttu-id="c8411-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8411-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8411-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8411-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8411-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8411-126">INPUTS</span></span>

### <span data-ttu-id="c8411-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c8411-127">System.String</span></span>

## <span data-ttu-id="c8411-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8411-128">OUTPUTS</span></span>

### <span data-ttu-id="c8411-129">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="c8411-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="c8411-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8411-130">NOTES</span></span>

## <span data-ttu-id="c8411-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8411-131">RELATED LINKS</span></span>
