---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 13a81733ac748d2593df967268021f10d60de50b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964291"
---
# <span data-ttu-id="aa711-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="aa711-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="aa711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa711-102">SYNOPSIS</span></span>
<span data-ttu-id="aa711-103">Список маршрутов, объявленных виртуальным сетевым шлюзом Azure</span><span class="sxs-lookup"><span data-stu-id="aa711-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="aa711-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa711-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa711-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa711-105">DESCRIPTION</span></span>
<span data-ttu-id="aa711-106">С учетом IP-адреса одноранговой платформы BGP маршруты объявляются для этого пирера с помощью указанного виртуального сетевого шлюза Azure.</span><span class="sxs-lookup"><span data-stu-id="aa711-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="aa711-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa711-107">EXAMPLES</span></span>

### <span data-ttu-id="aa711-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa711-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="aa711-109">Для шлюза Azure "Имя шлюза" в группе ресурсов resourceGroupName извлекает список маршрутов, объявляемого для пира BGP с IP-адресом 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="aa711-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="aa711-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aa711-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="aa711-111">Для шлюза Azure с именем gatewayName в resourceGroupName группы ресурсов извлекает маршруты, объявленные в первом пире BGP в списке одноранговых платформ BGP шлюза.</span><span class="sxs-lookup"><span data-stu-id="aa711-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="aa711-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa711-112">PARAMETERS</span></span>

### <span data-ttu-id="aa711-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa711-113">-AsJob</span></span>
<span data-ttu-id="aa711-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aa711-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa711-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa711-115">-DefaultProfile</span></span>
<span data-ttu-id="aa711-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa711-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa711-117">-Одноранговая</span><span class="sxs-lookup"><span data-stu-id="aa711-117">-Peer</span></span>
<span data-ttu-id="aa711-118">IP-адрес одноранговой оценки BGP.</span><span class="sxs-lookup"><span data-stu-id="aa711-118">BGP peer's IP address.</span></span> <span data-ttu-id="aa711-119">Это должен быть IP-адрес в адресном пространстве, доступном в виртуальной сети Azure, в который развертывается шлюз.</span><span class="sxs-lookup"><span data-stu-id="aa711-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="aa711-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa711-120">-ResourceGroupName</span></span>
<span data-ttu-id="aa711-121">Имя группы ресурсов виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="aa711-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="aa711-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="aa711-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="aa711-123">Имя виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="aa711-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="aa711-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa711-124">CommonParameters</span></span>
<span data-ttu-id="aa711-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa711-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa711-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa711-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa711-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa711-127">INPUTS</span></span>

### <span data-ttu-id="aa711-128">System.String</span><span class="sxs-lookup"><span data-stu-id="aa711-128">System.String</span></span>

## <span data-ttu-id="aa711-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa711-129">OUTPUTS</span></span>

### <span data-ttu-id="aa711-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="aa711-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="aa711-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa711-131">NOTES</span></span>
<span data-ttu-id="aa711-132">Эта команда применима только к виртуальным сетевым шлюзам Azure с поддержкой BGP-подключений.</span><span class="sxs-lookup"><span data-stu-id="aa711-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="aa711-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa711-133">RELATED LINKS</span></span>
