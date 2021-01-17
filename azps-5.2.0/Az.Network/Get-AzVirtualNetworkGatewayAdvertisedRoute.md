---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408919"
---
# <span data-ttu-id="520d3-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="520d3-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="520d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="520d3-102">SYNOPSIS</span></span>
<span data-ttu-id="520d3-103">Список маршрутов, объявленных виртуальным сетевым шлюзом Azure</span><span class="sxs-lookup"><span data-stu-id="520d3-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="520d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="520d3-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="520d3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="520d3-105">DESCRIPTION</span></span>
<span data-ttu-id="520d3-106">С учетом IP-адреса одноранговой платформы BGP маршруты объявляются для этого пирера с помощью указанного виртуального сетевого шлюза Azure.</span><span class="sxs-lookup"><span data-stu-id="520d3-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="520d3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="520d3-107">EXAMPLES</span></span>

### <span data-ttu-id="520d3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="520d3-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="520d3-109">Для шлюза Azure "Имя шлюза" в группе ресурсов resourceGroupName извлекает список маршрутов, объявленных в одноранговом клиенте BGP с IP-адресом 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="520d3-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="520d3-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="520d3-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="520d3-111">Для шлюза Azure с именем gatewayName в resourceGroupName группы ресурсов извлекает маршруты, объявленные в первом пире BGP в списке одноранговых платформ BGP шлюза.</span><span class="sxs-lookup"><span data-stu-id="520d3-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="520d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="520d3-112">PARAMETERS</span></span>

### <span data-ttu-id="520d3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="520d3-113">-AsJob</span></span>
<span data-ttu-id="520d3-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="520d3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="520d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520d3-115">-DefaultProfile</span></span>
<span data-ttu-id="520d3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="520d3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="520d3-117">-Одноранговая</span><span class="sxs-lookup"><span data-stu-id="520d3-117">-Peer</span></span>
<span data-ttu-id="520d3-118">IP-адрес одноранговой оценки BGP.</span><span class="sxs-lookup"><span data-stu-id="520d3-118">BGP peer's IP address.</span></span> <span data-ttu-id="520d3-119">Это должен быть IP-адрес в адресном пространстве, доступном в виртуальной сети Azure, в который развертывается шлюз.</span><span class="sxs-lookup"><span data-stu-id="520d3-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="520d3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="520d3-120">-ResourceGroupName</span></span>
<span data-ttu-id="520d3-121">Имя группы ресурсов виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="520d3-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="520d3-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="520d3-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="520d3-123">Имя виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="520d3-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="520d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520d3-124">CommonParameters</span></span>
<span data-ttu-id="520d3-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="520d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520d3-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="520d3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520d3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="520d3-127">INPUTS</span></span>

### <span data-ttu-id="520d3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="520d3-128">System.String</span></span>

## <span data-ttu-id="520d3-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="520d3-129">OUTPUTS</span></span>

### <span data-ttu-id="520d3-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="520d3-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="520d3-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="520d3-131">NOTES</span></span>
<span data-ttu-id="520d3-132">Эта команда применима только к виртуальным сетевым шлюзам Azure с поддержкой BGP-подключений.</span><span class="sxs-lookup"><span data-stu-id="520d3-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="520d3-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="520d3-133">RELATED LINKS</span></span>
