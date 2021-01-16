---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: f6dc25bc1000466d853715f62e38237ddfc76aa2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507806"
---
# <span data-ttu-id="f9de2-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9de2-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f9de2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9de2-102">SYNOPSIS</span></span>
<span data-ttu-id="f9de2-103">Создает VPN-подключение "сайт-сайт" между виртуальным сетевым шлюзом и мобильным VPN-устройством.</span><span class="sxs-lookup"><span data-stu-id="f9de2-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="f9de2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f9de2-104">SYNTAX</span></span>

### <span data-ttu-id="f9de2-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f9de2-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="f9de2-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9de2-106">SetByResourceId</span></span>
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

## <span data-ttu-id="f9de2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9de2-107">DESCRIPTION</span></span>
<span data-ttu-id="f9de2-108">Создает VPN-подключение "сайт-сайт" между виртуальным сетевым шлюзом и мобильным VPN-устройством.</span><span class="sxs-lookup"><span data-stu-id="f9de2-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="f9de2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f9de2-109">EXAMPLES</span></span>

### <span data-ttu-id="f9de2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9de2-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="f9de2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9de2-111">PARAMETERS</span></span>

### <span data-ttu-id="f9de2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9de2-112">-AsJob</span></span>
<span data-ttu-id="f9de2-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f9de2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9de2-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="f9de2-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="f9de2-115">-ConnectionProtocol</span><span class="sxs-lookup"><span data-stu-id="f9de2-115">-ConnectionProtocol</span></span>
<span data-ttu-id="f9de2-116">Протокол подключения шлюза:IKEv1/IKEv2</span><span class="sxs-lookup"><span data-stu-id="f9de2-116">Gateway connection protocol:IKEv1/IKEv2</span></span>

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

### <span data-ttu-id="f9de2-117">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="f9de2-117">-ConnectionType</span></span>

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

### <span data-ttu-id="f9de2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9de2-118">-DefaultProfile</span></span>
<span data-ttu-id="f9de2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9de2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9de2-120">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f9de2-120">-EnableBgp</span></span>

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

### <span data-ttu-id="f9de2-121">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="f9de2-121">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="f9de2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f9de2-122">-Force</span></span>

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

### <span data-ttu-id="f9de2-123">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="f9de2-123">-IpsecPolicies</span></span>
<span data-ttu-id="f9de2-124">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="f9de2-124">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="f9de2-125">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="f9de2-125">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="f9de2-126">-Location</span><span class="sxs-lookup"><span data-stu-id="f9de2-126">-Location</span></span>

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

### <span data-ttu-id="f9de2-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f9de2-127">-Name</span></span>

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

### <span data-ttu-id="f9de2-128">-Одноранговая</span><span class="sxs-lookup"><span data-stu-id="f9de2-128">-Peer</span></span>

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

### <span data-ttu-id="f9de2-129">-PeerId</span><span class="sxs-lookup"><span data-stu-id="f9de2-129">-PeerId</span></span>

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

### <span data-ttu-id="f9de2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9de2-130">-ResourceGroupName</span></span>

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

### <span data-ttu-id="f9de2-131">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="f9de2-131">-RoutingWeight</span></span>

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

### <span data-ttu-id="f9de2-132">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="f9de2-132">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="f9de2-133">Время обнаружения неавтных подключений за считанные секунды</span><span class="sxs-lookup"><span data-stu-id="f9de2-133">Dead Peer Detection Timeout of the connection in seconds</span></span>

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

### <span data-ttu-id="f9de2-134">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="f9de2-134">-SharedKey</span></span>

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

### <span data-ttu-id="f9de2-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9de2-135">-Tag</span></span>
<span data-ttu-id="f9de2-136">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="f9de2-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f9de2-137">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f9de2-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f9de2-138">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f9de2-138">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="f9de2-139">Список политик выбора трафика.</span><span class="sxs-lookup"><span data-stu-id="f9de2-139">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="f9de2-140">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9de2-140">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="f9de2-141">Следует ли использовать PrivateIP для этого VPN-туннель S2S</span><span class="sxs-lookup"><span data-stu-id="f9de2-141">Whether to use PrivateIP for this S2S VPN tunnel</span></span>

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

### <span data-ttu-id="f9de2-142">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="f9de2-142">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="f9de2-143">Использование селекторов трафика на основе политик для подключения S2S</span><span class="sxs-lookup"><span data-stu-id="f9de2-143">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="f9de2-144">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="f9de2-144">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="f9de2-145">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="f9de2-145">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="f9de2-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9de2-146">-Confirm</span></span>
<span data-ttu-id="f9de2-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f9de2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9de2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9de2-148">-WhatIf</span></span>
<span data-ttu-id="f9de2-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9de2-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9de2-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f9de2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9de2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9de2-151">CommonParameters</span></span>
<span data-ttu-id="f9de2-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9de2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9de2-153">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9de2-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9de2-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9de2-154">INPUTS</span></span>

### <span data-ttu-id="f9de2-155">System.String</span><span class="sxs-lookup"><span data-stu-id="f9de2-155">System.String</span></span>

### <span data-ttu-id="f9de2-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f9de2-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f9de2-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f9de2-157">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="f9de2-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f9de2-158">System.Int32</span></span>

### <span data-ttu-id="f9de2-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="f9de2-159">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="f9de2-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f9de2-160">System.Boolean</span></span>

### <span data-ttu-id="f9de2-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f9de2-161">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f9de2-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="f9de2-162">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f9de2-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span><span class="sxs-lookup"><span data-stu-id="f9de2-163">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

### <span data-ttu-id="f9de2-164">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9de2-164">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f9de2-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f9de2-165">OUTPUTS</span></span>

### <span data-ttu-id="f9de2-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9de2-166">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f9de2-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f9de2-167">NOTES</span></span>

## <span data-ttu-id="f9de2-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9de2-168">RELATED LINKS</span></span>

[<span data-ttu-id="f9de2-169">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9de2-169">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f9de2-170">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9de2-170">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f9de2-171">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f9de2-171">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
