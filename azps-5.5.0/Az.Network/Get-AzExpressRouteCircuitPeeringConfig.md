---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218809"
---
# <span data-ttu-id="c557a-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c557a-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="c557a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c557a-102">SYNOPSIS</span></span>
<span data-ttu-id="c557a-103">Получает конфигурацию пиринга для каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c557a-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="c557a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c557a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c557a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c557a-105">DESCRIPTION</span></span>
<span data-ttu-id="c557a-106">Cmdlet **Get-AzExpressRouteCircuitPeeringConfig** извлекает конфигурацию отношения пиринга для схемы ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c557a-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c557a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c557a-107">EXAMPLES</span></span>

### <span data-ttu-id="c557a-108">Пример 1. Отображение конфигурации пиринга для схемы ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c557a-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="c557a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c557a-109">PARAMETERS</span></span>

### <span data-ttu-id="c557a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c557a-110">-DefaultProfile</span></span>
<span data-ttu-id="c557a-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c557a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c557a-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c557a-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c557a-113">Объект схемы ExpressRoute, содержащий конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="c557a-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="c557a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c557a-114">-Name</span></span>
<span data-ttu-id="c557a-115">Имя извлекаемой конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="c557a-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="c557a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c557a-116">CommonParameters</span></span>
<span data-ttu-id="c557a-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c557a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c557a-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c557a-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c557a-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c557a-119">INPUTS</span></span>

### <span data-ttu-id="c557a-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c557a-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c557a-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c557a-121">OUTPUTS</span></span>

### <span data-ttu-id="c557a-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="c557a-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="c557a-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c557a-123">NOTES</span></span>

## <span data-ttu-id="c557a-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c557a-124">RELATED LINKS</span></span>

[<span data-ttu-id="c557a-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c557a-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c557a-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c557a-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c557a-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="c557a-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="c557a-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c557a-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
