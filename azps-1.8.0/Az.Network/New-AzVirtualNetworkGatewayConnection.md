---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8f6b095a502c235927a48f2043a9140483cedc3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730260"
---
# <span data-ttu-id="478e8-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="478e8-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="478e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="478e8-102">SYNOPSIS</span></span>
<span data-ttu-id="478e8-103">Создание подключения VPN между сайтами между шлюзом виртуальной сети и локальным устройством VPN.</span><span class="sxs-lookup"><span data-stu-id="478e8-103">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="478e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="478e8-104">SYNTAX</span></span>

### <span data-ttu-id="478e8-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="478e8-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478e8-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="478e8-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-AsJob] [-ExpressRouteGatewayBypass]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="478e8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="478e8-107">DESCRIPTION</span></span>
<span data-ttu-id="478e8-108">Создание подключения VPN между сайтами между шлюзом виртуальной сети и локальным устройством VPN.</span><span class="sxs-lookup"><span data-stu-id="478e8-108">Creates the Site-to-Site VPN connection between the virtual network gateway and the on-prem VPN device.</span></span>

## <span data-ttu-id="478e8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="478e8-109">EXAMPLES</span></span>

### <span data-ttu-id="478e8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="478e8-110">Example 1</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="478e8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="478e8-111">PARAMETERS</span></span>

### <span data-ttu-id="478e8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="478e8-112">-AsJob</span></span>
<span data-ttu-id="478e8-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="478e8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="478e8-114">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="478e8-114">-AuthorizationKey</span></span>

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

### <span data-ttu-id="478e8-115">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="478e8-115">-ConnectionType</span></span>

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

### <span data-ttu-id="478e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478e8-116">-DefaultProfile</span></span>
<span data-ttu-id="478e8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="478e8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="478e8-118">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="478e8-118">-EnableBgp</span></span>

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

### <span data-ttu-id="478e8-119">-ExpressRouteGatewayBypass</span><span class="sxs-lookup"><span data-stu-id="478e8-119">-ExpressRouteGatewayBypass</span></span>

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

### <span data-ttu-id="478e8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="478e8-120">-Force</span></span>

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

### <span data-ttu-id="478e8-121">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="478e8-121">-IpsecPolicies</span></span>
<span data-ttu-id="478e8-122">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="478e8-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="478e8-123">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="478e8-123">-LocalNetworkGateway2</span></span>

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

### <span data-ttu-id="478e8-124">-Location</span><span class="sxs-lookup"><span data-stu-id="478e8-124">-Location</span></span>

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

### <span data-ttu-id="478e8-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="478e8-125">-Name</span></span>

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

### <span data-ttu-id="478e8-126">-Peer</span><span class="sxs-lookup"><span data-stu-id="478e8-126">-Peer</span></span>

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

### <span data-ttu-id="478e8-127">-PeerId</span><span class="sxs-lookup"><span data-stu-id="478e8-127">-PeerId</span></span>

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

### <span data-ttu-id="478e8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478e8-128">-ResourceGroupName</span></span>

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

### <span data-ttu-id="478e8-129">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="478e8-129">-RoutingWeight</span></span>

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

### <span data-ttu-id="478e8-130">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="478e8-130">-SharedKey</span></span>

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

### <span data-ttu-id="478e8-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="478e8-131">-Tag</span></span>
<span data-ttu-id="478e8-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="478e8-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="478e8-133">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="478e8-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="478e8-134">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="478e8-134">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="478e8-135">Использование селекторов трафика на основе политики для подключения S2S</span><span class="sxs-lookup"><span data-stu-id="478e8-135">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="478e8-136">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="478e8-136">-VirtualNetworkGateway1</span></span>

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

### <span data-ttu-id="478e8-137">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="478e8-137">-VirtualNetworkGateway2</span></span>

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

### <span data-ttu-id="478e8-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="478e8-138">-Confirm</span></span>
<span data-ttu-id="478e8-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="478e8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478e8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478e8-140">-WhatIf</span></span>
<span data-ttu-id="478e8-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="478e8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="478e8-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="478e8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478e8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478e8-143">CommonParameters</span></span>
<span data-ttu-id="478e8-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="478e8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478e8-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478e8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478e8-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="478e8-146">INPUTS</span></span>

### <span data-ttu-id="478e8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="478e8-147">System.String</span></span>

### <span data-ttu-id="478e8-148">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="478e8-148">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="478e8-149">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="478e8-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="478e8-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="478e8-150">System.Int32</span></span>

### <span data-ttu-id="478e8-151">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="478e8-151">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

### <span data-ttu-id="478e8-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="478e8-152">System.Boolean</span></span>

### <span data-ttu-id="478e8-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="478e8-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="478e8-154">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="478e8-154">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="478e8-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="478e8-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="478e8-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="478e8-156">OUTPUTS</span></span>

### <span data-ttu-id="478e8-157">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="478e8-157">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="478e8-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="478e8-158">NOTES</span></span>

## <span data-ttu-id="478e8-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="478e8-159">RELATED LINKS</span></span>

[<span data-ttu-id="478e8-160">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="478e8-160">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="478e8-161">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="478e8-161">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="478e8-162">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="478e8-162">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
