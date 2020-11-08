---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234974"
---
# <span data-ttu-id="49fcd-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="49fcd-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="49fcd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="49fcd-103">Создает объект VHubRoute, который можно передать как параметр для команды New-AzVHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="49fcd-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="49fcd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49fcd-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49fcd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49fcd-105">DESCRIPTION</span></span>

<span data-ttu-id="49fcd-106">Создает объект VHubRoute.</span><span class="sxs-lookup"><span data-stu-id="49fcd-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="49fcd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49fcd-107">EXAMPLES</span></span>

### <span data-ttu-id="49fcd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49fcd-108">Example 1</span></span>

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

<span data-ttu-id="49fcd-109">Вышеприведенная команда создаст объект VHubRoute с помощью nextHop в качестве указанного брандмауэра, который затем можно добавить в ресурс VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="49fcd-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="49fcd-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="49fcd-110">Example 2</span></span>

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

<span data-ttu-id="49fcd-111">Вышеприведенная команда создаст объект VHubRoute с помощью nextHop в качестве указанного hubVnetConnection, который затем можно добавить в ресурс VHubRouteTable.</span><span class="sxs-lookup"><span data-stu-id="49fcd-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="49fcd-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49fcd-112">PARAMETERS</span></span>

### <span data-ttu-id="49fcd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49fcd-113">-DefaultProfile</span></span>
<span data-ttu-id="49fcd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49fcd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49fcd-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="49fcd-115">-Destination</span></span>
<span data-ttu-id="49fcd-116">Список назначений.</span><span class="sxs-lookup"><span data-stu-id="49fcd-116">List of Destinations.</span></span>

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

### <span data-ttu-id="49fcd-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="49fcd-117">-DestinationType</span></span>
<span data-ttu-id="49fcd-118">Тип назначений.</span><span class="sxs-lookup"><span data-stu-id="49fcd-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="49fcd-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49fcd-119">-Name</span></span>
<span data-ttu-id="49fcd-120">Имя маршрута.</span><span class="sxs-lookup"><span data-stu-id="49fcd-120">The route name.</span></span>

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

### <span data-ttu-id="49fcd-121">-NextHop</span><span class="sxs-lookup"><span data-stu-id="49fcd-121">-NextHop</span></span>
<span data-ttu-id="49fcd-122">Следующий прыжок.</span><span class="sxs-lookup"><span data-stu-id="49fcd-122">The next hop.</span></span>

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

### <span data-ttu-id="49fcd-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="49fcd-123">-NextHopType</span></span>
<span data-ttu-id="49fcd-124">Тип следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="49fcd-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="49fcd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49fcd-125">CommonParameters</span></span>
<span data-ttu-id="49fcd-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49fcd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49fcd-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49fcd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49fcd-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49fcd-128">INPUTS</span></span>

### <span data-ttu-id="49fcd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="49fcd-129">System.String</span></span>

## <span data-ttu-id="49fcd-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49fcd-130">OUTPUTS</span></span>

### <span data-ttu-id="49fcd-131">Microsoft. Azure. Commands. Network. Models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="49fcd-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="49fcd-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="49fcd-132">NOTES</span></span>

## <span data-ttu-id="49fcd-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49fcd-133">RELATED LINKS</span></span>

[<span data-ttu-id="49fcd-134">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="49fcd-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="49fcd-135">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="49fcd-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="49fcd-136">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="49fcd-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="49fcd-137">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="49fcd-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)