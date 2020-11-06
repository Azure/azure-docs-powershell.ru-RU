---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 6524e69662f26a993bbc9cdf74eba71ff801f879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562839"
---
# <span data-ttu-id="63a04-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="63a04-101">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="63a04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63a04-102">SYNOPSIS</span></span>
<span data-ttu-id="63a04-103">Удаление конфигурации подключения к каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="63a04-103">Removes an ExpressRoute circuit connection configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63a04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63a04-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String>
 [-ExpressRouteCircuit] <PSExpressRouteCircuit> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63a04-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63a04-105">DESCRIPTION</span></span>
<span data-ttu-id="63a04-106">Командлет **Remove-AzureRmExpressRouteCircuitConnectionConfig** удаляет конфигурацию подключения к каналу ExpressRoute, связанную с данным каналом Express Route.</span><span class="sxs-lookup"><span data-stu-id="63a04-106">The **Remove-AzureRmExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="63a04-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63a04-107">EXAMPLES</span></span>

### <span data-ttu-id="63a04-108">Пример 1: Удаление конфигурации подключения к каналу из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="63a04-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="63a04-109">Пример 2: Удаление конфигурации подключения к каналу с помощью конвейера из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="63a04-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="63a04-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63a04-110">PARAMETERS</span></span>

### <span data-ttu-id="63a04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a04-111">-DefaultProfile</span></span>
<span data-ttu-id="63a04-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63a04-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63a04-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="63a04-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="63a04-114">Цепь ExpressRoute, содержащая конфигурацию пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="63a04-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63a04-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63a04-115">-Name</span></span>
<span data-ttu-id="63a04-116">Имя конфигурации подключения к каналу, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="63a04-116">The name of the circuit connection configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a04-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63a04-117">-Confirm</span></span>
<span data-ttu-id="63a04-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63a04-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a04-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63a04-119">-WhatIf</span></span>
<span data-ttu-id="63a04-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63a04-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63a04-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63a04-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a04-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a04-122">CommonParameters</span></span>
<span data-ttu-id="63a04-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63a04-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a04-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63a04-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a04-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63a04-125">INPUTS</span></span>

### <span data-ttu-id="63a04-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="63a04-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="63a04-127">Параметры: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="63a04-127">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="63a04-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63a04-128">OUTPUTS</span></span>

### <span data-ttu-id="63a04-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="63a04-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="63a04-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="63a04-130">NOTES</span></span>

## <span data-ttu-id="63a04-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63a04-131">RELATED LINKS</span></span>

[<span data-ttu-id="63a04-132">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="63a04-132">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="63a04-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="63a04-133">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="63a04-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="63a04-134">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Add-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="63a04-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="63a04-135">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="63a04-136">New-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="63a04-136">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="63a04-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="63a04-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="63a04-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="63a04-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
