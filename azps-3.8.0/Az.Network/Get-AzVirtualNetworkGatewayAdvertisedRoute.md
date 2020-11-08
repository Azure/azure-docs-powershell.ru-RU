---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073271"
---
# <span data-ttu-id="f8339-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="f8339-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="f8339-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8339-102">SYNOPSIS</span></span>
<span data-ttu-id="f8339-103">Выводит маршруты, объявляемые шлюзом виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="f8339-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="f8339-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8339-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8339-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8339-105">DESCRIPTION</span></span>
<span data-ttu-id="f8339-106">Выдавая IP-адрес узла BGP, перечислите маршруты, объявляемые этим одноранговым узлом, с помощью указанного шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="f8339-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="f8339-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8339-107">EXAMPLES</span></span>

### <span data-ttu-id="f8339-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8339-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="f8339-109">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName извлекает список маршрутов, объявляемых на узел BGP с помощью IP-10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="f8339-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="f8339-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f8339-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="f8339-111">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName извлекает маршруты, объявляемые первым одноранговым узлом BGP в списке узлов BGP на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="f8339-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="f8339-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8339-112">PARAMETERS</span></span>

### <span data-ttu-id="f8339-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8339-113">-AsJob</span></span>
<span data-ttu-id="f8339-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f8339-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8339-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8339-115">-DefaultProfile</span></span>
<span data-ttu-id="f8339-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8339-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8339-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="f8339-117">-Peer</span></span>
<span data-ttu-id="f8339-118">IP-адрес узла BGP.</span><span class="sxs-lookup"><span data-stu-id="f8339-118">BGP peer's IP address.</span></span> <span data-ttu-id="f8339-119">Это должен быть IP-адрес в пространстве адресов, доступном в виртуальной сети Azure, в которой развернут шлюз.</span><span class="sxs-lookup"><span data-stu-id="f8339-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="f8339-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8339-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8339-121">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f8339-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="f8339-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f8339-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f8339-123">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f8339-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="f8339-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8339-124">CommonParameters</span></span>
<span data-ttu-id="f8339-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8339-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8339-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8339-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8339-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8339-127">INPUTS</span></span>

### <span data-ttu-id="f8339-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f8339-128">System.String</span></span>

## <span data-ttu-id="f8339-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8339-129">OUTPUTS</span></span>

### <span data-ttu-id="f8339-130">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="f8339-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="f8339-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8339-131">NOTES</span></span>
<span data-ttu-id="f8339-132">Эта команда применима только к шлюзам виртуальных сетей Azure, для которых включены подключения BGP.</span><span class="sxs-lookup"><span data-stu-id="f8339-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="f8339-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8339-133">RELATED LINKS</span></span>
