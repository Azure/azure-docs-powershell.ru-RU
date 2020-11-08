---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d20f84d91c110ae1f4e55508b33f758fc0d5583
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076887"
---
# <span data-ttu-id="6fd02-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="6fd02-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="6fd02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6fd02-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd02-103">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="6fd02-103">Create or update a quota.</span></span>

## <span data-ttu-id="6fd02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6fd02-104">SYNTAX</span></span>

### <span data-ttu-id="6fd02-105">Квоты (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6fd02-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd02-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd02-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fd02-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6fd02-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fd02-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fd02-108">DESCRIPTION</span></span>
<span data-ttu-id="6fd02-109">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="6fd02-109">Create or update a quota.</span></span>

## <span data-ttu-id="6fd02-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6fd02-110">EXAMPLES</span></span>

### <span data-ttu-id="6fd02-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="6fd02-111">EXAMPLE 1</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="6fd02-112">Обновление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="6fd02-112">Update a network quota by name.</span></span>

### <span data-ttu-id="6fd02-113">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="6fd02-113">EXAMPLE 2</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="6fd02-114">Обновление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="6fd02-114">Update a network quota by name.</span></span>

## <span data-ttu-id="6fd02-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6fd02-115">PARAMETERS</span></span>

### <span data-ttu-id="6fd02-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6fd02-116">-Name</span></span>
<span data-ttu-id="6fd02-117">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="6fd02-117">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-118">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6fd02-118">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="6fd02-119">Максимальные сетевые адаптеры, разрешенные на подписку.</span><span class="sxs-lookup"><span data-stu-id="6fd02-119">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-120">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6fd02-120">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="6fd02-121">Максимальное количество общедоступных IP-адресов, разрешенных для подписки.</span><span class="sxs-lookup"><span data-stu-id="6fd02-121">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6fd02-122">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="6fd02-123">Максимальное количество подключений к шлюзу виртуальной сети, разрешенных для одной подписки.</span><span class="sxs-lookup"><span data-stu-id="6fd02-123">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-124">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6fd02-124">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="6fd02-125">Максимальное число виртуальных сетей, разрешенных на подписку.</span><span class="sxs-lookup"><span data-stu-id="6fd02-125">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-126">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6fd02-126">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="6fd02-127">Максимальное количество шлюзов виртуальных сетей, разрешенных для каждой подписки.</span><span class="sxs-lookup"><span data-stu-id="6fd02-127">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-128">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6fd02-128">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="6fd02-129">Максимальное количество групп безопасности, разрешенных на подписку.</span><span class="sxs-lookup"><span data-stu-id="6fd02-129">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-130">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6fd02-130">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="6fd02-131">Максимально допустимое количество подсистем балансировки нагрузки для каждой подписки.</span><span class="sxs-lookup"><span data-stu-id="6fd02-131">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-132">-Location</span><span class="sxs-lookup"><span data-stu-id="6fd02-132">-Location</span></span>
<span data-ttu-id="6fd02-133">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6fd02-133">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Quotas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd02-134">-ResourceId</span></span>
<span data-ttu-id="6fd02-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6fd02-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fd02-136">-InputObject</span></span>
<span data-ttu-id="6fd02-137">Posbbily изменена сетевая квота, возвращенная Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="6fd02-137">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

```yaml
Type: Quota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fd02-138">-WhatIf</span></span>
<span data-ttu-id="6fd02-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6fd02-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fd02-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6fd02-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fd02-141">-Confirm</span></span>
<span data-ttu-id="6fd02-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6fd02-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd02-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd02-143">CommonParameters</span></span>
<span data-ttu-id="6fd02-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6fd02-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd02-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd02-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd02-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6fd02-146">INPUTS</span></span>

## <span data-ttu-id="6fd02-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fd02-147">OUTPUTS</span></span>

### <span data-ttu-id="6fd02-148">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="6fd02-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="6fd02-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="6fd02-149">NOTES</span></span>

## <span data-ttu-id="6fd02-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fd02-150">RELATED LINKS</span></span>
