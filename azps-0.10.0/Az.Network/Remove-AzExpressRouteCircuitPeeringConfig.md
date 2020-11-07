---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5feeba4ffb4f73365e9b6df86a03e8920b74f88e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909505"
---
# <span data-ttu-id="bb388-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="bb388-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="bb388-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb388-102">SYNOPSIS</span></span>
<span data-ttu-id="bb388-103">Удаление конфигурации пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bb388-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="bb388-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb388-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb388-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb388-105">DESCRIPTION</span></span>
<span data-ttu-id="bb388-106">Командлет **Remove-AzExpressRouteCircuitPeeringConfig** удаляет конфигурацию пиринга канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="bb388-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="bb388-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb388-107">EXAMPLES</span></span>

### <span data-ttu-id="bb388-108">Пример 1: Удаление конфигурации пиринга из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="bb388-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="bb388-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb388-109">PARAMETERS</span></span>

### <span data-ttu-id="bb388-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb388-110">-DefaultProfile</span></span>
<span data-ttu-id="bb388-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb388-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb388-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb388-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="bb388-113">Цепь ExpressRoute, содержащая конфигурацию пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bb388-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="bb388-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb388-114">-Name</span></span>
<span data-ttu-id="bb388-115">Имя конфигурации пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bb388-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="bb388-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="bb388-116">-PeerAddressType</span></span>
<span data-ttu-id="bb388-117">Семейство адресов пиринга</span><span class="sxs-lookup"><span data-stu-id="bb388-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="bb388-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb388-118">CommonParameters</span></span>
<span data-ttu-id="bb388-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb388-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb388-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb388-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb388-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb388-121">INPUTS</span></span>

### <span data-ttu-id="bb388-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb388-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="bb388-123">Параметр "ExpressRouteCircuit" принимает значение типа "PSExpressRouteCircuit" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bb388-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="bb388-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb388-124">OUTPUTS</span></span>

### <span data-ttu-id="bb388-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb388-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="bb388-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb388-126">NOTES</span></span>

## <span data-ttu-id="bb388-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb388-127">RELATED LINKS</span></span>

[<span data-ttu-id="bb388-128">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="bb388-128">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="bb388-129">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb388-129">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="bb388-130">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="bb388-130">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="bb388-131">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="bb388-131">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
