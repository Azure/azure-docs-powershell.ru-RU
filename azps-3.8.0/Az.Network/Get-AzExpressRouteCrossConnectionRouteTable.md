---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073370"
---
# <span data-ttu-id="bbe29-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="bbe29-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="bbe29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbe29-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe29-103">Возвращает таблицу маршрутов из перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bbe29-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="bbe29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbe29-104">SYNTAX</span></span>

### <span data-ttu-id="bbe29-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="bbe29-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bbe29-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="bbe29-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbe29-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe29-107">DESCRIPTION</span></span>
<span data-ttu-id="bbe29-108">Командлет **Get-AzExpressRouteCrossConnectionRouteTable** извлекает детальную таблицу маршрутов канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bbe29-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="bbe29-109">В таблице маршрутов отобразятся все маршруты или их можно отфильтровать, чтобы показать маршруты для определенного типа пиринга.</span><span class="sxs-lookup"><span data-stu-id="bbe29-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="bbe29-110">Вы можете использовать таблицу маршрутов для проверки конфигурации и подключения к одноранговым данным.</span><span class="sxs-lookup"><span data-stu-id="bbe29-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="bbe29-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbe29-111">EXAMPLES</span></span>

### <span data-ttu-id="bbe29-112">Пример 1: отображение таблицы маршрутов для основного пути</span><span class="sxs-lookup"><span data-stu-id="bbe29-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="bbe29-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbe29-113">PARAMETERS</span></span>

### <span data-ttu-id="bbe29-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="bbe29-114">-CrossConnectionName</span></span>
<span data-ttu-id="bbe29-115">Имя перекрестного соединения Express Route</span><span class="sxs-lookup"><span data-stu-id="bbe29-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="bbe29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe29-116">-DefaultProfile</span></span>
<span data-ttu-id="bbe29-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe29-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbe29-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="bbe29-118">-DevicePath</span></span>
<span data-ttu-id="bbe29-119">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="bbe29-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="bbe29-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="bbe29-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="bbe29-121">Перекрестное соединение Express Route</span><span class="sxs-lookup"><span data-stu-id="bbe29-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="bbe29-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="bbe29-122">-PeeringType</span></span>
<span data-ttu-id="bbe29-123">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="bbe29-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="bbe29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe29-124">-ResourceGroupName</span></span>
<span data-ttu-id="bbe29-125">Имя группы ресурсов, содержащей перекрестное соединение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bbe29-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="bbe29-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe29-126">CommonParameters</span></span>
<span data-ttu-id="bbe29-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbe29-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe29-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbe29-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe29-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbe29-129">INPUTS</span></span>

### <span data-ttu-id="bbe29-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="bbe29-130">None</span></span>
<span data-ttu-id="bbe29-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bbe29-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bbe29-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe29-132">OUTPUTS</span></span>

### <span data-ttu-id="bbe29-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="bbe29-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="bbe29-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbe29-134">NOTES</span></span>

## <span data-ttu-id="bbe29-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbe29-135">RELATED LINKS</span></span>

[<span data-ttu-id="bbe29-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="bbe29-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="bbe29-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="bbe29-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
