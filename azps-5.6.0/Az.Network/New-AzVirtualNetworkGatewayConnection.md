---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 78adeb351c0b18fe8ca7e3c3a2d286abe2f97400
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977843"
---
# <span data-ttu-id="32eb3-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="32eb3-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="32eb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="32eb3-103">Создает VPN-подключение "сайт-сайт" между виртуальным сетевым шлюзом и мобильным VPN-устройством.</span><span class="sxs-lookup"><span data-stu-id="32eb3-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="32eb3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32eb3-104">SYNTAX</span></span>

### <span data-ttu-id="32eb3-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32eb3-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-Peer <PSPeering>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] 
 [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32eb3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="32eb3-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-DpdTimeoutInSeconds <Int32>] [-ConnectionMode <String>] [-SharedKey <String>]
 [-PeerId <String>] [-EnableBgp <Boolean>] [-UseLocalAzureIpAddress] [-Tag <Hashtable>] [-Force]
 [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>]
 [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-ConnectionProtocol <String>] [-AsJob]
 [-ExpressRouteGatewayBypass] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32eb3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32eb3-107">DESCRIPTION</span></span>
<span data-ttu-id="32eb3-108">Создает VPN-подключение "сайт-сайт" между виртуальным сетевым шлюзом и мобильным VPN-устройством.</span><span class="sxs-lookup"><span data-stu-id="32eb3-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="32eb3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32eb3-109">EXAMPLES</span></span>

### <span data-ttu-id="32eb3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="32eb3-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="32eb3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32eb3-111">PARAMETERS</span></span>

### <span data-ttu-id="32eb3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32eb3-112">-AsJob</span></span>
<span data-ttu-id="32eb3-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="32eb3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32eb3-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="32eb3-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="32eb3-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="32eb3-115">-ConnectionProtocol</span></span>
<span data-ttu-id="32eb3-116">Протокол подключения шлюза:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="32eb3-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="32eb3-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="32eb3-117">-ConnectionType</span></span>

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

### <span data-ttu-id="32eb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32eb3-118">-DefaultProfile</span></span>
<span data-ttu-id="32eb3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32eb3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32eb3-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="32eb3-120">-EnableBgp</span></span>

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

### <span data-ttu-id="32eb3-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="32eb3-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="32eb3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="32eb3-122">-Force</span></span>

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

### <span data-ttu-id="32eb3-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="32eb3-123">-IpsecPolicies</span></span>
<span data-ttu-id="32eb3-124">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="32eb3-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="32eb3-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="32eb3-125">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="32eb3-126">-Location</span><span class="sxs-lookup"><span data-stu-id="32eb3-126">-Location</span></span>

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

### <span data-ttu-id="32eb3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="32eb3-127">-Name</span></span>

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

### <span data-ttu-id="32eb3-128">-Peer</span><span class="sxs-lookup"><span data-stu-id="32eb3-128">-Peer</span></span>

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

### <span data-ttu-id="32eb3-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="32eb3-129">-PeerId</span></span>

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

### <span data-ttu-id="32eb3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32eb3-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="32eb3-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="32eb3-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="32eb3-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="32eb3-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="32eb3-133">Время обнаружения за считанные секунды при обнаружении неавтных подключений</span><span class="sxs-lookup"><span data-stu-id="32eb3-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="32eb3-134">-ConnectionMode</span><span class="sxs-lookup"><span data-stu-id="32eb3-134">-ConnectionMode</span></span>
<span data-ttu-id="32eb3-135">Режим подключения виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="32eb3-135">Virtual Network Gateway Connection Mode</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: Default
Accept wildcard characters: False
```

### <span data-ttu-id="32eb3-136">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="32eb3-136">-SharedKey</span></span>

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

### <span data-ttu-id="32eb3-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="32eb3-137">-Tag</span></span>
<span data-ttu-id="32eb3-138">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="32eb3-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="32eb3-139">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="32eb3-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="32eb3-140">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="32eb3-140">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="32eb3-141">Список политик выбора трафика.</span><span class="sxs-lookup"><span data-stu-id="32eb3-141">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="32eb3-142">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="32eb3-142">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="32eb3-143">Следует ли использовать PrivateIP для этого VPN-туннель S2S</span><span class="sxs-lookup"><span data-stu-id="32eb3-143">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

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

### <span data-ttu-id="32eb3-144">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="32eb3-144">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="32eb3-145">Использование селекторов трафика на основе политик для подключения S2S</span><span class="sxs-lookup"><span data-stu-id="32eb3-145">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="32eb3-146">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="32eb3-146">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="32eb3-147">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="32eb3-147">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="32eb3-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32eb3-148">-Confirm</span></span>
<span data-ttu-id="32eb3-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32eb3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32eb3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32eb3-150">-WhatIf</span></span>
<span data-ttu-id="32eb3-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32eb3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32eb3-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="32eb3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32eb3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32eb3-153">CommonParameters</span></span>
<span data-ttu-id="32eb3-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32eb3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32eb3-155">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32eb3-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32eb3-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32eb3-156">INPUTS</span></span>

### <span data-ttu-id="32eb3-157">System.String</span><span class="sxs-lookup"><span data-stu-id="32eb3-157">System.String</span></span>

### <span data-ttu-id="32eb3-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="32eb3-158">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="32eb3-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="32eb3-159">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="32eb3-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="32eb3-160">System.Int32</span></span>

### <span data-ttu-id="32eb3-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="32eb3-161">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="32eb3-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32eb3-162">System.Boolean</span></span>

### <span data-ttu-id="32eb3-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="32eb3-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="32eb3-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="32eb3-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="32eb3-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="32eb3-165">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="32eb3-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="32eb3-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="32eb3-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32eb3-167">OUTPUTS</span></span>

### <span data-ttu-id="32eb3-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="32eb3-168">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="32eb3-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32eb3-169">NOTES</span></span>

## <span data-ttu-id="32eb3-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32eb3-170">RELATED LINKS</span></span>

[<span data-ttu-id="32eb3-171">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="32eb3-171">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="32eb3-172">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="32eb3-172">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="32eb3-173">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="32eb3-173">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
