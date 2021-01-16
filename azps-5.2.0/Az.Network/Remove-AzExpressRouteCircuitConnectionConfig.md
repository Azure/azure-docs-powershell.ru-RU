---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414711"
---
# <span data-ttu-id="00a13-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="00a13-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="00a13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00a13-102">SYNOPSIS</span></span>
<span data-ttu-id="00a13-103">Удаляет конфигурацию подключения к каналу ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="00a13-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="00a13-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="00a13-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00a13-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00a13-105">DESCRIPTION</span></span>
<span data-ttu-id="00a13-106">С **помощью cmdlet Remove-AzExpressRouteCircuitConnectionConfig** удаляется конфигурация подключения к каналу ExpressRoute, связанная с тем или иным каналом Express Route.</span><span class="sxs-lookup"><span data-stu-id="00a13-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="00a13-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="00a13-107">EXAMPLES</span></span>

### <span data-ttu-id="00a13-108">Пример 1. Удаление конфигурации подключения к каналу ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="00a13-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="00a13-109">Пример 2. Удаление конфигурации подключения к каналу с помощью piping из схемы ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="00a13-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="00a13-110">Пример 3. Удаление конфигурации подключения к каналу ExpressRoute для определенного семейства адресов</span><span class="sxs-lookup"><span data-stu-id="00a13-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="00a13-111">Пример 4. Удаление конфигурации подключения к каналу с помощью piping из схемы ExpressRoute для определенного семейства адресов</span><span class="sxs-lookup"><span data-stu-id="00a13-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="00a13-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00a13-112">PARAMETERS</span></span>

### <span data-ttu-id="00a13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a13-113">-DefaultProfile</span></span>
<span data-ttu-id="00a13-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00a13-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00a13-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="00a13-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="00a13-116">Канал ExpressRoute, содержащий конфигурацию пиринга, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="00a13-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="00a13-117">-Name</span><span class="sxs-lookup"><span data-stu-id="00a13-117">-Name</span></span>
<span data-ttu-id="00a13-118">Имя удаляемой конфигурации подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="00a13-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="00a13-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="00a13-119">-AddressPrefixType</span></span>
<span data-ttu-id="00a13-120">Определяет семейство адресов, которое необходимо удалить из config.</span><span class="sxs-lookup"><span data-stu-id="00a13-120">Specifies the address family that needs to be removed from the config</span></span> 

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

### <span data-ttu-id="00a13-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00a13-121">-Confirm</span></span>
<span data-ttu-id="00a13-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00a13-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00a13-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00a13-123">-WhatIf</span></span>
<span data-ttu-id="00a13-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00a13-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00a13-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="00a13-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00a13-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a13-126">CommonParameters</span></span>
<span data-ttu-id="00a13-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00a13-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a13-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00a13-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a13-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00a13-129">INPUTS</span></span>

### <span data-ttu-id="00a13-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="00a13-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="00a13-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="00a13-131">OUTPUTS</span></span>

### <span data-ttu-id="00a13-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="00a13-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="00a13-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="00a13-133">NOTES</span></span>

## <span data-ttu-id="00a13-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00a13-134">RELATED LINKS</span></span>

[<span data-ttu-id="00a13-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="00a13-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="00a13-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="00a13-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="00a13-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="00a13-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="00a13-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="00a13-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="00a13-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="00a13-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="00a13-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="00a13-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="00a13-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="00a13-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)