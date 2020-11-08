---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244095"
---
# <span data-ttu-id="aa571-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="aa571-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="aa571-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa571-102">SYNOPSIS</span></span>
<span data-ttu-id="aa571-103">Удаление конфигурации пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="aa571-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="aa571-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa571-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa571-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa571-105">DESCRIPTION</span></span>
<span data-ttu-id="aa571-106">Командлет **Remove-AzExpressRouteCircuitPeeringConfig** удаляет конфигурацию пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="aa571-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="aa571-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa571-107">EXAMPLES</span></span>

### <span data-ttu-id="aa571-108">Пример 1: Удаление конфигурации пиринга из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="aa571-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="aa571-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa571-109">PARAMETERS</span></span>

### <span data-ttu-id="aa571-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa571-110">-DefaultProfile</span></span>
<span data-ttu-id="aa571-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa571-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa571-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aa571-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="aa571-113">Цепь ExpressRoute, содержащая конфигурацию пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="aa571-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="aa571-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa571-114">-Name</span></span>
<span data-ttu-id="aa571-115">Имя конфигурации пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="aa571-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="aa571-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="aa571-116">-PeerAddressType</span></span>
<span data-ttu-id="aa571-117">Семейство адресов пиринга</span><span class="sxs-lookup"><span data-stu-id="aa571-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa571-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa571-118">CommonParameters</span></span>
<span data-ttu-id="aa571-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa571-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa571-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa571-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa571-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa571-121">INPUTS</span></span>

### <span data-ttu-id="aa571-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aa571-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="aa571-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa571-123">OUTPUTS</span></span>

### <span data-ttu-id="aa571-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aa571-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="aa571-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa571-125">NOTES</span></span>

## <span data-ttu-id="aa571-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa571-126">RELATED LINKS</span></span>

[<span data-ttu-id="aa571-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="aa571-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="aa571-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aa571-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="aa571-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="aa571-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="aa571-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aa571-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
