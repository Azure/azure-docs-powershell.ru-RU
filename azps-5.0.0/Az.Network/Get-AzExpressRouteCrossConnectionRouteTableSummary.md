---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 7479d18660ede3f70ac5e62f614b8a815b86433c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317210"
---
# <span data-ttu-id="ccea1-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ccea1-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="ccea1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ccea1-102">SYNOPSIS</span></span>
<span data-ttu-id="ccea1-103">Возвращает сводку по таблице маршрутов для перекрестного соединения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ccea1-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="ccea1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ccea1-104">SYNTAX</span></span>

### <span data-ttu-id="ccea1-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="ccea1-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccea1-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="ccea1-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccea1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccea1-107">DESCRIPTION</span></span>
<span data-ttu-id="ccea1-108">Командлет **Get-AzExpressRouteCrossConnectionRouteTableSummary** извлекает сводку сведений о соседях BGP для определенного контекста маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ccea1-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="ccea1-109">Эти сведения полезны для определения времени, в течение которого был установлен контекст маршрутизации, и количества префиксов маршрутов, объявленных маршрутизатором пиринга.</span><span class="sxs-lookup"><span data-stu-id="ccea1-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="ccea1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ccea1-110">EXAMPLES</span></span>

### <span data-ttu-id="ccea1-111">Пример 1: отображение сводки маршрута для основного пути</span><span class="sxs-lookup"><span data-stu-id="ccea1-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="ccea1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ccea1-112">PARAMETERS</span></span>

### <span data-ttu-id="ccea1-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="ccea1-113">-CrossConnectionName</span></span>
<span data-ttu-id="ccea1-114">Имя перекрестного соединения Express Route</span><span class="sxs-lookup"><span data-stu-id="ccea1-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="ccea1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccea1-115">-DefaultProfile</span></span>
<span data-ttu-id="ccea1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccea1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccea1-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="ccea1-117">-DevicePath</span></span>
<span data-ttu-id="ccea1-118">Допустимые значения этого параметра: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="ccea1-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="ccea1-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ccea1-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ccea1-120">Перекрестное соединение Express Route</span><span class="sxs-lookup"><span data-stu-id="ccea1-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="ccea1-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ccea1-121">-PeeringType</span></span>
<span data-ttu-id="ccea1-122">Допустимые значения этого параметра: `AzurePrivatePeering` , `AzurePublicPeering` и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ccea1-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ccea1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccea1-123">-ResourceGroupName</span></span>
<span data-ttu-id="ccea1-124">Имя группы ресурсов, содержащей перекрестное соединение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ccea1-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="ccea1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccea1-125">CommonParameters</span></span>
<span data-ttu-id="ccea1-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ccea1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccea1-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccea1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccea1-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ccea1-128">INPUTS</span></span>

### <span data-ttu-id="ccea1-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="ccea1-129">None</span></span>
<span data-ttu-id="ccea1-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ccea1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ccea1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccea1-131">OUTPUTS</span></span>

### <span data-ttu-id="ccea1-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="ccea1-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="ccea1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ccea1-133">NOTES</span></span>

## <span data-ttu-id="ccea1-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccea1-134">RELATED LINKS</span></span>

[<span data-ttu-id="ccea1-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="ccea1-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="ccea1-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ccea1-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
