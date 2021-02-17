---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: bca0dde2947b214d13032b54681f2fc179c26af1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401969"
---
# <span data-ttu-id="2b8c7-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2b8c7-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="2b8c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8c7-103">Возвращает сводку таблицы маршрутов по каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2b8c7-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2b8c7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b8c7-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b8c7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b8c7-105">DESCRIPTION</span></span>
<span data-ttu-id="2b8c7-106">Cmdlet **Get-AzExpressRouteCircuitRouteTableSummary** извлекает сводку данных о соседних BGP для определенного контекста маршрутации.</span><span class="sxs-lookup"><span data-stu-id="2b8c7-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="2b8c7-107">Эти сведения полезны для определения времени установления контекста маршрутки и количества префиксов маршрутов, объявленных маршрутизатором пиринга.</span><span class="sxs-lookup"><span data-stu-id="2b8c7-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="2b8c7-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b8c7-108">EXAMPLES</span></span>

### <span data-ttu-id="2b8c7-109">Пример 1. Отображение сводки маршрута для основного пути</span><span class="sxs-lookup"><span data-stu-id="2b8c7-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="2b8c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b8c7-110">PARAMETERS</span></span>

### <span data-ttu-id="2b8c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8c7-111">-DefaultProfile</span></span>
<span data-ttu-id="2b8c7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b8c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b8c7-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="2b8c7-113">-DevicePath</span></span>
<span data-ttu-id="2b8c7-114">Допустимыми значениями для этого параметра являются: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="2b8c7-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="2b8c7-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="2b8c7-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="2b8c7-116">Имя проверяемого контура ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2b8c7-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="2b8c7-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2b8c7-117">-PeeringType</span></span>
<span data-ttu-id="2b8c7-118">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2b8c7-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="2b8c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b8c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="2b8c7-120">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2b8c7-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="2b8c7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8c7-121">CommonParameters</span></span>
<span data-ttu-id="2b8c7-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b8c7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8c7-123">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b8c7-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8c7-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b8c7-124">INPUTS</span></span>

### <span data-ttu-id="2b8c7-125">System.String</span><span class="sxs-lookup"><span data-stu-id="2b8c7-125">System.String</span></span>

## <span data-ttu-id="2b8c7-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b8c7-126">OUTPUTS</span></span>

### <span data-ttu-id="2b8c7-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="2b8c7-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="2b8c7-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b8c7-128">NOTES</span></span>

## <span data-ttu-id="2b8c7-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b8c7-129">RELATED LINKS</span></span>

[<span data-ttu-id="2b8c7-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2b8c7-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="2b8c7-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2b8c7-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="2b8c7-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="2b8c7-132">Get-AzExpressRouteCircuitStat</span></span>](Get-AzExpressRouteCircuitStat.md)
