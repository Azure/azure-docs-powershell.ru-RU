---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8b4a8c9f-874c-4a27-b87e-c8ad7e73188d
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 432af4d97f2ddf085d23db33cc0f2604c1fc7aa5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517993"
---
# <span data-ttu-id="f48c7-101">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f48c7-101">Set-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="f48c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f48c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f48c7-103">Обновляет конфигурацию подключения к каналу, созданную в частных пирингах для express Route Circuit.</span><span class="sxs-lookup"><span data-stu-id="f48c7-103">Updates a circuit connection configuration created in Private Peerings for an Express Route Circuit.</span></span> 

## <span data-ttu-id="f48c7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f48c7-104">SYNTAX</span></span>

### <span data-ttu-id="f48c7-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f48c7-105">SetByResource (Default)</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-AddressPrefix] <String> [-AddressPrefixType <String>] [-AuthorizationKey <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f48c7-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f48c7-106">SetByResourceId</span></span>
```
Set-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-PeerExpressRouteCircuitPeering] <String> [-AddressPrefix] <String> -[AddressPrefixType <String>] [-AuthorizationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f48c7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f48c7-107">DESCRIPTION</span></span>
<span data-ttu-id="f48c7-108">Cmdlet **Set-AzExpressRouteCircuitConnectionConfig** обновляет конфигурацию подключения к каналу, созданному в частном пиринге для схемы ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f48c7-108">The **Set-AzExpressRouteCircuitConnectionConfig** cmdlet updates a circuit connection configuration created in private peering for an ExpressRoute circuit.</span></span> <span data-ttu-id="f48c7-109">Это позволяет пиринг двух каналов Express Route в разных регионах или подписках.</span><span class="sxs-lookup"><span data-stu-id="f48c7-109">This allows peering two Express Route Circuits across regions or subscriptions.</span></span>
<span data-ttu-id="f48c7-110">Обратите внимание, что перед запуском **Set-AzExpressRouteCircuitConnectionConfig** необходимо добавить подключение к каналу с помощью **Add-AzExpressRouteCircuitConnectionConfig.**</span><span class="sxs-lookup"><span data-stu-id="f48c7-110">Note that, before running **Set-AzExpressRouteCircuitConnectionConfig** you must add the circuit connection using **Add-AzExpressRouteCircuitConnectionConfig**.</span></span> <span data-ttu-id="f48c7-111">Кроме того, после запуска **Set-AzExpressRouteCircuitPeeringConfig** необходимо вызвать Set-AzExpressRouteCircuit для активации конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f48c7-111">Also, after running **Set-AzExpressRouteCircuitPeeringConfig**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the configuration.</span></span>


## <span data-ttu-id="f48c7-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f48c7-112">EXAMPLES</span></span>

### <span data-ttu-id="f48c7-113">Пример 1. Обновление ресурса подключения к каналу с существующим каналом ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f48c7-113">Example 1: Update a circuit connection resource to an existing ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = 'aa:bb::0/125'
$addressPrefixType = 'IPv6'
Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AddressPrefixType $addressPrefixType -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="f48c7-114">Пример 2. Настройка конфигурации подключения к каналу с помощью piping на существующем канале ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="f48c7-114">Example 2: Set a circuit connection configuration using Piping to an existing ExpressRoute Circuit</span></span>
```
$circuit_peer = Get-AzExpressRouteCircuit -Name $peeringCircuitName -ResourceGroupName $rg
$addressSpace = '60.0.0.0/29'
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Set-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -PeerExpressRouteCircuitPeering $circuit_peer.Peerings[0].Id -AddressPrefix $addressSpace -AuthorizationKey $circuit_peer.Authorizations[0].AuthorizationKey |Set-AzExpressRouteCircuit
```

## <span data-ttu-id="f48c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f48c7-115">PARAMETERS</span></span>

### <span data-ttu-id="f48c7-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f48c7-116">-AddressPrefix</span></span>
<span data-ttu-id="f48c7-117">Минимальное /29 адресное пространство для создания VxLan-туннельов между каналами express route для IPv4-каналов.</span><span class="sxs-lookup"><span data-stu-id="f48c7-117">A minimum /29 customer address space to create VxLan tunnels between Express Route Circuits for IPv4 tunnels.</span></span>
<span data-ttu-id="f48c7-118">или не менее /125 адресного пространства для создания VxLan-каналов между каналами Express Route для IPv6-каналов.</span><span class="sxs-lookup"><span data-stu-id="f48c7-118">or a minimum of /125 customer address space to create VxLan tunnels between Express Route Circuits for IPv6 tunnels.</span></span>

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
### <span data-ttu-id="f48c7-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="f48c7-119">-AddressPrefixType</span></span>
<span data-ttu-id="f48c7-120">Определяет семейство адресов, к которой принадлежит префикс адреса.</span><span class="sxs-lookup"><span data-stu-id="f48c7-120">Specifies the address family that address prefix belongs to.</span></span>

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

### <span data-ttu-id="f48c7-121">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="f48c7-121">-AuthorizationKey</span></span>
<span data-ttu-id="f48c7-122">Ключ авторизации для одноранговой схемы Express Route в другой подписке.</span><span class="sxs-lookup"><span data-stu-id="f48c7-122">Authorization Key to peer Express Route Circuit in another subscription.</span></span> <span data-ttu-id="f48c7-123">Авторизацию в одноранговом канале можно создать с помощью существующих команд.</span><span class="sxs-lookup"><span data-stu-id="f48c7-123">Authorization on peer circuit can be created using existing commands.</span></span>

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

### <span data-ttu-id="f48c7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48c7-124">-DefaultProfile</span></span>
<span data-ttu-id="f48c7-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f48c7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f48c7-126">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f48c7-126">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f48c7-127">Канал ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f48c7-127">The ExpressRoute circuit being modified.</span></span> <span data-ttu-id="f48c7-128">Это объект Azure, возвращенный **cmdlet Get-AzExpressRouteCircuit.**</span><span class="sxs-lookup"><span data-stu-id="f48c7-128">This is Azure object returned by the **Get-AzExpressRouteCircuit** cmdlet.</span></span>

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

### <span data-ttu-id="f48c7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f48c7-129">-Name</span></span>
<span data-ttu-id="f48c7-130">Имя добавляемого ресурса подключения к каналу.</span><span class="sxs-lookup"><span data-stu-id="f48c7-130">The name of the circuit connection resource to be added.</span></span>

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

### <span data-ttu-id="f48c7-131">-PeerExpressRouteCircuitPeering</span><span class="sxs-lookup"><span data-stu-id="f48c7-131">-PeerExpressRouteCircuitPeering</span></span>
<span data-ttu-id="f48c7-132">ИД ресурса для личного пиринга удаленного канала, который будет пирингом текущего.</span><span class="sxs-lookup"><span data-stu-id="f48c7-132">Resource Id for Private Peering of remote circuit which will be peered with the current circuit.</span></span>

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

### <span data-ttu-id="f48c7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f48c7-133">-Confirm</span></span>
<span data-ttu-id="f48c7-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f48c7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f48c7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f48c7-135">-WhatIf</span></span>
<span data-ttu-id="f48c7-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f48c7-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f48c7-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f48c7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f48c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48c7-138">CommonParameters</span></span>
<span data-ttu-id="f48c7-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48c7-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f48c7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48c7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f48c7-141">INPUTS</span></span>

### <span data-ttu-id="f48c7-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f48c7-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

### <span data-ttu-id="f48c7-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f48c7-143">System.String</span></span>

## <span data-ttu-id="f48c7-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f48c7-144">OUTPUTS</span></span>

### <span data-ttu-id="f48c7-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f48c7-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f48c7-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f48c7-146">NOTES</span></span>

## <span data-ttu-id="f48c7-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f48c7-147">RELATED LINKS</span></span>

[<span data-ttu-id="f48c7-148">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f48c7-148">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f48c7-149">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f48c7-149">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f48c7-150">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="f48c7-150">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="f48c7-151">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f48c7-151">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="f48c7-152">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f48c7-152">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
