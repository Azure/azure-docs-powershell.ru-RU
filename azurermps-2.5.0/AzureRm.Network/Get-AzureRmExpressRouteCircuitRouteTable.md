---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
ms.openlocfilehash: 883d2ae51046f3dc1ee6c8350d996fedbfff083e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914078"
---
# <span data-ttu-id="0a663-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a663-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="0a663-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a663-102">SYNOPSIS</span></span>
<span data-ttu-id="0a663-103">Возвращает таблицу маршрутов из канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0a663-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a663-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a663-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a663-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a663-105">DESCRIPTION</span></span>
<span data-ttu-id="0a663-106">Командлет **Get-AzureRmExpressRouteCircuitRouteTable** извлекает детальную таблицу маршрутов канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0a663-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="0a663-107">В таблице маршрутов отобразятся все маршруты или их можно отфильтровать, чтобы показать маршруты для определенного типа пиринга.</span><span class="sxs-lookup"><span data-stu-id="0a663-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="0a663-108">Вы можете использовать таблицу маршрутов для проверки конфигурации и подключения к одноранговым данным.</span><span class="sxs-lookup"><span data-stu-id="0a663-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="0a663-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a663-109">EXAMPLES</span></span>

### <span data-ttu-id="0a663-110">Пример 1: отображение таблицы маршрутов для основного пути</span><span class="sxs-lookup"><span data-stu-id="0a663-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="0a663-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a663-111">PARAMETERS</span></span>

### <span data-ttu-id="0a663-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a663-112">-DefaultProfile</span></span>
<span data-ttu-id="0a663-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a663-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a663-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="0a663-114">-DevicePath</span></span>
<span data-ttu-id="0a663-115">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="0a663-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a663-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="0a663-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="0a663-117">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0a663-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a663-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="0a663-118">-PeeringType</span></span>
<span data-ttu-id="0a663-119">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="0a663-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a663-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a663-120">-ResourceGroupName</span></span>
<span data-ttu-id="0a663-121">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0a663-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a663-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a663-122">CommonParameters</span></span>
<span data-ttu-id="0a663-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a663-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a663-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a663-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a663-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a663-125">INPUTS</span></span>

## <span data-ttu-id="0a663-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a663-126">OUTPUTS</span></span>

### <span data-ttu-id="0a663-127">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="0a663-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="0a663-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a663-128">NOTES</span></span>

## <span data-ttu-id="0a663-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a663-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a663-130">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0a663-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="0a663-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0a663-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="0a663-132">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="0a663-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
