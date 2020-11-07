---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 749f1b84ed033e903d3e50652e6199f184fffa2b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913589"
---
# <span data-ttu-id="927fc-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="927fc-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="927fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="927fc-102">SYNOPSIS</span></span>
<span data-ttu-id="927fc-103">Удаление конфигурации пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="927fc-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="927fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="927fc-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="927fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="927fc-105">DESCRIPTION</span></span>
<span data-ttu-id="927fc-106">Командлет **Remove-AzureRmExpressRouteCircuitPeeringConfig** удаляет конфигурацию пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="927fc-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="927fc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="927fc-107">EXAMPLES</span></span>

### <span data-ttu-id="927fc-108">Пример 1: Удаление конфигурации пиринга из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="927fc-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="927fc-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="927fc-109">PARAMETERS</span></span>

### <span data-ttu-id="927fc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="927fc-110">-DefaultProfile</span></span>
<span data-ttu-id="927fc-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="927fc-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="927fc-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="927fc-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="927fc-113">Цепь ExpressRoute, содержащая конфигурацию пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="927fc-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="927fc-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="927fc-114">-Name</span></span>
<span data-ttu-id="927fc-115">Имя конфигурации пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="927fc-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="927fc-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="927fc-116">-PeerAddressType</span></span>
<span data-ttu-id="927fc-117">Семейство адресов пиринга</span><span class="sxs-lookup"><span data-stu-id="927fc-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="927fc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927fc-118">CommonParameters</span></span>
<span data-ttu-id="927fc-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="927fc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927fc-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="927fc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927fc-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="927fc-121">INPUTS</span></span>

### <span data-ttu-id="927fc-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="927fc-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="927fc-123">Параметр "ExpressRouteCircuit" принимает значение типа "PSExpressRouteCircuit" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="927fc-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="927fc-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="927fc-124">OUTPUTS</span></span>

### <span data-ttu-id="927fc-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="927fc-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="927fc-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="927fc-126">NOTES</span></span>

## <span data-ttu-id="927fc-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="927fc-127">RELATED LINKS</span></span>

[<span data-ttu-id="927fc-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="927fc-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="927fc-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="927fc-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="927fc-130">New-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="927fc-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="927fc-131">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="927fc-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
