---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bf69b628224baa74014d75b4c687a15d830d13c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730181"
---
# <span data-ttu-id="d7d6b-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d7d6b-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="d7d6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d6b-103">Удаление конфигурации подключения к каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="d7d6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7d6b-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7d6b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d6b-106">Командлет **Remove-AzExpressRouteCircuitConnectionConfig** удаляет конфигурацию подключения к каналу ExpressRoute, связанную с данным каналом Express Route.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="d7d6b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-107">EXAMPLES</span></span>

### <span data-ttu-id="d7d6b-108">Пример 1: Удаление конфигурации подключения к каналу из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d7d6b-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="d7d6b-109">Пример 2: Удаление конфигурации подключения к каналу с помощью конвейера из канала ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="d7d6b-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="d7d6b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-110">PARAMETERS</span></span>

### <span data-ttu-id="d7d6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d6b-111">-DefaultProfile</span></span>
<span data-ttu-id="d7d6b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7d6b-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d7d6b-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="d7d6b-114">Цепь ExpressRoute, содержащая конфигурацию пиринга, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="d7d6b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d7d6b-115">-Name</span></span>
<span data-ttu-id="d7d6b-116">Имя конфигурации подключения к каналу, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="d7d6b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7d6b-117">-Confirm</span></span>
<span data-ttu-id="d7d6b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d6b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d6b-119">-WhatIf</span></span>
<span data-ttu-id="d7d6b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7d6b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d6b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d6b-122">CommonParameters</span></span>
<span data-ttu-id="d7d6b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7d6b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d6b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d6b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d6b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7d6b-125">INPUTS</span></span>

### <span data-ttu-id="d7d6b-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d7d6b-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d7d6b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-127">OUTPUTS</span></span>

### <span data-ttu-id="d7d6b-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d7d6b-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d7d6b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7d6b-129">NOTES</span></span>

## <span data-ttu-id="d7d6b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7d6b-130">RELATED LINKS</span></span>

[<span data-ttu-id="d7d6b-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d7d6b-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="d7d6b-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d7d6b-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d7d6b-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d7d6b-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d7d6b-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d7d6b-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d7d6b-135">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="d7d6b-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="d7d6b-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d7d6b-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="d7d6b-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d7d6b-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)