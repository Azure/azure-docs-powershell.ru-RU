---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0F141A92-4994-45B3-AE94-09865BC691C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: 0b4bdbcdb4a753943278b759d584bb034a717b62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915126"
---
# <span data-ttu-id="aaa4f-101">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aaa4f-101">New-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="aaa4f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aaa4f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaa4f-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aaa4f-103">SYNTAX</span></span>

### <span data-ttu-id="aaa4f-104">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aaa4f-104">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-Peer <PSPeering>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaa4f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="aaa4f-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> -Location <String>
 [-AuthorizationKey <String>] -VirtualNetworkGateway1 <PSVirtualNetworkGateway>
 [-VirtualNetworkGateway2 <PSVirtualNetworkGateway>] [-LocalNetworkGateway2 <PSLocalNetworkGateway>]
 -ConnectionType <String> [-RoutingWeight <Int32>] [-SharedKey <String>] [-PeerId <String>]
 [-EnableBgp <Boolean>] [-Tag <Hashtable>] [-Force] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaa4f-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaa4f-106">DESCRIPTION</span></span>

## <span data-ttu-id="aaa4f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aaa4f-107">EXAMPLES</span></span>

### <span data-ttu-id="aaa4f-108">1:</span><span class="sxs-lookup"><span data-stu-id="aaa4f-108">1:</span></span>
```
New-AzureRmVirtualNetworkGatewayConnection -Name conn-client-1 -ResourceGroupName $RG1 -VirtualNetworkGateway1 $vnetgw1 -VirtualNetworkGateway2 $vnetgw2 -Location $loc1 -ConnectionType Vnet2Vnet -SharedKey 'a1b2c3d4e5'
```

## <span data-ttu-id="aaa4f-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aaa4f-109">PARAMETERS</span></span>

### <span data-ttu-id="aaa4f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaa4f-110">-AsJob</span></span>
<span data-ttu-id="aaa4f-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aaa4f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aaa4f-112">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="aaa4f-112">-AuthorizationKey</span></span>
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

### <span data-ttu-id="aaa4f-113">-ConnectionType</span><span class="sxs-lookup"><span data-stu-id="aaa4f-113">-ConnectionType</span></span>
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

### <span data-ttu-id="aaa4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa4f-114">-DefaultProfile</span></span>
<span data-ttu-id="aaa4f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa4f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaa4f-116">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="aaa4f-116">-EnableBgp</span></span>
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

### <span data-ttu-id="aaa4f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="aaa4f-117">-Force</span></span>
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

### <span data-ttu-id="aaa4f-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="aaa4f-118">-IpsecPolicies</span></span>
<span data-ttu-id="aaa4f-119">Список политик IPSec.</span><span class="sxs-lookup"><span data-stu-id="aaa4f-119">A list of IPSec policies.</span></span>
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

### <span data-ttu-id="aaa4f-120">-LocalNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="aaa4f-120">-LocalNetworkGateway2</span></span>
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

### <span data-ttu-id="aaa4f-121">-Location</span><span class="sxs-lookup"><span data-stu-id="aaa4f-121">-Location</span></span>
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

### <span data-ttu-id="aaa4f-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aaa4f-122">-Name</span></span>
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

### <span data-ttu-id="aaa4f-123">-Peer</span><span class="sxs-lookup"><span data-stu-id="aaa4f-123">-Peer</span></span>
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

### <span data-ttu-id="aaa4f-124">-PeerId</span><span class="sxs-lookup"><span data-stu-id="aaa4f-124">-PeerId</span></span>
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

### <span data-ttu-id="aaa4f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa4f-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="aaa4f-126">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="aaa4f-126">-RoutingWeight</span></span>
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

### <span data-ttu-id="aaa4f-127">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="aaa4f-127">-SharedKey</span></span>
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

### <span data-ttu-id="aaa4f-128">-Тег</span><span class="sxs-lookup"><span data-stu-id="aaa4f-128">-Tag</span></span>
<span data-ttu-id="aaa4f-129">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="aaa4f-129">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aaa4f-130">Например:</span><span class="sxs-lookup"><span data-stu-id="aaa4f-130">For example:</span></span>

<span data-ttu-id="aaa4f-131">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="aaa4f-131">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aaa4f-132">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="aaa4f-132">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="aaa4f-133">Использование селекторов трафика на основе политики для подключения S2S</span><span class="sxs-lookup"><span data-stu-id="aaa4f-133">Use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="aaa4f-134">-VirtualNetworkGateway1</span><span class="sxs-lookup"><span data-stu-id="aaa4f-134">-VirtualNetworkGateway1</span></span>
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

### <span data-ttu-id="aaa4f-135">-VirtualNetworkGateway2</span><span class="sxs-lookup"><span data-stu-id="aaa4f-135">-VirtualNetworkGateway2</span></span>
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

### <span data-ttu-id="aaa4f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaa4f-136">-Confirm</span></span>
<span data-ttu-id="aaa4f-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aaa4f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaa4f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa4f-138">-WhatIf</span></span>
<span data-ttu-id="aaa4f-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aaa4f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaa4f-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aaa4f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaa4f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa4f-141">CommonParameters</span></span>
<span data-ttu-id="aaa4f-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aaa4f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa4f-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa4f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa4f-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aaa4f-144">INPUTS</span></span>

## <span data-ttu-id="aaa4f-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaa4f-145">OUTPUTS</span></span>

### <span data-ttu-id="aaa4f-146">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aaa4f-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="aaa4f-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="aaa4f-147">NOTES</span></span>

## <span data-ttu-id="aaa4f-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaa4f-148">RELATED LINKS</span></span>

[<span data-ttu-id="aaa4f-149">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aaa4f-149">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="aaa4f-150">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aaa4f-150">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="aaa4f-151">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="aaa4f-151">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)
