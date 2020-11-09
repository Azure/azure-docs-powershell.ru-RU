---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 9cd5a4417f3fd8d6d40cfdf70e6c76f1910ce7c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317021"
---
# <span data-ttu-id="a3c9b-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="a3c9b-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="a3c9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c9b-103">Создает объект VHubRoute, который можно передать как параметр для команды New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="a3c9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3c9b-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3c9b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3c9b-105">DESCRIPTION</span></span>

<span data-ttu-id="a3c9b-106">Создает объект VHubRoute.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="a3c9b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3c9b-107">EXAMPLES</span></span>

### <span data-ttu-id="a3c9b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3c9b-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="a3c9b-109">Вышеприведенная команда создаст объект VHubRoute с помощью nextHop в качестве указанного брандмауэра, который затем можно добавить в ресурс VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="a3c9b-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a3c9b-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="a3c9b-111">Вышеприведенная команда создаст объект VHubRoute с помощью nextHop в качестве указанного hubVnetConnection, который затем можно добавить в ресурс VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>


### <span data-ttu-id="a3c9b-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a3c9b-112">Example 3</span></span>
```powershell
PS C:\> $hub = Get-AzVirtualHub -ResourceGroupName {rgname} -Name {virtual-hub-name}
PS C:\> $hubVnetConn = Get-AzVirtualHubVnetConnection -ParentObject $hub -Name {connection-name}
PS C:\> $hubVnetConn
Name                   : conn_2
Id                     : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubVirtualNetworkConnections/conn_2
RemoteVirtualNetwork   : /subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualNetworks/rVnet_2
EnableInternetSecurity : True
ProvisioningState      : Succeeded
RoutingConfiguration   : {
                           "AssociatedRouteTable": {
                             "Id": "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                           },
                           "PropagatedRouteTables": {
                             "Labels": [
                               "default"
                             ],
                             "Ids": [
                               {
                                 "Id":
                         "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/{virtual-hub-name}/hubRouteTables/defaultRouteTable"
                               }
                             ]
                           },
                           "VnetRoutes": {
                             "StaticRoutes": []
                           }
                         }
                         
PS C:\> $staticRoute1 = New-AzStaticRoute -Name "static_route1" -AddressPrefix @("10.2.1.0/24", "10.2.3.0/24") -NextHopIpAddress "10.2.0.5"
PS C:\> $routingConfig = $hubVnetConn.RoutingConfiguration
PS C:\> $routingConfig.VnetRoutes.StaticRoutes = @($staticRoute1)
PS C:\> $routingConfig
AssociatedRouteTable  : Microsoft.Azure.Commands.Network.Models.PSResourceId
PropagatedRouteTables : {
                          "Labels": [
                            "default"
                          ],
                          "Ids": [
                            {
                              "Id":
                        "/subscriptions/{subscriptionID}/resourceGroups/{rgname}/providers/Microsoft.Network/virtualHubs/rTestHub1/hubRouteTables/defaultRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "static_route1",
                              "AddressPrefixes": [
                                "10.2.1.0/24",
                                "10.2.3.0/24"
                              ],
                              "NextHopIpAddress": "10.2.0.5"
                            }
                          ]
                        }

PS C:\> Update-AzVirtualHubVnetConnection -InputObject $hubVnetConn -RoutingConfiguration $routingConfig
```
<span data-ttu-id="a3c9b-113">Описанные выше команды получит RoutingConfiguration уже существующий AzVHubRoute и добавить статический маршрут для соединения.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-113">The above commands will get the RoutingConfiguration of an already existing AzVHubRoute and then add a static route on the connection.</span></span> <span data-ttu-id="a3c9b-114">Кроме того, если вы планируете создать новое подключение с использованием статического маршрута, ознакомьтесь с разрешениями в [статье](New-AzRoutingConfiguration.md) пример 1.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-114">Alternatively, if you hope to create a new connection with the static route within it, please see Example 1 [here.](New-AzRoutingConfiguration.md)</span></span>
## <span data-ttu-id="a3c9b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3c9b-115">PARAMETERS</span></span>

### <span data-ttu-id="a3c9b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c9b-116">-DefaultProfile</span></span>
<span data-ttu-id="a3c9b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c9b-118">-Destination</span><span class="sxs-lookup"><span data-stu-id="a3c9b-118">-Destination</span></span>
<span data-ttu-id="a3c9b-119">Список назначений.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-119">List of Destinations.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c9b-120">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="a3c9b-120">-DestinationType</span></span>
<span data-ttu-id="a3c9b-121">Тип назначений.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-121">Type of Destinations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c9b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3c9b-122">-Name</span></span>
<span data-ttu-id="a3c9b-123">Имя маршрута.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-123">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c9b-124">-NextHop</span><span class="sxs-lookup"><span data-stu-id="a3c9b-124">-NextHop</span></span>
<span data-ttu-id="a3c9b-125">Следующий прыжок.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-125">The next hop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c9b-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="a3c9b-126">-NextHopType</span></span>
<span data-ttu-id="a3c9b-127">Тип следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-127">The Next Hop type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3c9b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c9b-128">CommonParameters</span></span>
<span data-ttu-id="a3c9b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3c9b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c9b-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3c9b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c9b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3c9b-131">INPUTS</span></span>

### <span data-ttu-id="a3c9b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a3c9b-132">System.String</span></span>

## <span data-ttu-id="a3c9b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3c9b-133">OUTPUTS</span></span>

### <span data-ttu-id="a3c9b-134">Microsoft. Azure. Commands. Network. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="a3c9b-134">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="a3c9b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3c9b-135">NOTES</span></span>

## <span data-ttu-id="a3c9b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3c9b-136">RELATED LINKS</span></span>

[<span data-ttu-id="a3c9b-137">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a3c9b-137">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="a3c9b-138">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a3c9b-138">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="a3c9b-139">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a3c9b-139">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="a3c9b-140">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="a3c9b-140">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)