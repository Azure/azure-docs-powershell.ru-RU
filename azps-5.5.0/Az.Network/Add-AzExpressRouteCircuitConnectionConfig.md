---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7b4a8c9f-874c-4a27-b87e-c8ad7e73188d
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: e8691d31956e1ee59f692cc3d37fa1e2d5598efa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214009"
---
# <span data-ttu-id="2a066-101">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2a066-101">Add-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="2a066-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a066-102">SYNOPSIS</span></span>
<span data-ttu-id="2a066-103">Добавляет конфигурацию подключения к каналу express Route в частном пиринге.</span><span class="sxs-lookup"><span data-stu-id="2a066-103">Adds a circuit connection configuration to Private Peering of an Express Route Circuit.</span></span> 

## <span data-ttu-id="2a066-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a066-104">SYNTAX</span></span>

### <span data-ttu-id="2a066-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a066-105">SetByResource (Default)</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a066-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a066-106">SetByResourceId</span></span>
```
Add-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a066-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a066-107">DESCRIPTION</span></span>
<span data-ttu-id="2a066-108">Cmdlet **Add-AzExpressRouteCircuitConnectionConfig** добавляет конфигурацию подключения к частному пирингу для каналов ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2a066-108">The **Add-AzExpressRouteCircuitConnectionConfig** cmdlet adds a circuit connection configuration to private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="2a066-109">Это позволяет пиринг двух каналов Express Route в разных регионах или подписках. Обратите внимание, что после запуска **Add-AzExpressRouteCircuitConnectionConfig** необходимо вызвать Set-AzExpressRouteCircuit для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2a066-109">This allows peering two Express Route Circuits across regions or subscriptions.Note that, after running **Add-AzExpressRouteCircuitConnectionConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="2a066-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a066-110">EXAMPLES</span></span>

### <span data-ttu-id="2a066-111">Пример 1. Добавление ресурса подключения к каналу ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2a066-111">Example 1: Add a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
$addressPrefixType = 'IPv4'
Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="2a066-112">Пример 2. Добавление конфигурации подключения к каналу с помощью Piping в существующем канале ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2a066-112">Example 2: Add a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Add-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="2a066-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a066-113">PARAMETERS</span></span>

### <span data-ttu-id="2a066-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2a066-114">-AddressPrefix</span></span>
<span data-ttu-id="2a066-115">Минимальное /29 адресное пространство для создания VxLan-туннельов между каналами express route для IPv4-каналов.</span><span class="sxs-lookup"><span data-stu-id="2a066-115">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="2a066-116">или не менее /125 адресного пространства для создания VxLan-каналов между каналами express route для IPv6-каналов.</span><span class="sxs-lookup"><span data-stu-id="2a066-116">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="2a066-117">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="2a066-117">-AddressPrefixType</span></span>
<span data-ttu-id="2a066-118">Эта определяет семейство адресов, к которой принадлежит префикс адреса.</span><span class="sxs-lookup"><span data-stu-id="2a066-118">This specifies the Address Family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="2a066-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="2a066-119">-AuthorizationKey</span></span>
<span data-ttu-id="2a066-120">Ключ авторизации для одноранговой схемы Express Route в другой подписке.</span><span class="sxs-lookup"><span data-stu-id="2a066-120">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="2a066-121">Авторизацию в одноранговом канале можно создать с помощью существующих команд.</span><span class="sxs-lookup"><span data-stu-id="2a066-121">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="2a066-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a066-122">-DefaultProfile</span></span>
<span data-ttu-id="2a066-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a066-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a066-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2a066-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2a066-125">Канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2a066-125">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="2a066-126">Это объект Azure, возвращенный **cmdlet Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="2a066-126">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="2a066-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2a066-127">-Name</span></span>
<span data-ttu-id="2a066-128">Имя добавляемого ресурса подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="2a066-128">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="2a066-129">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="2a066-129">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="2a066-130">ИД ресурса для личного пиринга удаленного канала, который будет пирингом текущего.</span><span class="sxs-lookup"><span data-stu-id="2a066-130">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="2a066-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a066-131">-Confirm</span></span>
<span data-ttu-id="2a066-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2a066-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a066-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a066-133">-WhatIf</span></span>
<span data-ttu-id="2a066-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a066-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a066-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a066-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a066-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a066-136">CommonParameters</span></span>
<span data-ttu-id="2a066-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a066-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a066-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a066-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a066-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a066-139">INPUTS</span></span>

### <span data-ttu-id="2a066-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2a066-140">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="2a066-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2a066-141">System.String</span></span>

## <span data-ttu-id="2a066-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a066-142">OUTPUTS</span></span>

### <span data-ttu-id="2a066-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2a066-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2a066-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a066-144">NOTES</span></span>

## <span data-ttu-id="2a066-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a066-145">RELATED LINKS</span></span>

[<span data-ttu-id="2a066-146">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2a066-146">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="2a066-147">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2a066-147">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="2a066-148">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2a066-148">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="2a066-149">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2a066-149">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="2a066-150">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2a066-150">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)