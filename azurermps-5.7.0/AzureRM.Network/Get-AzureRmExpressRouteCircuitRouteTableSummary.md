---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 849fb653308537a3d37740a21ba8b488903406ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565486"
---
# <span data-ttu-id="c33e1-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c33e1-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="c33e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c33e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c33e1-103">Возвращает сводку по таблице маршрутов для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c33e1-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c33e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c33e1-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c33e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c33e1-105">DESCRIPTION</span></span>
<span data-ttu-id="c33e1-106">Командлет **Get-AzureRmExpressRouteCircuitRouteTableSummary** извлекает сводку сведений о соседях BGP для определенного контекста маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c33e1-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="c33e1-107">Эти сведения полезны для определения времени, в течение которого был установлен контекст маршрутизации, и количества префиксов маршрутов, объявленных маршрутизатором пиринга.</span><span class="sxs-lookup"><span data-stu-id="c33e1-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="c33e1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c33e1-108">EXAMPLES</span></span>

### <span data-ttu-id="c33e1-109">Пример 1: отображение сводки маршрута для основного пути</span><span class="sxs-lookup"><span data-stu-id="c33e1-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="c33e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c33e1-110">PARAMETERS</span></span>

### <span data-ttu-id="c33e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33e1-111">-DefaultProfile</span></span>
<span data-ttu-id="c33e1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c33e1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c33e1-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="c33e1-113">-DevicePath</span></span>
<span data-ttu-id="c33e1-114">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="c33e1-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="c33e1-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="c33e1-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="c33e1-116">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c33e1-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="c33e1-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c33e1-117">-PeeringType</span></span>
<span data-ttu-id="c33e1-118">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c33e1-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="c33e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c33e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="c33e1-120">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c33e1-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="c33e1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33e1-121">CommonParameters</span></span>
<span data-ttu-id="c33e1-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c33e1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33e1-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c33e1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33e1-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c33e1-124">INPUTS</span></span>

### <span data-ttu-id="c33e1-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="c33e1-125">None</span></span>
<span data-ttu-id="c33e1-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c33e1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c33e1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c33e1-127">OUTPUTS</span></span>

### <span data-ttu-id="c33e1-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="c33e1-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="c33e1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c33e1-129">NOTES</span></span>

## <span data-ttu-id="c33e1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c33e1-130">RELATED LINKS</span></span>

[<span data-ttu-id="c33e1-131">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c33e1-131">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="c33e1-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c33e1-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c33e1-133">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="c33e1-133">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
