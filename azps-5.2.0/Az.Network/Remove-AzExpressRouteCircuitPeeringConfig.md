---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414700"
---
# <span data-ttu-id="973ca-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="973ca-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="973ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="973ca-102">SYNOPSIS</span></span>
<span data-ttu-id="973ca-103">Удаляет конфигурацию пиринга каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="973ca-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="973ca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="973ca-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="973ca-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="973ca-105">DESCRIPTION</span></span>
<span data-ttu-id="973ca-106">Для удаления конфигурации пиринга каналов ExpressRoute удаляется cmdlet **Remove-AzExpressRouteCircuitPeeringConfig.**</span><span class="sxs-lookup"><span data-stu-id="973ca-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="973ca-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="973ca-107">EXAMPLES</span></span>

### <span data-ttu-id="973ca-108">Пример 1. Удаление конфигурации пиринга из схемы ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="973ca-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="973ca-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="973ca-109">PARAMETERS</span></span>

### <span data-ttu-id="973ca-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973ca-110">-DefaultProfile</span></span>
<span data-ttu-id="973ca-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="973ca-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="973ca-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="973ca-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="973ca-113">Канал ExpressRoute, содержащий конфигурацию пиринга, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="973ca-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="973ca-114">-Name</span><span class="sxs-lookup"><span data-stu-id="973ca-114">-Name</span></span>
<span data-ttu-id="973ca-115">Имя удаляемой конфигурации пиринга.</span><span class="sxs-lookup"><span data-stu-id="973ca-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="973ca-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="973ca-116">-PeerAddressType</span></span>
<span data-ttu-id="973ca-117">Семейство адресов пиринга</span><span class="sxs-lookup"><span data-stu-id="973ca-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="973ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973ca-118">CommonParameters</span></span>
<span data-ttu-id="973ca-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="973ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973ca-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="973ca-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973ca-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="973ca-121">INPUTS</span></span>

### <span data-ttu-id="973ca-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="973ca-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="973ca-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="973ca-123">OUTPUTS</span></span>

### <span data-ttu-id="973ca-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="973ca-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="973ca-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="973ca-125">NOTES</span></span>

## <span data-ttu-id="973ca-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="973ca-126">RELATED LINKS</span></span>

[<span data-ttu-id="973ca-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="973ca-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="973ca-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="973ca-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="973ca-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="973ca-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="973ca-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="973ca-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
