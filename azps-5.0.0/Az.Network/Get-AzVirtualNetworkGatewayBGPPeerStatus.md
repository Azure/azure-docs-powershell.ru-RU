---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 62fed5537cc22ee21679cbe1b8d126d9d30efb71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248338"
---
# <span data-ttu-id="5dbfa-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="5dbfa-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="5dbfa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5dbfa-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbfa-103">Список узлов BGP шлюза виртуальной сети Azure</span><span class="sxs-lookup"><span data-stu-id="5dbfa-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="5dbfa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5dbfa-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dbfa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dbfa-105">DESCRIPTION</span></span>
<span data-ttu-id="5dbfa-106">Эта команда перечисляет узлы BGP, для шлюза виртуальной сети Azure которого настроено значение Peer.</span><span class="sxs-lookup"><span data-stu-id="5dbfa-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="5dbfa-107">Также задано состояние каждого однорангового элемента.</span><span class="sxs-lookup"><span data-stu-id="5dbfa-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="5dbfa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5dbfa-108">EXAMPLES</span></span>

### <span data-ttu-id="5dbfa-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5dbfa-109">Example 1</span></span>
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

<span data-ttu-id="5dbfa-110">Получение одноранговых узлов BGP для шлюза виртуальной сети Azure с именем gatewayName в группе ресурсов "resourceGroup".</span><span class="sxs-lookup"><span data-stu-id="5dbfa-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="5dbfa-111">Этот пример выходных данных показывает один подключенный узел BGP с IP-адресом 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="5dbfa-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="5dbfa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5dbfa-112">PARAMETERS</span></span>

### <span data-ttu-id="5dbfa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5dbfa-113">-AsJob</span></span>
<span data-ttu-id="5dbfa-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5dbfa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5dbfa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dbfa-115">-DefaultProfile</span></span>
<span data-ttu-id="5dbfa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dbfa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dbfa-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="5dbfa-117">-Peer</span></span>
<span data-ttu-id="5dbfa-118">IP-адрес однорангового узла, для которого требуется получить состояние</span><span class="sxs-lookup"><span data-stu-id="5dbfa-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="5dbfa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dbfa-119">-ResourceGroupName</span></span>
<span data-ttu-id="5dbfa-120">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="5dbfa-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="5dbfa-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5dbfa-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5dbfa-122">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="5dbfa-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="5dbfa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbfa-123">CommonParameters</span></span>
<span data-ttu-id="5dbfa-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5dbfa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbfa-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dbfa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbfa-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5dbfa-126">INPUTS</span></span>

### <span data-ttu-id="5dbfa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5dbfa-127">System.String</span></span>

## <span data-ttu-id="5dbfa-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dbfa-128">OUTPUTS</span></span>

### <span data-ttu-id="5dbfa-129">Microsoft. Azure. Commands. Network. Models. PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="5dbfa-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="5dbfa-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5dbfa-130">NOTES</span></span>

## <span data-ttu-id="5dbfa-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dbfa-131">RELATED LINKS</span></span>
