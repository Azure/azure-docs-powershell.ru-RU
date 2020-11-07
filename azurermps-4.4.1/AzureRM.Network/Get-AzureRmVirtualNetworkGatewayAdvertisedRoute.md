---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: a9b8cd9f13de8c1c4e3a7f20a0ffe410211f8973
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732762"
---
# <span data-ttu-id="8f262-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="8f262-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="8f262-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f262-102">SYNOPSIS</span></span>
<span data-ttu-id="8f262-103">Выводит маршруты, объявляемые шлюзом виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="8f262-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f262-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f262-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f262-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f262-105">DESCRIPTION</span></span>
<span data-ttu-id="8f262-106">Выдавая IP-адрес узла BGP, перечислите маршруты, объявляемые этим одноранговым узлом, с помощью указанного шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="8f262-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="8f262-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f262-107">EXAMPLES</span></span>

### <span data-ttu-id="8f262-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f262-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="8f262-109">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName retrives список маршрутов, объявляемых на узел BGP с IP-адресом 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="8f262-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="8f262-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8f262-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="8f262-111">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName извлекает маршруты, объявляемые первым одноранговым узлом BGP в списке узлов BGP на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="8f262-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="8f262-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f262-112">PARAMETERS</span></span>

### <span data-ttu-id="8f262-113">-Peer</span><span class="sxs-lookup"><span data-stu-id="8f262-113">-Peer</span></span>
<span data-ttu-id="8f262-114">IP-адрес узла BGP.</span><span class="sxs-lookup"><span data-stu-id="8f262-114">BGP peer's IP address.</span></span> <span data-ttu-id="8f262-115">Это должен быть IP-адрес в пространстве адресов, доступном в виртуальной сети Azure, в которой развернут шлюз.</span><span class="sxs-lookup"><span data-stu-id="8f262-115">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="8f262-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f262-116">-ResourceGroupName</span></span>
<span data-ttu-id="8f262-117">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8f262-117">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="8f262-118">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8f262-118">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8f262-119">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8f262-119">Virtual network gateway name</span></span>

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

### <span data-ttu-id="8f262-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f262-120">-DefaultProfile</span></span>
<span data-ttu-id="8f262-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f262-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f262-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f262-122">CommonParameters</span></span>
<span data-ttu-id="8f262-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f262-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f262-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f262-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f262-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f262-125">INPUTS</span></span>

### <span data-ttu-id="8f262-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8f262-126">System.String</span></span>

## <span data-ttu-id="8f262-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f262-127">OUTPUTS</span></span>

### <span data-ttu-id="8f262-128">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="8f262-128">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="8f262-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f262-129">NOTES</span></span>
<span data-ttu-id="8f262-130">Эта команда применима только к шлюзам виртуальных сетей Azure, для которых включены подключения BGP.</span><span class="sxs-lookup"><span data-stu-id="8f262-130">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="8f262-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f262-131">RELATED LINKS</span></span>

