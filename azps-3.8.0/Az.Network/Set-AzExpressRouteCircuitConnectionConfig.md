---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065816"
---
# <span data-ttu-id="c835e-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c835e-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="c835e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c835e-102">SYNOPSIS</span></span>
<span data-ttu-id="c835e-103">Обновляет конфигурацию подключения к каналу, созданную в частных соединениях для канала Express Route.</span><span class="sxs-lookup"><span data-stu-id="c835e-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="c835e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c835e-104">SYNTAX</span></span>

### <span data-ttu-id="c835e-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c835e-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c835e-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c835e-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c835e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c835e-107">DESCRIPTION</span></span>
<span data-ttu-id="c835e-108">Командлет **Set-AzExpressRouteCircuitConnectionConfig** обновляет конфигурацию подключения к каналу, созданную в частном одноранговом соединении для канала ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c835e-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="c835e-109">Это позволяет одноранговые линии двух каналов Express для разных регионов или подписок.</span><span class="sxs-lookup"><span data-stu-id="c835e-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="c835e-110">Обратите внимание, что перед выполнением **Set-AzExpressRouteCircuitConnectionConfig** необходимо добавить подключение к каналу с помощью **Add-AzExpressRouteCircuitConnectionConfig**.</span><span class="sxs-lookup"><span data-stu-id="c835e-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="c835e-111">Кроме того, после выполнения **Set-AzExpressRouteCircuitPeeringConfig** необходимо вызвать командлет Set-AzExpressRouteCircuit для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c835e-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="c835e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c835e-112">EXAMPLES</span></span>

### <span data-ttu-id="c835e-113">Пример 1: Обновление ресурса соединения канала с существующей цепью ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c835e-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="c835e-114">Пример 2: Настройка подключения к каналу с использованием конвейера для существующей цепи ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c835e-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="c835e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c835e-115">PARAMETERS</span></span>

### <span data-ttu-id="c835e-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c835e-116">-AddressPrefix</span></span>
<span data-ttu-id="c835e-117">Минимальное/29 адресное пространство клиента для создания туннелей VxLan между цепями прямых маршрутов для туннелей IPv4.</span><span class="sxs-lookup"><span data-stu-id="c835e-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="c835e-118">или как минимум/125 адресного пространства клиента для создания туннелей VxLan между цепями прямых маршрутов для туннелей IPv6.</span><span class="sxs-lookup"><span data-stu-id="c835e-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="c835e-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="c835e-119">-AddressPrefixType</span></span>
<span data-ttu-id="c835e-120">Указывает семейство адресов, которому принадлежит префикс адреса.</span><span class="sxs-lookup"><span data-stu-id="c835e-120">Specifies the address family that address prefix belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: IPv4
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c835e-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="c835e-121">-AuthorizationKey</span></span>
<span data-ttu-id="c835e-122">Ключ авторизации для однорангового канала Express Route в другой подписке.</span><span class="sxs-lookup"><span data-stu-id="c835e-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="c835e-123">Авторизация в одноранговых каналах может быть создана с помощью существующих команд.</span><span class="sxs-lookup"><span data-stu-id="c835e-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="c835e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c835e-124">-DefaultProfile</span></span>
<span data-ttu-id="c835e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c835e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c835e-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c835e-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="c835e-127">Изменяемая цепь ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c835e-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="c835e-128">Это объект Azure, возвращенный командлетом **Get-AzExpressRouteCircuit** .</span><span class="sxs-lookup"><span data-stu-id="c835e-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="c835e-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c835e-129">-Name</span></span>
<span data-ttu-id="c835e-130">Имя добавляемого ресурса подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="c835e-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="c835e-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="c835e-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="c835e-132">Идентификатор ресурса для частного однорангового соединения удаленной цепи, который будет одноранговым с текущим каналом.</span><span class="sxs-lookup"><span data-stu-id="c835e-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="c835e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c835e-133">-Confirm</span></span>
<span data-ttu-id="c835e-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c835e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c835e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c835e-135">-WhatIf</span></span>
<span data-ttu-id="c835e-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c835e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c835e-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c835e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c835e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c835e-138">CommonParameters</span></span>
<span data-ttu-id="c835e-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c835e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c835e-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c835e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c835e-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c835e-141">INPUTS</span></span>

### <span data-ttu-id="c835e-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c835e-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="c835e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c835e-143">System.String</span></span>

## <span data-ttu-id="c835e-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c835e-144">OUTPUTS</span></span>

### <span data-ttu-id="c835e-145">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c835e-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="c835e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="c835e-146">NOTES</span></span>

## <span data-ttu-id="c835e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c835e-147">RELATED LINKS</span></span>

[<span data-ttu-id="c835e-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c835e-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c835e-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c835e-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c835e-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c835e-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="c835e-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c835e-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="c835e-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c835e-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
