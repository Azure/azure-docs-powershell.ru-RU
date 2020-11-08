---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248339"
---
# <span data-ttu-id="9e3d8-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="9e3d8-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="9e3d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e3d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3d8-103">Выводит маршруты, объявляемые шлюзом виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="9e3d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e3d8-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e3d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e3d8-105">DESCRIPTION</span></span>
<span data-ttu-id="9e3d8-106">Выдавая IP-адрес узла BGP, перечислите маршруты, объявляемые этим одноранговым узлом, с помощью указанного шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="9e3d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e3d8-107">EXAMPLES</span></span>

### <span data-ttu-id="9e3d8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e3d8-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="9e3d8-109">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName извлекает список маршрутов, объявляемых на узел BGP с помощью IP-10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="9e3d8-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="9e3d8-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9e3d8-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="9e3d8-111">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName извлекает маршруты, объявляемые первым одноранговым узлом BGP в списке узлов BGP на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="9e3d8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e3d8-112">PARAMETERS</span></span>

### <span data-ttu-id="9e3d8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e3d8-113">-AsJob</span></span>
<span data-ttu-id="9e3d8-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9e3d8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e3d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3d8-115">-DefaultProfile</span></span>
<span data-ttu-id="9e3d8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e3d8-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="9e3d8-117">-Peer</span></span>
<span data-ttu-id="9e3d8-118">IP-адрес узла BGP.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-118">BGP peer's IP address.</span></span> <span data-ttu-id="9e3d8-119">Это должен быть IP-адрес в пространстве адресов, доступном в виртуальной сети Azure, в которой развернут шлюз.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="9e3d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e3d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e3d8-121">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="9e3d8-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="9e3d8-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9e3d8-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9e3d8-123">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="9e3d8-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="9e3d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3d8-124">CommonParameters</span></span>
<span data-ttu-id="9e3d8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3d8-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e3d8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3d8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e3d8-127">INPUTS</span></span>

### <span data-ttu-id="9e3d8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9e3d8-128">System.String</span></span>

## <span data-ttu-id="9e3d8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e3d8-129">OUTPUTS</span></span>

### <span data-ttu-id="9e3d8-130">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="9e3d8-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="9e3d8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e3d8-131">NOTES</span></span>
<span data-ttu-id="9e3d8-132">Эта команда применима только к шлюзам виртуальных сетей Azure, для которых включены подключения BGP.</span><span class="sxs-lookup"><span data-stu-id="9e3d8-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="9e3d8-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e3d8-133">RELATED LINKS</span></span>
