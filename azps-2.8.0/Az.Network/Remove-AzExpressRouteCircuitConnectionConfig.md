---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c596dffcef97dfbb1cabbc5ca2c2455a7768c25f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409942"
---
# <span data-ttu-id="e2c7e-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e2c7e-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="e2c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c7e-103">Удаляет конфигурацию подключения к каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="e2c7e-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="e2c7e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2c7e-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2c7e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="e2c7e-106">С **помощью cmdlet Remove-AzExpressRouteCircuitConnectionConfig** удаляется конфигурация подключения к каналу ExpressRoute, связанная с этим каналом Express Route.</span><span class="sxs-lookup"><span data-stu-id="e2c7e-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="e2c7e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2c7e-107">EXAMPLES</span></span>

### <span data-ttu-id="e2c7e-108">Пример 1. Удаление конфигурации подключения к каналу ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e2c7e-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="e2c7e-109">Пример 2. Удаление конфигурации подключения к каналу с помощью piping из схемы ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e2c7e-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="e2c7e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2c7e-110">PARAMETERS</span></span>

### <span data-ttu-id="e2c7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c7e-111">-DefaultProfile</span></span>
<span data-ttu-id="e2c7e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2c7e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2c7e-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2c7e-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="e2c7e-114">Канал ExpressRoute, содержащий конфигурацию пиринга, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e2c7e-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="e2c7e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e2c7e-115">-Name</span></span>
<span data-ttu-id="e2c7e-116">Имя удаляемой конфигурации подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="e2c7e-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="e2c7e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2c7e-117">-Confirm</span></span>
<span data-ttu-id="e2c7e-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e2c7e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2c7e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2c7e-119">-WhatIf</span></span>
<span data-ttu-id="e2c7e-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2c7e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2c7e-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e2c7e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2c7e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c7e-122">CommonParameters</span></span>
<span data-ttu-id="e2c7e-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2c7e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c7e-124">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2c7e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c7e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2c7e-125">INPUTS</span></span>

### <span data-ttu-id="e2c7e-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2c7e-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e2c7e-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2c7e-127">OUTPUTS</span></span>

### <span data-ttu-id="e2c7e-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2c7e-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e2c7e-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2c7e-129">NOTES</span></span>

## <span data-ttu-id="e2c7e-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2c7e-130">RELATED LINKS</span></span>

[<span data-ttu-id="e2c7e-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2c7e-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e2c7e-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e2c7e-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="e2c7e-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e2c7e-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="e2c7e-134">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2c7e-134">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="e2c7e-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e2c7e-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
