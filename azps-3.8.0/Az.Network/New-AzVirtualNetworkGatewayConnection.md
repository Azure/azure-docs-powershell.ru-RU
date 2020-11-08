---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f6dc25bc1000466d853715f62e38237ddfc76aa2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073232"
---
# <span data-ttu-id="623cc-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="623cc-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="623cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="623cc-102">SYNOPSIS</span></span>
<span data-ttu-id="623cc-103">Создание подключения VPN между сайтами между шлюзом виртуальной сети и локальным устройством VPN.</span><span class="sxs-lookup"><span data-stu-id="623cc-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="623cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="623cc-104">SYNTAX</span></span>

### <span data-ttu-id="623cc-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="623cc-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="623cc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="623cc-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="623cc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="623cc-107">DESCRIPTION</span></span>
<span data-ttu-id="623cc-108">Создание подключения VPN между сайтами между шлюзом виртуальной сети и локальным устройством VPN.</span><span class="sxs-lookup"><span data-stu-id="623cc-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="623cc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="623cc-109">EXAMPLES</span></span>

### <span data-ttu-id="623cc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="623cc-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="623cc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="623cc-111">PARAMETERS</span></span>

### <span data-ttu-id="623cc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="623cc-112">-AsJob</span></span>
<span data-ttu-id="623cc-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="623cc-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="623cc-114">-AuthorizationKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="623cc-115">-ConnectionProtocol</span></span>
<span data-ttu-id="623cc-116">Протокол подключения к шлюзу: IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="623cc-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IKEv1, IKEv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="623cc-117">-ConnectionType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623cc-118">-DefaultProfile</span></span>
<span data-ttu-id="623cc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="623cc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="623cc-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="623cc-120">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="623cc-121">-ExpressRouteGatewayBypass</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="623cc-122">-Force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="623cc-123">-IpsecPolicies</span></span>
<span data-ttu-id="623cc-124">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="623cc-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="623cc-125">-LocalNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-126">-Location</span><span class="sxs-lookup"><span data-stu-id="623cc-126">-Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="623cc-127">-Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-128">-Peer</span><span class="sxs-lookup"><span data-stu-id="623cc-128">-Peer</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="623cc-129">-PeerId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623cc-130">-ResourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="623cc-131">-RoutingWeight</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="623cc-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="623cc-133">Таймаут обнаружения однорангового элемента для соединения в секундах</span><span class="sxs-lookup"><span data-stu-id="623cc-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="623cc-134">-SharedKey</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="623cc-135">-Tag</span></span>
<span data-ttu-id="623cc-136">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="623cc-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="623cc-137">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="623cc-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-138">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="623cc-138">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="623cc-139">Список политик выбора трафика.</span><span class="sxs-lookup"><span data-stu-id="623cc-139">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-140">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="623cc-140">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="623cc-141">Следует ли использовать PrivateIP для этого туннеля VPN на S2S</span><span class="sxs-lookup"><span data-stu-id="623cc-141">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-142">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="623cc-142">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="623cc-143">Использование селекторов трафика на основе политики для подключения S2S</span><span class="sxs-lookup"><span data-stu-id="623cc-143">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-144">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="623cc-144">-VirtualNetworkGateway1</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-145">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="623cc-145">-VirtualNetworkGateway2</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="623cc-146">-Confirm</span></span>
<span data-ttu-id="623cc-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="623cc-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="623cc-148">-WhatIf</span></span>
<span data-ttu-id="623cc-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="623cc-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="623cc-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="623cc-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623cc-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623cc-151">CommonParameters</span></span>
<span data-ttu-id="623cc-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="623cc-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623cc-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="623cc-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623cc-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="623cc-154">INPUTS</span></span>

### <span data-ttu-id="623cc-155">System. String</span><span class="sxs-lookup"><span data-stu-id="623cc-155">System.String</span></span>

### <span data-ttu-id="623cc-156">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="623cc-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="623cc-157">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="623cc-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="623cc-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="623cc-158">System.Int32</span></span>

### <span data-ttu-id="623cc-159">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="623cc-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="623cc-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="623cc-160">System.Boolean</span></span>

### <span data-ttu-id="623cc-161">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="623cc-161">System.Collections.Hashtable</span></span>

### <span data-ttu-id="623cc-162">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="623cc-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="623cc-163">Microsoft. Azure. Commands. Network. Models. PSTrafficSelectorPolicy []</span><span class="sxs-lookup"><span data-stu-id="623cc-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="623cc-164">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="623cc-164">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="623cc-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="623cc-165">OUTPUTS</span></span>

### <span data-ttu-id="623cc-166">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="623cc-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="623cc-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="623cc-167">NOTES</span></span>

## <span data-ttu-id="623cc-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="623cc-168">RELATED LINKS</span></span>

[<span data-ttu-id="623cc-169">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="623cc-169">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="623cc-170">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="623cc-170">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="623cc-171">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="623cc-171">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
