---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
ms.openlocfilehash: a6a199fcac918bcdee76f5dfdecafa3e82fe7f6d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913306"
---
# <span data-ttu-id="46a86-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="46a86-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="46a86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46a86-102">SYNOPSIS</span></span>
<span data-ttu-id="46a86-103">Список узлов BGP шлюза виртуальной сети Azure</span><span class="sxs-lookup"><span data-stu-id="46a86-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46a86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46a86-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46a86-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46a86-105">DESCRIPTION</span></span>
<span data-ttu-id="46a86-106">Эта команда перечисляет узлы BGP, для шлюза виртуальной сети Azure которого настроено значение Peer.</span><span class="sxs-lookup"><span data-stu-id="46a86-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="46a86-107">Также задано состояние каждого однорангового элемента.</span><span class="sxs-lookup"><span data-stu-id="46a86-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="46a86-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46a86-108">EXAMPLES</span></span>

### <span data-ttu-id="46a86-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46a86-109">Example 1</span></span>
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

<span data-ttu-id="46a86-110">Получение одноранговых узлов BGP для шлюза виртуальной сети Azure с именем gatewayName в группе ресурсов "resourceGroup".</span><span class="sxs-lookup"><span data-stu-id="46a86-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>

<span data-ttu-id="46a86-111">Этот пример выходных данных показывает один подключенный узел BGP с IP-адресом 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="46a86-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="46a86-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46a86-112">PARAMETERS</span></span>

### <span data-ttu-id="46a86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46a86-113">-AsJob</span></span>
<span data-ttu-id="46a86-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="46a86-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a86-115">-DefaultProfile</span></span>
<span data-ttu-id="46a86-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46a86-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a86-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="46a86-117">-Peer</span></span>
<span data-ttu-id="46a86-118">IP-адрес однорангового узла, для которого требуется получить состояние</span><span class="sxs-lookup"><span data-stu-id="46a86-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a86-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a86-119">-ResourceGroupName</span></span>
<span data-ttu-id="46a86-120">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="46a86-120">Virtual network gateway resource group's name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a86-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="46a86-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="46a86-122">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="46a86-122">Virtual network gateway name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46a86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a86-123">CommonParameters</span></span>
<span data-ttu-id="46a86-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46a86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a86-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46a86-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a86-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46a86-126">INPUTS</span></span>

### <span data-ttu-id="46a86-127">System. String</span><span class="sxs-lookup"><span data-stu-id="46a86-127">System.String</span></span>

## <span data-ttu-id="46a86-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46a86-128">OUTPUTS</span></span>

### <span data-ttu-id="46a86-129">Microsoft. Azure. Commands. Network. Models. PSBGPPeerStatus []</span><span class="sxs-lookup"><span data-stu-id="46a86-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus[]</span></span>

## <span data-ttu-id="46a86-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="46a86-130">NOTES</span></span>

## <span data-ttu-id="46a86-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46a86-131">RELATED LINKS</span></span>

