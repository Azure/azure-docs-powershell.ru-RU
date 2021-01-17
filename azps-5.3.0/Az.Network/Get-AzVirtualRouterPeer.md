---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422087"
---
# <span data-ttu-id="6ffff-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="6ffff-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="6ffff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ffff-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffff-103">Одноранговая служба VirtualRouter в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6ffff-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="6ffff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ffff-104">SYNTAX</span></span>

### <span data-ttu-id="6ffff-105">VirtualRouterPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ffff-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ffff-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffff-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ffff-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ffff-107">DESCRIPTION</span></span>
<span data-ttu-id="6ffff-108">**Cmdlet Get-AzVirtualRouterPeer** получает одноранг в Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="6ffff-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="6ffff-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ffff-109">EXAMPLES</span></span>

### <span data-ttu-id="6ffff-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ffff-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="6ffff-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6ffff-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="6ffff-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ffff-112">PARAMETERS</span></span>

### <span data-ttu-id="6ffff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffff-113">-DefaultProfile</span></span>
<span data-ttu-id="6ffff-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ffff-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="6ffff-115">-PeerName</span></span>
<span data-ttu-id="6ffff-116">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="6ffff-116">The name of the virtual router peer.</span></span>

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

### <span data-ttu-id="6ffff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffff-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ffff-118">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="6ffff-118">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="6ffff-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ffff-119">-ResourceId</span></span>
<span data-ttu-id="6ffff-120">ResourceId виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="6ffff-120">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="6ffff-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="6ffff-121">-VirtualRouterName</span></span>
<span data-ttu-id="6ffff-122">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="6ffff-122">The name of the virtual router.</span></span>

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

### <span data-ttu-id="6ffff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffff-123">CommonParameters</span></span>
<span data-ttu-id="6ffff-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffff-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ffff-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffff-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ffff-126">INPUTS</span></span>

### <span data-ttu-id="6ffff-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6ffff-127">System.String</span></span>

## <span data-ttu-id="6ffff-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ffff-128">OUTPUTS</span></span>

### <span data-ttu-id="6ffff-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="6ffff-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="6ffff-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ffff-130">NOTES</span></span>

## <span data-ttu-id="6ffff-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ffff-131">RELATED LINKS</span></span>
