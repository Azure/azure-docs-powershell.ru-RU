---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 5042f7055c9d74dcabc01aa81169c9290816953c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909994"
---
# <span data-ttu-id="dd280-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="dd280-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="dd280-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd280-102">SYNOPSIS</span></span>
<span data-ttu-id="dd280-103">Возвращает сводку по таблице маршрутов для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dd280-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="dd280-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd280-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd280-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd280-105">DESCRIPTION</span></span>
<span data-ttu-id="dd280-106">Командлет **Get-AzExpressRouteCircuitRouteTableSummary** извлекает сводку сведений о соседях BGP для определенного контекста маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="dd280-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="dd280-107">Эти сведения полезны для определения времени, в течение которого был установлен контекст маршрутизации, и количества префиксов маршрутов, объявленных маршрутизатором пиринга.</span><span class="sxs-lookup"><span data-stu-id="dd280-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="dd280-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd280-108">EXAMPLES</span></span>

### <span data-ttu-id="dd280-109">Пример 1: отображение сводки маршрута для основного пути</span><span class="sxs-lookup"><span data-stu-id="dd280-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="dd280-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd280-110">PARAMETERS</span></span>

### <span data-ttu-id="dd280-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd280-111">-DefaultProfile</span></span>
<span data-ttu-id="dd280-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd280-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd280-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="dd280-113">-DevicePath</span></span>
<span data-ttu-id="dd280-114">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="dd280-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="dd280-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="dd280-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="dd280-116">Имя проверяемого канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dd280-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="dd280-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="dd280-117">-PeeringType</span></span>
<span data-ttu-id="dd280-118">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="dd280-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="dd280-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd280-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd280-120">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dd280-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="dd280-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd280-121">CommonParameters</span></span>
<span data-ttu-id="dd280-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd280-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd280-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd280-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd280-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd280-124">INPUTS</span></span>

## <span data-ttu-id="dd280-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd280-125">OUTPUTS</span></span>

### <span data-ttu-id="dd280-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="dd280-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="dd280-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd280-127">NOTES</span></span>

## <span data-ttu-id="dd280-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd280-128">RELATED LINKS</span></span>

[<span data-ttu-id="dd280-129">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="dd280-129">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="dd280-130">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="dd280-130">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="dd280-131">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="dd280-131">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
