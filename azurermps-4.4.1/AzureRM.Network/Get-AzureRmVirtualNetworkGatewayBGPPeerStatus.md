---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 42960533c33cc2d5f8f4ee809cdd7a25c483c75d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565601"
---
# <span data-ttu-id="bb9d2-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="bb9d2-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="bb9d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="bb9d2-103">Список узлов BGP шлюза виртуальной сети Azure</span><span class="sxs-lookup"><span data-stu-id="bb9d2-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb9d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb9d2-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb9d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb9d2-105">DESCRIPTION</span></span>
<span data-ttu-id="bb9d2-106">Эта команда перечисляет узлы BGP, для шлюза виртуальной сети Azure которого настроено значение Peer.</span><span class="sxs-lookup"><span data-stu-id="bb9d2-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="bb9d2-107">Также задано состояние каждого однорангового элемента.</span><span class="sxs-lookup"><span data-stu-id="bb9d2-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="bb9d2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb9d2-108">EXAMPLES</span></span>

### <span data-ttu-id="bb9d2-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bb9d2-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="bb9d2-110">Получение одноранговых узлов BGP для шлюза виртуальной сети Azure с именем gatewayName в группе ресурсов "resourceGroup".</span><span class="sxs-lookup"><span data-stu-id="bb9d2-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="bb9d2-111">Этот пример выходных данных показывает один подключенный узел BGP с IP-адресом 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="bb9d2-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="bb9d2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb9d2-112">PARAMETERS</span></span>

### <span data-ttu-id="bb9d2-113">-Peer</span><span class="sxs-lookup"><span data-stu-id="bb9d2-113">-Peer</span></span>
<span data-ttu-id="bb9d2-114">IP-адрес однорангового узла, для которого требуется получить состояние</span><span class="sxs-lookup"><span data-stu-id="bb9d2-114">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="bb9d2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb9d2-115">-ResourceGroupName</span></span>
<span data-ttu-id="bb9d2-116">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="bb9d2-116">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="bb9d2-117">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bb9d2-117">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bb9d2-118">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="bb9d2-118">Virtual network gateway name</span></span>

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

### <span data-ttu-id="bb9d2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb9d2-119">-DefaultProfile</span></span>
<span data-ttu-id="bb9d2-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb9d2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb9d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb9d2-121">CommonParameters</span></span>
<span data-ttu-id="bb9d2-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb9d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb9d2-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb9d2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb9d2-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb9d2-124">INPUTS</span></span>

### <span data-ttu-id="bb9d2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="bb9d2-125">System.String</span></span>

## <span data-ttu-id="bb9d2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb9d2-126">OUTPUTS</span></span>

### <span data-ttu-id="bb9d2-127">Microsoft. Azure. Commands. Network. Models. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="bb9d2-127">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="bb9d2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb9d2-128">NOTES</span></span>

## <span data-ttu-id="bb9d2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb9d2-129">RELATED LINKS</span></span>

