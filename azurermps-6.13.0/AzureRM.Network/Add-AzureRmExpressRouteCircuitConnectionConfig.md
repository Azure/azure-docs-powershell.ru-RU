---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: aab4e78cd01e814ed8eb81b820e20bd3da4c03f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568490"
---
# <span data-ttu-id="aeb1b-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="aeb1b-101">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="aeb1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aeb1b-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb1b-103">Добавляет конфигурацию подключения к каналу в частный одноранговый канал Express Route.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeb1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aeb1b-104">SYNTAX</span></span>

### <span data-ttu-id="aeb1b-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aeb1b-105">SetByResource (Default)</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeb1b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aeb1b-106">SetByResourceId</span></span>
```
Add-AzureRmExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeb1b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeb1b-107">DESCRIPTION</span></span>
<span data-ttu-id="aeb1b-108">Командлет **Add-AzureRmExpressRouteCircuitConnectionConfig** добавляет конфигурацию подключения к каналу в частный одноранговый канал для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-108">The **Add-AzureRmExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="aeb1b-109">Это позволяет одноранговые линии двух каналов Express для разных регионов или подписок. Обратите внимание, что после выполнения **Add-AzureRmExpressRouteCircuitPeeringConfig** необходимо вызвать командлет Set-AzureRmExpressRouteCircuit для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzureRmExpressRouteCircuitPeeringConfig** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="aeb1b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aeb1b-110">EXAMPLES</span></span>

### <span data-ttu-id="aeb1b-111">Пример 1: Добавление ресурса соединения канала в существующую цепь ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="aeb1b-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="aeb1b-112">Пример 2: Добавление конфигурации подключения к каналу с помощью конвейера в существующую цепь ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="aeb1b-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzureRmExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzureRmExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzureRmExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="aeb1b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aeb1b-113">PARAMETERS</span></span>

### <span data-ttu-id="aeb1b-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="aeb1b-114">-AddressPrefix</span></span>
<span data-ttu-id="aeb1b-115">Минимальное/29 адресное пространство клиента для создания туннелей VxLan между цепями прямых маршрутов</span><span class="sxs-lookup"><span data-stu-id="aeb1b-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits</span></span>

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

### <span data-ttu-id="aeb1b-116">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="aeb1b-116">-AuthorizationKey</span></span>
<span data-ttu-id="aeb1b-117">Ключ авторизации для однорангового канала Express Route в другой подписке.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-117">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="aeb1b-118">Авторизация в одноранговых каналах может быть создана с помощью существующих команд.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-118">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="aeb1b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb1b-119">-DefaultProfile</span></span>
<span data-ttu-id="aeb1b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeb1b-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aeb1b-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="aeb1b-122">Изменяемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-122">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="aeb1b-123">Это объект Azure, возвращенный командлетом **Get-AzureRmExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="aeb1b-123">This is Azure object returned by the **Get-AzureRmExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="aeb1b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aeb1b-124">-Name</span></span>
<span data-ttu-id="aeb1b-125">Имя добавляемого ресурса подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-125">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="aeb1b-126">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="aeb1b-126">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="aeb1b-127">Идентификатор ресурса для частного однорангового соединения удаленной цепи, который будет одноранговым с текущим каналом.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-127">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="aeb1b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aeb1b-128">-Confirm</span></span>
<span data-ttu-id="aeb1b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeb1b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeb1b-130">-WhatIf</span></span>
<span data-ttu-id="aeb1b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeb1b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeb1b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb1b-133">CommonParameters</span></span>
<span data-ttu-id="aeb1b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aeb1b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb1b-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb1b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb1b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aeb1b-136">INPUTS</span></span>

### <span data-ttu-id="aeb1b-137">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aeb1b-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="aeb1b-138">Параметры: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aeb1b-138">Parameters: ExpressRouteCircuit (ByValue)</span></span>

### <span data-ttu-id="aeb1b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="aeb1b-139">System.String</span></span>

## <span data-ttu-id="aeb1b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aeb1b-140">OUTPUTS</span></span>

### <span data-ttu-id="aeb1b-141">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aeb1b-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="aeb1b-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="aeb1b-142">NOTES</span></span>

## <span data-ttu-id="aeb1b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aeb1b-143">RELATED LINKS</span></span>

[<span data-ttu-id="aeb1b-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aeb1b-144">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="aeb1b-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="aeb1b-145">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Get-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="aeb1b-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="aeb1b-146">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Remove-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="aeb1b-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="aeb1b-147">Set-AzureRmExpressRouteCircuitConnectionConfig</span></span>](Set-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="aeb1b-148">New-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="aeb1b-148">New-AzureRmExpressRouteCircuitConnectionConfig</span></span>](New-AzureRmExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="aeb1b-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aeb1b-149">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="aeb1b-150">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="aeb1b-150">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)
