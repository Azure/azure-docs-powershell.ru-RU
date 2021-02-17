---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: b8087721351a834f50a2f3f3b8a9b792f4bfc393
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408225"
---
# <span data-ttu-id="62e4f-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="62e4f-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="62e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="62e4f-103">Возвращает таблицу маршрутов из каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="62e4f-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="62e4f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62e4f-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62e4f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="62e4f-106">Cmdlet **Get-AzExpressRouteCircuitRouteTable** извлекает подробную таблицу маршрутов из схемы ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="62e4f-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="62e4f-107">В таблице маршрутов будут отфильтроваться все маршруты или отфильтровать маршруты для определенного типа пиринга.</span><span class="sxs-lookup"><span data-stu-id="62e4f-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="62e4f-108">Таблицу маршрутов можно использовать для проверки конфигурации пиринга и подключения.</span><span class="sxs-lookup"><span data-stu-id="62e4f-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="62e4f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62e4f-109">EXAMPLES</span></span>

### <span data-ttu-id="62e4f-110">Пример 1. Отображение таблицы маршрутов для основного пути</span><span class="sxs-lookup"><span data-stu-id="62e4f-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="62e4f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62e4f-111">PARAMETERS</span></span>

### <span data-ttu-id="62e4f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e4f-112">-DefaultProfile</span></span>
<span data-ttu-id="62e4f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62e4f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62e4f-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="62e4f-114">-DevicePath</span></span>
<span data-ttu-id="62e4f-115">Допустимыми значениями для этого параметра являются: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="62e4f-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="62e4f-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="62e4f-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="62e4f-117">Имя проверяемого контура ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="62e4f-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="62e4f-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="62e4f-118">-PeeringType</span></span>
<span data-ttu-id="62e4f-119">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="62e4f-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="62e4f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e4f-120">-ResourceGroupName</span></span>
<span data-ttu-id="62e4f-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="62e4f-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="62e4f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e4f-122">CommonParameters</span></span>
<span data-ttu-id="62e4f-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e4f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e4f-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62e4f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e4f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62e4f-125">INPUTS</span></span>

### <span data-ttu-id="62e4f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="62e4f-126">System.String</span></span>

## <span data-ttu-id="62e4f-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62e4f-127">OUTPUTS</span></span>

### <span data-ttu-id="62e4f-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="62e4f-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="62e4f-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62e4f-129">NOTES</span></span>

## <span data-ttu-id="62e4f-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62e4f-130">RELATED LINKS</span></span>

[<span data-ttu-id="62e4f-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="62e4f-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="62e4f-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="62e4f-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="62e4f-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="62e4f-133">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
