---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 62fed5537cc22ee21679cbe1b8d126d9d30efb71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518782"
---
# <span data-ttu-id="e9fdf-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="e9fdf-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="e9fdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="e9fdf-103">Список одноранговых платформ BGP виртуального сетевого шлюза Azure</span><span class="sxs-lookup"><span data-stu-id="e9fdf-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="e9fdf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9fdf-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9fdf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9fdf-105">DESCRIPTION</span></span>
<span data-ttu-id="e9fdf-106">Эта команда является одноранговой службой BGP, для настройки одноранговой связи с виртуальным сетевым шлюзом Azure.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="e9fdf-107">Также предоставляется состояние каждого из них.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="e9fdf-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9fdf-108">EXAMPLES</span></span>

### <span data-ttu-id="e9fdf-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e9fdf-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="e9fdf-110">Извлекает одноранговые платформы BGP для виртуального сетевого шлюза Azure "Имя шлюза" в группе ресурсов resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="e9fdf-111">В этом примере показан один подключенный одноранг BGP с IP-адресом 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="e9fdf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9fdf-112">PARAMETERS</span></span>

### <span data-ttu-id="e9fdf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9fdf-113">-AsJob</span></span>
<span data-ttu-id="e9fdf-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e9fdf-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fdf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9fdf-115">-DefaultProfile</span></span>
<span data-ttu-id="e9fdf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9fdf-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="e9fdf-117">-Peer</span></span>
<span data-ttu-id="e9fdf-118">IP-адрес одноранговой сети, для получения состояния</span><span class="sxs-lookup"><span data-stu-id="e9fdf-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="e9fdf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9fdf-119">-ResourceGroupName</span></span>
<span data-ttu-id="e9fdf-120">Имя группы ресурсов виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="e9fdf-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="e9fdf-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e9fdf-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e9fdf-122">Имя виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="e9fdf-122">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fdf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9fdf-123">CommonParameters</span></span>
<span data-ttu-id="e9fdf-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9fdf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9fdf-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9fdf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9fdf-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9fdf-126">INPUTS</span></span>

### <span data-ttu-id="e9fdf-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e9fdf-127">System.String</span></span>

## <span data-ttu-id="e9fdf-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9fdf-128">OUTPUTS</span></span>

### <span data-ttu-id="e9fdf-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="e9fdf-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="e9fdf-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9fdf-130">NOTES</span></span>

## <span data-ttu-id="e9fdf-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9fdf-131">RELATED LINKS</span></span>
