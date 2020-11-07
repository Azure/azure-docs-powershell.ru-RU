---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 187b7848dc3634ee67521e03f46f4684f23b9913
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913629"
---
# <span data-ttu-id="cca69-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cca69-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="cca69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cca69-102">SYNOPSIS</span></span>
<span data-ttu-id="cca69-103">Возвращает конфигурацию пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cca69-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cca69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cca69-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cca69-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cca69-105">DESCRIPTION</span></span>
<span data-ttu-id="cca69-106">Командлет **Get-AzureRmExpressRouteCircuitPeeringConfig** извлекает конфигурацию однорангового отношения для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="cca69-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="cca69-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cca69-107">EXAMPLES</span></span>

### <span data-ttu-id="cca69-108">Пример 1: отображение конфигурации пиринга для канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="cca69-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="cca69-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cca69-109">PARAMETERS</span></span>

### <span data-ttu-id="cca69-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca69-110">-DefaultProfile</span></span>
<span data-ttu-id="cca69-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cca69-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cca69-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cca69-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="cca69-113">Объект цепи ExpressRoute, который содержит конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="cca69-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cca69-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cca69-114">-Name</span></span>
<span data-ttu-id="cca69-115">Имя конфигурации пиринга, которую нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="cca69-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cca69-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca69-116">CommonParameters</span></span>
<span data-ttu-id="cca69-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cca69-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca69-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca69-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca69-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cca69-119">INPUTS</span></span>

### <span data-ttu-id="cca69-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cca69-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="cca69-121">Параметр "ExpressRouteCircuit" принимает значение типа "PSExpressRouteCircuit" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cca69-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="cca69-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cca69-122">OUTPUTS</span></span>

### <span data-ttu-id="cca69-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="cca69-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="cca69-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="cca69-124">NOTES</span></span>

## <span data-ttu-id="cca69-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cca69-125">RELATED LINKS</span></span>

[<span data-ttu-id="cca69-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cca69-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cca69-127">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cca69-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cca69-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="cca69-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="cca69-129">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="cca69-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
