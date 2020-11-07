---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: bb6ffb1537a5beb6a845bbad742b864360da55d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902962"
---
# <span data-ttu-id="7c5c8-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7c5c8-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="7c5c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5c8-103">Возвращает таблицу маршрутов из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="7c5c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c5c8-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c5c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="7c5c8-106">Командлет **Get-AzExpressRouteCircuitRouteTable** извлекает детальную таблицу маршрутов канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="7c5c8-107">В таблице маршрутов отобразятся все маршруты или их можно отфильтровать, чтобы показать маршруты для определенного типа пиринга.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="7c5c8-108">Вы можете использовать таблицу маршрутов для проверки конфигурации и подключения к одноранговым данным.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="7c5c8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c5c8-109">EXAMPLES</span></span>

### <span data-ttu-id="7c5c8-110">Пример 1: отображение таблицы маршрутов для основного пути</span><span class="sxs-lookup"><span data-stu-id="7c5c8-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="7c5c8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c5c8-111">PARAMETERS</span></span>

### <span data-ttu-id="7c5c8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5c8-112">-DefaultProfile</span></span>
<span data-ttu-id="7c5c8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c5c8-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="7c5c8-114">-DevicePath</span></span>
<span data-ttu-id="7c5c8-115">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="7c5c8-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="7c5c8-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="7c5c8-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="7c5c8-117">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="7c5c8-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7c5c8-118">-PeeringType</span></span>
<span data-ttu-id="7c5c8-119">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7c5c8-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="7c5c8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c5c8-120">-ResourceGroupName</span></span>
<span data-ttu-id="7c5c8-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="7c5c8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5c8-122">CommonParameters</span></span>
<span data-ttu-id="7c5c8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c5c8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5c8-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c5c8-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5c8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c5c8-125">INPUTS</span></span>

### <span data-ttu-id="7c5c8-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7c5c8-126">System.String</span></span>

## <span data-ttu-id="7c5c8-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c5c8-127">OUTPUTS</span></span>

### <span data-ttu-id="7c5c8-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="7c5c8-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="7c5c8-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c5c8-129">NOTES</span></span>

## <span data-ttu-id="7c5c8-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c5c8-130">RELATED LINKS</span></span>

[<span data-ttu-id="7c5c8-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7c5c8-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="7c5c8-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7c5c8-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="7c5c8-133">Get-AzExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="7c5c8-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
