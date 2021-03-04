---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 7b17b124b7d4e0dc89ee7e61469b26401002db9f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962744"
---
# <span data-ttu-id="f059e-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="f059e-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="f059e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f059e-102">SYNOPSIS</span></span>
<span data-ttu-id="f059e-103">Одноранговая служба VirtualRouter в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f059e-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="f059e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f059e-104">SYNTAX</span></span>

### <span data-ttu-id="f059e-105">VirtualRouterPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f059e-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f059e-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f059e-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f059e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f059e-107">DESCRIPTION</span></span>
<span data-ttu-id="f059e-108">**Cmdlet Get-AzVirtualRouterPeer** получает одноранг в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f059e-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="f059e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f059e-109">EXAMPLES</span></span>

### <span data-ttu-id="f059e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f059e-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="f059e-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f059e-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="f059e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f059e-112">PARAMETERS</span></span>

### <span data-ttu-id="f059e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f059e-113">-DefaultProfile</span></span>
<span data-ttu-id="f059e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f059e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f059e-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="f059e-115">-PeerName</span></span>
<span data-ttu-id="f059e-116">Имя виртуального одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="f059e-116">The name of the virtual router peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f059e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f059e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f059e-118">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="f059e-118">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f059e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f059e-119">-ResourceId</span></span>
<span data-ttu-id="f059e-120">ResourceId виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="f059e-120">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f059e-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="f059e-121">-VirtualRouterName</span></span>
<span data-ttu-id="f059e-122">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="f059e-122">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f059e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f059e-123">CommonParameters</span></span>
<span data-ttu-id="f059e-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f059e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f059e-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f059e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f059e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f059e-126">INPUTS</span></span>

### <span data-ttu-id="f059e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="f059e-127">System.String</span></span>

## <span data-ttu-id="f059e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f059e-128">OUTPUTS</span></span>

### <span data-ttu-id="f059e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="f059e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="f059e-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f059e-130">NOTES</span></span>

## <span data-ttu-id="f059e-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f059e-131">RELATED LINKS</span></span>
