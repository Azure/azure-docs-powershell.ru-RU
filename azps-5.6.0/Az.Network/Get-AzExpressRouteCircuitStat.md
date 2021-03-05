---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: e0f4b24581860f17024c9b01e62b3c84616c6f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997730"
---
# <span data-ttu-id="7162e-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="7162e-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="7162e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7162e-102">SYNOPSIS</span></span>
<span data-ttu-id="7162e-103">Возвращает статистику использования для каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7162e-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="7162e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7162e-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7162e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7162e-105">DESCRIPTION</span></span>
<span data-ttu-id="7162e-106">Чтобы получить статистику по каналу ExpressRoute, можно получить статистику трафика для **get-AzExpressRouteCircuitStat.**</span><span class="sxs-lookup"><span data-stu-id="7162e-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="7162e-107">Статистика содержит количество переданных и полученных bytes как по основному, так и по дополнительному маршруту.</span><span class="sxs-lookup"><span data-stu-id="7162e-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="7162e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7162e-108">EXAMPLES</span></span>

### <span data-ttu-id="7162e-109">Пример 1. Отображение статистики трафика для одноранговых служб ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7162e-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="7162e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7162e-110">PARAMETERS</span></span>

### <span data-ttu-id="7162e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7162e-111">-DefaultProfile</span></span>
<span data-ttu-id="7162e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7162e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7162e-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="7162e-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="7162e-114">Имя проверяемого контура ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7162e-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="7162e-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="7162e-115">-PeeringType</span></span>
<span data-ttu-id="7162e-116">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="7162e-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7162e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7162e-117">-ResourceGroupName</span></span>
<span data-ttu-id="7162e-118">Имя группы ресурсов, содержащей канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7162e-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="7162e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7162e-119">CommonParameters</span></span>
<span data-ttu-id="7162e-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7162e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7162e-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7162e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7162e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7162e-122">INPUTS</span></span>

### <span data-ttu-id="7162e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7162e-123">System.String</span></span>

## <span data-ttu-id="7162e-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7162e-124">OUTPUTS</span></span>

### <span data-ttu-id="7162e-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="7162e-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="7162e-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7162e-126">NOTES</span></span>

## <span data-ttu-id="7162e-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7162e-127">RELATED LINKS</span></span>

[<span data-ttu-id="7162e-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7162e-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="7162e-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7162e-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="7162e-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7162e-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
