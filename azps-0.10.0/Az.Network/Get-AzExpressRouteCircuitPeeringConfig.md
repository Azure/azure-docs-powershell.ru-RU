---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9c52ff23d4e92af0d1f62cdfc5d5fda01b3221da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910002"
---
# <span data-ttu-id="367e8-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="367e8-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="367e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="367e8-102">SYNOPSIS</span></span>
<span data-ttu-id="367e8-103">Возвращает конфигурацию пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="367e8-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="367e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="367e8-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="367e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="367e8-105">DESCRIPTION</span></span>
<span data-ttu-id="367e8-106">Командлет **Get-AzExpressRouteCircuitPeeringConfig** извлекает конфигурацию однорангового отношения для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="367e8-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="367e8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="367e8-107">EXAMPLES</span></span>

### <span data-ttu-id="367e8-108">Пример 1: отображение конфигурации пиринга для канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="367e8-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="367e8-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="367e8-109">PARAMETERS</span></span>

### <span data-ttu-id="367e8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367e8-110">-DefaultProfile</span></span>
<span data-ttu-id="367e8-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="367e8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="367e8-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="367e8-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="367e8-113">Объект цепи ExpressRoute, который содержит конфигурацию пиринга.</span><span class="sxs-lookup"><span data-stu-id="367e8-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="367e8-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="367e8-114">-Name</span></span>
<span data-ttu-id="367e8-115">Имя конфигурации пиринга, которую нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="367e8-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="367e8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367e8-116">CommonParameters</span></span>
<span data-ttu-id="367e8-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="367e8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367e8-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367e8-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367e8-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="367e8-119">INPUTS</span></span>

### <span data-ttu-id="367e8-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="367e8-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="367e8-121">Параметр "ExpressRouteCircuit" принимает значение типа "PSExpressRouteCircuit" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="367e8-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="367e8-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="367e8-122">OUTPUTS</span></span>

### <span data-ttu-id="367e8-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="367e8-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="367e8-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="367e8-124">NOTES</span></span>

## <span data-ttu-id="367e8-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="367e8-125">RELATED LINKS</span></span>

[<span data-ttu-id="367e8-126">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="367e8-126">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="367e8-127">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="367e8-127">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="367e8-128">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="367e8-128">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="367e8-129">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="367e8-129">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
