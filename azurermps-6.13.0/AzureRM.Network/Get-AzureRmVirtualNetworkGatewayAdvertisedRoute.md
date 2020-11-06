---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: 288a2382470682c8c7b55f7342d5a0f193446019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570200"
---
# <span data-ttu-id="97b7c-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="97b7c-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="97b7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="97b7c-103">Выводит маршруты, объявляемые шлюзом виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="97b7c-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97b7c-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97b7c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="97b7c-106">Выдавая IP-адрес узла BGP, перечислите маршруты, объявляемые этим одноранговым узлом, с помощью указанного шлюза виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="97b7c-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="97b7c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97b7c-107">EXAMPLES</span></span>

### <span data-ttu-id="97b7c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="97b7c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="97b7c-109">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName retrives список маршрутов, объявляемых на узел BGP с IP-адресом 10.0.0.254</span><span class="sxs-lookup"><span data-stu-id="97b7c-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="97b7c-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="97b7c-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="97b7c-111">Для шлюза Azure с именем gatewayName в группе ресурсов resourceGroupName извлекает маршруты, объявляемые первым одноранговым узлом BGP в списке узлов BGP на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="97b7c-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="97b7c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97b7c-112">PARAMETERS</span></span>

### <span data-ttu-id="97b7c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97b7c-113">-AsJob</span></span>
<span data-ttu-id="97b7c-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="97b7c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97b7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b7c-115">-DefaultProfile</span></span>
<span data-ttu-id="97b7c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97b7c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97b7c-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="97b7c-117">-Peer</span></span>
<span data-ttu-id="97b7c-118">IP-адрес узла BGP.</span><span class="sxs-lookup"><span data-stu-id="97b7c-118">BGP peer's IP address.</span></span> <span data-ttu-id="97b7c-119">Это должен быть IP-адрес в пространстве адресов, доступном в виртуальной сети Azure, в которой развернут шлюз.</span><span class="sxs-lookup"><span data-stu-id="97b7c-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="97b7c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b7c-120">-ResourceGroupName</span></span>
<span data-ttu-id="97b7c-121">Имя группы ресурсов шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="97b7c-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="97b7c-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="97b7c-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="97b7c-123">Имя шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="97b7c-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="97b7c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b7c-124">CommonParameters</span></span>
<span data-ttu-id="97b7c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97b7c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b7c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b7c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b7c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97b7c-127">INPUTS</span></span>

### <span data-ttu-id="97b7c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="97b7c-128">System.String</span></span>

## <span data-ttu-id="97b7c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97b7c-129">OUTPUTS</span></span>

### <span data-ttu-id="97b7c-130">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="97b7c-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="97b7c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="97b7c-131">NOTES</span></span>
<span data-ttu-id="97b7c-132">Эта команда применима только к шлюзам виртуальных сетей Azure, для которых включены подключения BGP.</span><span class="sxs-lookup"><span data-stu-id="97b7c-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="97b7c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97b7c-133">RELATED LINKS</span></span>
