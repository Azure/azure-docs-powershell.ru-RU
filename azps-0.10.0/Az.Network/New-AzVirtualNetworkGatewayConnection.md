---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 7aede18c438faca196d696a69e7f7651edac132e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909602"
---
# <span data-ttu-id="31852-101">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31852-101">New-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="31852-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31852-102">SYNOPSIS</span></span>

## <span data-ttu-id="31852-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31852-103">SYNTAX</span></span>

### <span data-ttu-id="31852-104">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31852-104">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31852-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="31852-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31852-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31852-106">DESCRIPTION</span></span>

## <span data-ttu-id="31852-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31852-107">EXAMPLES</span></span>

### <span data-ttu-id="31852-108">1:</span><span class="sxs-lookup"><span data-stu-id="31852-108">1:</span></span>
```
New-AzVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="31852-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31852-109">PARAMETERS</span></span>

### <span data-ttu-id="31852-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31852-110">-AsJob</span></span>
<span data-ttu-id="31852-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="31852-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31852-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="31852-112">-AuthorizationKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="31852-113">-ConnectionType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPsec, Vnet2Vnet, ExpressRoute, VPNClient

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31852-114">-DefaultProfile</span></span>
<span data-ttu-id="31852-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31852-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31852-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="31852-116">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-117">-Force</span><span class="sxs-lookup"><span data-stu-id="31852-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31852-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="31852-118">-IpsecPolicies</span></span>
<span data-ttu-id="31852-119">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="31852-119">A list of IPSec policies.</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="31852-120">-LocalNetworkGateway2</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-121">-Location</span><span class="sxs-lookup"><span data-stu-id="31852-121">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31852-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="31852-123">-Peer</span></span>
```yaml
Type: PSPeering
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="31852-124">-PeerId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31852-125">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="31852-126">-RoutingWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="31852-127">-SharedKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="31852-128">-Tag</span></span>
<span data-ttu-id="31852-129">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="31852-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="31852-130">Например:</span><span class="sxs-lookup"><span data-stu-id="31852-130">For example:</span></span>

<span data-ttu-id="31852-131">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="31852-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="31852-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="31852-133">Использование селекторов трафика на основе политики для подключения S2S</span><span class="sxs-lookup"><span data-stu-id="31852-133">Use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31852-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="31852-134">-VirtualNetworkGateway1</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="31852-135">-VirtualNetworkGateway2</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31852-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31852-136">-Confirm</span></span>
<span data-ttu-id="31852-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31852-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31852-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31852-138">-WhatIf</span></span>
<span data-ttu-id="31852-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31852-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31852-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31852-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31852-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31852-141">CommonParameters</span></span>
<span data-ttu-id="31852-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31852-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31852-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31852-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31852-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31852-144">INPUTS</span></span>

## <span data-ttu-id="31852-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31852-145">OUTPUTS</span></span>

### <span data-ttu-id="31852-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31852-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="31852-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="31852-147">NOTES</span></span>

## <span data-ttu-id="31852-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31852-148">RELATED LINKS</span></span>

[<span data-ttu-id="31852-149">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31852-149">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="31852-150">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31852-150">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="31852-151">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="31852-151">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
