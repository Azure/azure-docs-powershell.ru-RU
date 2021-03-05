---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 28a61e18f01f550f1b1ffd924119da3323905ad1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995375"
---
# <span data-ttu-id="60cb9-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="60cb9-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="60cb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="60cb9-103">Возвращает таблицу маршрутов из каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60cb9-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="60cb9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60cb9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60cb9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="60cb9-106">Cmdlet **Get-AzExpressRouteCircuitRouteTable** извлекает подробную таблицу маршрутов из схемы ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60cb9-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="60cb9-107">В таблице маршрутов будут отфильтроваться все маршруты или отфильтровать маршруты для определенного типа пиринга.</span><span class="sxs-lookup"><span data-stu-id="60cb9-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="60cb9-108">Таблицу маршрутов можно использовать для проверки конфигурации пиринга и подключения.</span><span class="sxs-lookup"><span data-stu-id="60cb9-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="60cb9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60cb9-109">EXAMPLES</span></span>

### <span data-ttu-id="60cb9-110">Пример 1. Отображение таблицы маршрутов для основного пути</span><span class="sxs-lookup"><span data-stu-id="60cb9-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="60cb9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60cb9-111">PARAMETERS</span></span>

### <span data-ttu-id="60cb9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60cb9-112">-DefaultProfile</span></span>
<span data-ttu-id="60cb9-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60cb9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60cb9-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="60cb9-114">-DevicePath</span></span>
<span data-ttu-id="60cb9-115">Допустимыми значениями для этого параметра являются: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="60cb9-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="60cb9-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="60cb9-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="60cb9-117">Имя проверяемого контура ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60cb9-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="60cb9-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="60cb9-118">-PeeringType</span></span>
<span data-ttu-id="60cb9-119">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="60cb9-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="60cb9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60cb9-120">-ResourceGroupName</span></span>
<span data-ttu-id="60cb9-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="60cb9-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="60cb9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cb9-122">CommonParameters</span></span>
<span data-ttu-id="60cb9-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60cb9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cb9-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60cb9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cb9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60cb9-125">INPUTS</span></span>

### <span data-ttu-id="60cb9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="60cb9-126">System.String</span></span>

## <span data-ttu-id="60cb9-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60cb9-127">OUTPUTS</span></span>

### <span data-ttu-id="60cb9-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="60cb9-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="60cb9-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60cb9-129">NOTES</span></span>

## <span data-ttu-id="60cb9-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60cb9-130">RELATED LINKS</span></span>

[<span data-ttu-id="60cb9-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="60cb9-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="60cb9-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="60cb9-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="60cb9-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="60cb9-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
