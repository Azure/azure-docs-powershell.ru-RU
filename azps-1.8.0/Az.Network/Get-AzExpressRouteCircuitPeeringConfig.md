---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c8e821408f3d65ace31ab2340f544a0a47e120e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730599"
---
# <span data-ttu-id="360b3-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="360b3-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="360b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="360b3-102">SYNOPSIS</span></span>
<span data-ttu-id="360b3-103">Возвращает конфигурацию пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="360b3-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="360b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="360b3-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="360b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="360b3-105">DESCRIPTION</span></span>
<span data-ttu-id="360b3-106">Командлет **Get-AzExpressRouteCircuitPeeringConfig** извлекает конфигурацию однорангового отношения для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="360b3-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="360b3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="360b3-107">EXAMPLES</span></span>

### <span data-ttu-id="360b3-108">Пример 1: отображение конфигурации пиринга для канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="360b3-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="360b3-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="360b3-109">PARAMETERS</span></span>

### <span data-ttu-id="360b3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360b3-110">-DefaultProfile</span></span>
<span data-ttu-id="360b3-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="360b3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="360b3-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="360b3-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="360b3-113">Объект цепи ExpressRoute, который содержит конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="360b3-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="360b3-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="360b3-114">-Name</span></span>
<span data-ttu-id="360b3-115">Имя конфигурации пиринга, которую нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="360b3-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="360b3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360b3-116">CommonParameters</span></span>
<span data-ttu-id="360b3-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="360b3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360b3-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="360b3-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360b3-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="360b3-119">INPUTS</span></span>

### <span data-ttu-id="360b3-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="360b3-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="360b3-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="360b3-121">OUTPUTS</span></span>

### <span data-ttu-id="360b3-122">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="360b3-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="360b3-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="360b3-123">NOTES</span></span>

## <span data-ttu-id="360b3-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="360b3-124">RELATED LINKS</span></span>

[<span data-ttu-id="360b3-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="360b3-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="360b3-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="360b3-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="360b3-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="360b3-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="360b3-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="360b3-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
