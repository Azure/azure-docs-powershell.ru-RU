---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
ms.openlocfilehash: 0097cd022387b3ac2ee8ceb1fa2a831b60c4256d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913307"
---
# <span data-ttu-id="8f022-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="8f022-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="8f022-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f022-102">SYNOPSIS</span></span>
<span data-ttu-id="8f022-103">Выводит маршруты, объявляемые шлюзом виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="8f022-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f022-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f022-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f022-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f022-105">DESCRIPTION</span></span>
<span data-ttu-id="8f022-106">Выдавая IP-адрес узла BGP, перечислите маршруты, объявляемые этим одноранговым узлом, с помощью указанного шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="8f022-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="8f022-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f022-107">EXAMPLES</span></span>

### <span data-ttu-id="8f022-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f022-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="8f022-109">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName retrives список маршрутов, объявляемых на узел BGP с IP-адресом 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="8f022-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="8f022-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8f022-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="8f022-111">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName извлекает маршруты, объявляемые первым одноранговым узлом BGP в списке узлов BGP на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="8f022-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="8f022-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f022-112">PARAMETERS</span></span>

### <span data-ttu-id="8f022-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f022-113">-AsJob</span></span>
<span data-ttu-id="8f022-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8f022-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f022-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f022-115">-DefaultProfile</span></span>
<span data-ttu-id="8f022-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f022-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f022-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="8f022-117">-Peer</span></span>
<span data-ttu-id="8f022-118">IP-адрес узла BGP.</span><span class="sxs-lookup"><span data-stu-id="8f022-118">BGP peer's IP address.</span></span> <span data-ttu-id="8f022-119">Это должен быть IP-адрес в пространстве адресов, доступном в виртуальной сети Azure, в которой развернут шлюз.</span><span class="sxs-lookup"><span data-stu-id="8f022-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="8f022-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f022-120">-ResourceGroupName</span></span>
<span data-ttu-id="8f022-121">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8f022-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="8f022-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8f022-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8f022-123">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8f022-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="8f022-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f022-124">CommonParameters</span></span>
<span data-ttu-id="8f022-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f022-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f022-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f022-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f022-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f022-127">INPUTS</span></span>

### <span data-ttu-id="8f022-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8f022-128">System.String</span></span>

## <span data-ttu-id="8f022-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f022-129">OUTPUTS</span></span>

### <span data-ttu-id="8f022-130">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="8f022-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="8f022-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f022-131">NOTES</span></span>
<span data-ttu-id="8f022-132">Эта команда применима только к шлюзам виртуальных сетей Azure, для которых включены подключения BGP.</span><span class="sxs-lookup"><span data-stu-id="8f022-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="8f022-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f022-133">RELATED LINKS</span></span>

