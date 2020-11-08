---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246230"
---
# <span data-ttu-id="dcedb-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dcedb-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="dcedb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcedb-102">SYNOPSIS</span></span>
<span data-ttu-id="dcedb-103">Возвращает сводку по таблице маршрутов для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcedb-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="dcedb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcedb-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcedb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcedb-105">DESCRIPTION</span></span>
<span data-ttu-id="dcedb-106">Командлет **Get-AzExpressRouteCircuitRouteTableSummary** извлекает сводку сведений о соседях BGP для определенного контекста маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="dcedb-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="dcedb-107">Эти сведения полезны для определения времени, в течение которого был установлен контекст маршрутизации, и количества префиксов маршрутов, объявленных маршрутизатором пиринга.</span><span class="sxs-lookup"><span data-stu-id="dcedb-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="dcedb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcedb-108">EXAMPLES</span></span>

### <span data-ttu-id="dcedb-109">Пример 1: отображение сводки маршрута для основного пути</span><span class="sxs-lookup"><span data-stu-id="dcedb-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="dcedb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcedb-110">PARAMETERS</span></span>

### <span data-ttu-id="dcedb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcedb-111">-DefaultProfile</span></span>
<span data-ttu-id="dcedb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcedb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcedb-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="dcedb-113">-DevicePath</span></span>
<span data-ttu-id="dcedb-114">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="dcedb-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcedb-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="dcedb-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="dcedb-116">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcedb-116">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcedb-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="dcedb-117">-PeeringType</span></span>
<span data-ttu-id="dcedb-118">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="dcedb-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcedb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcedb-119">-ResourceGroupName</span></span>
<span data-ttu-id="dcedb-120">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dcedb-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="dcedb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcedb-121">CommonParameters</span></span>
<span data-ttu-id="dcedb-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcedb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcedb-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcedb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcedb-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcedb-124">INPUTS</span></span>

### <span data-ttu-id="dcedb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dcedb-125">System.String</span></span>

## <span data-ttu-id="dcedb-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcedb-126">OUTPUTS</span></span>

### <span data-ttu-id="dcedb-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="dcedb-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="dcedb-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcedb-128">NOTES</span></span>

## <span data-ttu-id="dcedb-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcedb-129">RELATED LINKS</span></span>

[<span data-ttu-id="dcedb-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="dcedb-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="dcedb-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="dcedb-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="dcedb-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="dcedb-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
