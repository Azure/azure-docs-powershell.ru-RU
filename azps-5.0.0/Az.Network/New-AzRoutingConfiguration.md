---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: 31601c93a6979d09dfb3641cac079cba2757d043
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317060"
---
# <span data-ttu-id="b9f35-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9f35-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="b9f35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9f35-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f35-103">Создает объект RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b9f35-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="b9f35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9f35-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9f35-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9f35-105">DESCRIPTION</span></span>
<span data-ttu-id="b9f35-106">Создает объект RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b9f35-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="b9f35-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9f35-107">EXAMPLES</span></span>

### <span data-ttu-id="b9f35-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9f35-108">Example 1</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
```

<span data-ttu-id="b9f35-109">Вышеприведенная команда создаст объект RoutingConfiguration, который затем можно будет добавить в ресурс подключения.</span><span class="sxs-lookup"><span data-stu-id="b9f35-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="b9f35-110">Статические маршруты разрешены только для объекта HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="b9f35-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="b9f35-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9f35-111">PARAMETERS</span></span>

### <span data-ttu-id="b9f35-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f35-112">-DefaultProfile</span></span>
<span data-ttu-id="b9f35-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9f35-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9f35-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="b9f35-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="b9f35-115">Таблица маршрута Hub, связанная с этой конфигурацией маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="b9f35-115">The hub route table associated with this routing configuration.</span></span>

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

### <span data-ttu-id="b9f35-116">-ID</span><span class="sxs-lookup"><span data-stu-id="b9f35-116">-Id</span></span>
<span data-ttu-id="b9f35-117">Список идентификаторов ресурсов всех таблиц узлов-маршрутов, для которых объявляются маршруты для свойства PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="b9f35-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="b9f35-118">-Label</span><span class="sxs-lookup"><span data-stu-id="b9f35-118">-Label</span></span>
<span data-ttu-id="b9f35-119">Список меток для свойства PropagatedRouteTables.</span><span class="sxs-lookup"><span data-stu-id="b9f35-119">The list of labels for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f35-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="b9f35-120">-StaticRoute</span></span>
<span data-ttu-id="b9f35-121">Список маршрутов, управляющих маршрутизацией от VirtualHub к виртуальному сетевому подключению.</span><span class="sxs-lookup"><span data-stu-id="b9f35-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

```yaml
Type: PSStaticRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f35-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f35-122">CommonParameters</span></span>
<span data-ttu-id="b9f35-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9f35-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f35-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9f35-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f35-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9f35-125">INPUTS</span></span>

### <span data-ttu-id="b9f35-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b9f35-126">System.String</span></span>

### <span data-ttu-id="b9f35-127">Microsoft. Azure. Commands. Network. Models. PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="b9f35-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="b9f35-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9f35-128">OUTPUTS</span></span>

### <span data-ttu-id="b9f35-129">Microsoft. Azure. Commands. Network. Models. PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9f35-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="b9f35-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9f35-130">NOTES</span></span>

## <span data-ttu-id="b9f35-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9f35-131">RELATED LINKS</span></span>

[<span data-ttu-id="b9f35-132">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="b9f35-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="b9f35-133">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="b9f35-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="b9f35-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="b9f35-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="b9f35-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b9f35-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="b9f35-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="b9f35-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="b9f35-137">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b9f35-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="b9f35-138">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="b9f35-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="b9f35-139">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b9f35-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="b9f35-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b9f35-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)