---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 204d70753d3a4ae80e05dfff90d4a5b50b47ab58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568886"
---
# <span data-ttu-id="580ed-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="580ed-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="580ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="580ed-102">SYNOPSIS</span></span>
<span data-ttu-id="580ed-103">Возвращает конфигурацию пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="580ed-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="580ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="580ed-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="580ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="580ed-105">DESCRIPTION</span></span>
<span data-ttu-id="580ed-106">Командлет **Get-AzureRmExpressRouteCircuitPeeringConfig** извлекает конфигурацию однорангового отношения для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="580ed-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="580ed-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="580ed-107">EXAMPLES</span></span>

### <span data-ttu-id="580ed-108">Пример 1: отображение конфигурации пиринга для канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="580ed-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="580ed-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="580ed-109">PARAMETERS</span></span>

### <span data-ttu-id="580ed-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580ed-110">-DefaultProfile</span></span>
<span data-ttu-id="580ed-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="580ed-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580ed-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="580ed-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="580ed-113">Объект цепи ExpressRoute, который содержит конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="580ed-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="580ed-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="580ed-114">-Name</span></span>
<span data-ttu-id="580ed-115">Имя конфигурации пиринга, которую нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="580ed-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="580ed-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580ed-116">CommonParameters</span></span>
<span data-ttu-id="580ed-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="580ed-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580ed-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="580ed-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580ed-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="580ed-119">INPUTS</span></span>

### <span data-ttu-id="580ed-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="580ed-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="580ed-121">Параметры: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="580ed-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="580ed-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="580ed-122">OUTPUTS</span></span>

### <span data-ttu-id="580ed-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="580ed-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="580ed-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="580ed-124">NOTES</span></span>

## <span data-ttu-id="580ed-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="580ed-125">RELATED LINKS</span></span>

[<span data-ttu-id="580ed-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="580ed-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="580ed-127">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="580ed-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="580ed-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="580ed-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="580ed-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="580ed-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
