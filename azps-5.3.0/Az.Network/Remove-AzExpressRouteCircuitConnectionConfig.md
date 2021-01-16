---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507789"
---
# <span data-ttu-id="5f93b-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5f93b-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="5f93b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f93b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f93b-103">Удаляет конфигурацию подключения к каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5f93b-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="5f93b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5f93b-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f93b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f93b-105">DESCRIPTION</span></span>
<span data-ttu-id="5f93b-106">С **помощью cmdlet Remove-AzExpressRouteCircuitConnectionConfig** удаляется конфигурация подключения к каналу ExpressRoute, связанная с тем или иным каналом Express Route.</span><span class="sxs-lookup"><span data-stu-id="5f93b-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="5f93b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5f93b-107">EXAMPLES</span></span>

### <span data-ttu-id="5f93b-108">Пример 1. Удаление конфигурации подключения к каналу ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5f93b-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="5f93b-109">Пример 2. Удаление конфигурации подключения к каналу с помощью piping из схемы ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5f93b-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="5f93b-110">Пример 3. Удаление конфигурации подключения к каналу ExpressRoute для определенного семейства адресов</span><span class="sxs-lookup"><span data-stu-id="5f93b-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="5f93b-111">Пример 4. Удаление конфигурации подключения к каналу с помощью piping из схемы ExpressRoute для определенного семейства адресов</span><span class="sxs-lookup"><span data-stu-id="5f93b-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="5f93b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f93b-112">PARAMETERS</span></span>

### <span data-ttu-id="5f93b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f93b-113">-DefaultProfile</span></span>
<span data-ttu-id="5f93b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f93b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f93b-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f93b-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5f93b-116">Канал ExpressRoute, содержащий конфигурацию пиринга, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="5f93b-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="5f93b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5f93b-117">-Name</span></span>
<span data-ttu-id="5f93b-118">Имя удаляемой конфигурации подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="5f93b-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="5f93b-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="5f93b-119">-AddressPrefixType</span></span>
<span data-ttu-id="5f93b-120">Определяет семейство адресов, которое необходимо удалить из config.</span><span class="sxs-lookup"><span data-stu-id="5f93b-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f93b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f93b-121">-Confirm</span></span>
<span data-ttu-id="5f93b-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5f93b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f93b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f93b-123">-WhatIf</span></span>
<span data-ttu-id="5f93b-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f93b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f93b-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5f93b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f93b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f93b-126">CommonParameters</span></span>
<span data-ttu-id="5f93b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f93b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f93b-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f93b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f93b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f93b-129">INPUTS</span></span>

### <span data-ttu-id="5f93b-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f93b-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5f93b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f93b-131">OUTPUTS</span></span>

### <span data-ttu-id="5f93b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f93b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5f93b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5f93b-133">NOTES</span></span>

## <span data-ttu-id="5f93b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f93b-134">RELATED LINKS</span></span>

[<span data-ttu-id="5f93b-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f93b-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="5f93b-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5f93b-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5f93b-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5f93b-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5f93b-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5f93b-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5f93b-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5f93b-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="5f93b-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f93b-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="5f93b-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5f93b-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)