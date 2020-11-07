---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: a3b5b20eac34076dd6a5490a5d9cf1a5e2c49684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903117"
---
# <span data-ttu-id="ba870-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ba870-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="ba870-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba870-102">SYNOPSIS</span></span>
<span data-ttu-id="ba870-103">Добавляет конфигурацию подключения к каналу в частный одноранговый канал Express Route.</span><span class="sxs-lookup"><span data-stu-id="ba870-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="ba870-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba870-104">SYNTAX</span></span>

### <span data-ttu-id="ba870-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba870-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba870-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba870-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba870-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba870-107">DESCRIPTION</span></span>
<span data-ttu-id="ba870-108">Командлет **Add-AzExpressRouteCircuitConnectionConfig** добавляет конфигурацию подключения к каналу в частный одноранговый канал для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ba870-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="ba870-109">Это позволяет одноранговые линии двух каналов Express для разных регионов или подписок. Обратите внимание, что после выполнения **Add-AzExpressRouteCircuitPeeringConfig** необходимо вызвать командлет Set-AzExpressRouteCircuit для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ba870-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="ba870-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba870-110">EXAMPLES</span></span>

### <span data-ttu-id="ba870-111">Пример 1: Добавление ресурса соединения канала в существующую цепь ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ba870-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="ba870-112">Пример 2: Добавление конфигурации подключения к каналу с помощью конвейера в существующую цепь ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="ba870-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="ba870-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba870-113">PARAMETERS</span></span>

### <span data-ttu-id="ba870-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ba870-114">-AddressPrefix</span></span>
<span data-ttu-id="ba870-115">Минимальное/29 адресное пространство клиента для создания туннелей VxLan между цепями прямых маршрутов</span><span class="sxs-lookup"><span data-stu-id="ba870-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba870-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="ba870-116">-AuthorizationKey</span></span>
<span data-ttu-id="ba870-117">Ключ авторизации для однорангового канала Express Route в другой подписке.</span><span class="sxs-lookup"><span data-stu-id="ba870-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="ba870-118">Авторизация в одноранговых каналах может быть создана с помощью существующих команд.</span><span class="sxs-lookup"><span data-stu-id="ba870-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="ba870-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba870-119">-DefaultProfile</span></span>
<span data-ttu-id="ba870-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba870-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba870-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ba870-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ba870-122">Изменяемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ba870-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="ba870-123">Это объект Azure, возвращенный командлетом **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="ba870-123">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="ba870-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba870-124">-Name</span></span>
<span data-ttu-id="ba870-125">Имя добавляемого ресурса подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="ba870-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="ba870-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="ba870-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="ba870-127">Идентификатор ресурса для частного однорангового соединения удаленной цепи, который будет одноранговым с текущим каналом.</span><span class="sxs-lookup"><span data-stu-id="ba870-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba870-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba870-128">-Confirm</span></span>
<span data-ttu-id="ba870-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba870-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba870-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba870-130">-WhatIf</span></span>
<span data-ttu-id="ba870-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba870-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba870-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba870-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba870-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba870-133">CommonParameters</span></span>
<span data-ttu-id="ba870-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba870-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba870-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba870-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba870-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba870-136">INPUTS</span></span>

### <span data-ttu-id="ba870-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ba870-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="ba870-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ba870-138">System.String</span></span>

## <span data-ttu-id="ba870-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba870-139">OUTPUTS</span></span>

### <span data-ttu-id="ba870-140">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ba870-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ba870-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba870-141">NOTES</span></span>

## <span data-ttu-id="ba870-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba870-142">RELATED LINKS</span></span>

[<span data-ttu-id="ba870-143">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ba870-143">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ba870-144">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ba870-144">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ba870-145">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ba870-145">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ba870-146">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ba870-146">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ba870-147">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="ba870-147">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="ba870-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ba870-148">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="ba870-149">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ba870-149">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)