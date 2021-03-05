---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: c92033fa0ed907aab4c36f7dd980fb977a47be73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979603"
---
# <span data-ttu-id="92187-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="92187-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="92187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92187-102">SYNOPSIS</span></span>
<span data-ttu-id="92187-103">Получает таблицу маршрутов из перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="92187-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="92187-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92187-104">SYNTAX</span></span>

### <span data-ttu-id="92187-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="92187-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92187-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="92187-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92187-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92187-107">DESCRIPTION</span></span>
<span data-ttu-id="92187-108">Для получения подробной таблицы маршрутов из схемы ExpressRoute извлекается из таблицы маршрутов **Get-AzExpressRouteCrossConnectionRouteTable.**</span><span class="sxs-lookup"><span data-stu-id="92187-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="92187-109">В таблице маршрутов будут отфильтроваться все маршруты или отфильтровать маршруты для определенного типа пиринга.</span><span class="sxs-lookup"><span data-stu-id="92187-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="92187-110">Таблицу маршрутов можно использовать для проверки конфигурации пиринга и подключения.</span><span class="sxs-lookup"><span data-stu-id="92187-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="92187-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92187-111">EXAMPLES</span></span>

### <span data-ttu-id="92187-112">Пример 1. Отображение таблицы маршрутов для основного пути</span><span class="sxs-lookup"><span data-stu-id="92187-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="92187-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92187-113">PARAMETERS</span></span>

### <span data-ttu-id="92187-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="92187-114">-CrossConnectionName</span></span>
<span data-ttu-id="92187-115">Имя перекрестного подключения Express Route</span><span class="sxs-lookup"><span data-stu-id="92187-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92187-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92187-116">-DefaultProfile</span></span>
<span data-ttu-id="92187-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92187-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92187-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="92187-118">-DevicePath</span></span>
<span data-ttu-id="92187-119">Допустимыми значениями для этого параметра являются: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="92187-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="92187-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="92187-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="92187-121">Перекрестное подключение Express Route</span><span class="sxs-lookup"><span data-stu-id="92187-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92187-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="92187-122">-PeeringType</span></span>
<span data-ttu-id="92187-123">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="92187-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="92187-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92187-124">-ResourceGroupName</span></span>
<span data-ttu-id="92187-125">Имя группы ресурсов, содержащей перекрестное подключение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="92187-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92187-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92187-126">CommonParameters</span></span>
<span data-ttu-id="92187-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92187-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92187-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92187-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92187-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92187-129">INPUTS</span></span>

### <span data-ttu-id="92187-130">Нет</span><span class="sxs-lookup"><span data-stu-id="92187-130">None</span></span>
<span data-ttu-id="92187-131">Этот cmdlet не принимает входные данные.</span><span class="sxs-lookup"><span data-stu-id="92187-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92187-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92187-132">OUTPUTS</span></span>

### <span data-ttu-id="92187-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="92187-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="92187-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92187-134">NOTES</span></span>

## <span data-ttu-id="92187-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92187-135">RELATED LINKS</span></span>

[<span data-ttu-id="92187-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="92187-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="92187-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="92187-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
