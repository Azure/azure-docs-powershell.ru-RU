---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248587"
---
# <span data-ttu-id="623fc-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="623fc-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="623fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="623fc-102">SYNOPSIS</span></span>
<span data-ttu-id="623fc-103">Возвращает конфигурацию пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="623fc-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="623fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="623fc-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="623fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="623fc-105">DESCRIPTION</span></span>
<span data-ttu-id="623fc-106">Командлет **Get-AzExpressRouteCircuitPeeringConfig** извлекает конфигурацию однорангового отношения для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="623fc-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="623fc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="623fc-107">EXAMPLES</span></span>

### <span data-ttu-id="623fc-108">Пример 1: отображение конфигурации пиринга для канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="623fc-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="623fc-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="623fc-109">PARAMETERS</span></span>

### <span data-ttu-id="623fc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623fc-110">-DefaultProfile</span></span>
<span data-ttu-id="623fc-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="623fc-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="623fc-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="623fc-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="623fc-113">Объект цепи ExpressRoute, который содержит конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="623fc-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="623fc-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="623fc-114">-Name</span></span>
<span data-ttu-id="623fc-115">Имя конфигурации пиринга, которую нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="623fc-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623fc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623fc-116">CommonParameters</span></span>
<span data-ttu-id="623fc-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="623fc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623fc-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="623fc-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623fc-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="623fc-119">INPUTS</span></span>

### <span data-ttu-id="623fc-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="623fc-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="623fc-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="623fc-121">OUTPUTS</span></span>

### <span data-ttu-id="623fc-122">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="623fc-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="623fc-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="623fc-123">NOTES</span></span>

## <span data-ttu-id="623fc-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="623fc-124">RELATED LINKS</span></span>

[<span data-ttu-id="623fc-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="623fc-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="623fc-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="623fc-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="623fc-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="623fc-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="623fc-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="623fc-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
