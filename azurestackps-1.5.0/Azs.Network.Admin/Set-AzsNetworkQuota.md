---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2867f0c438f1f8752137f680365ecade255d291
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556115"
---
# <span data-ttu-id="b77c2-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="b77c2-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="b77c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b77c2-102">SYNOPSIS</span></span>
<span data-ttu-id="b77c2-103">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="b77c2-103">Create or update a quota.</span></span>

## <span data-ttu-id="b77c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b77c2-104">SYNTAX</span></span>

### <span data-ttu-id="b77c2-105">Квоты (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b77c2-105">Quotas (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b77c2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b77c2-106">ResourceId</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b77c2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b77c2-107">InputObject</span></span>
```
Set-AzsNetworkQuota [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxLoadBalancersPerSubscription <Int64>] -InputObject <Quota> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b77c2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b77c2-108">DESCRIPTION</span></span>
<span data-ttu-id="b77c2-109">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="b77c2-109">Create or update a quota.</span></span>

## <span data-ttu-id="b77c2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b77c2-110">EXAMPLES</span></span>

### <span data-ttu-id="b77c2-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b77c2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="b77c2-112">Обновление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="b77c2-112">Update a network quota by name.</span></span>

### <span data-ttu-id="b77c2-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b77c2-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="b77c2-114">Обновление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="b77c2-114">Update a network quota by name.</span></span>

## <span data-ttu-id="b77c2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b77c2-115">PARAMETERS</span></span>

### <span data-ttu-id="b77c2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b77c2-116">-InputObject</span></span>
<span data-ttu-id="b77c2-117">Posbbily изменена сетевая квота, возвращенная Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="b77c2-117">Posbbily modified network quota returned by Get-AzsNetworkQuota</span></span>

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

### <span data-ttu-id="b77c2-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b77c2-118">-Location</span></span>
<span data-ttu-id="b77c2-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b77c2-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b77c2-120">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b77c2-120">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="b77c2-121">Максимально допустимое количество подсистем балансировки нагрузки для каждой подписки.</span><span class="sxs-lookup"><span data-stu-id="b77c2-121">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="b77c2-122">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b77c2-122">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="b77c2-123">Максимальные сетевые адаптеры, разрешенные на подписку.</span><span class="sxs-lookup"><span data-stu-id="b77c2-123">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="b77c2-124">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b77c2-124">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="b77c2-125">Максимальное количество общедоступных IP-адресов, разрешенных для подписки.</span><span class="sxs-lookup"><span data-stu-id="b77c2-125">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="b77c2-126">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b77c2-126">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="b77c2-127">Максимальное количество групп безопасности, разрешенных на подписку.</span><span class="sxs-lookup"><span data-stu-id="b77c2-127">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="b77c2-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b77c2-128">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="b77c2-129">Максимальное количество подключений к шлюзу виртуальной сети, разрешенных для одной подписки.</span><span class="sxs-lookup"><span data-stu-id="b77c2-129">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="b77c2-130">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b77c2-130">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="b77c2-131">Максимальное количество шлюзов виртуальных сетей, разрешенных для каждой подписки.</span><span class="sxs-lookup"><span data-stu-id="b77c2-131">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="b77c2-132">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="b77c2-132">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="b77c2-133">Максимальное число виртуальных сетей, разрешенных на подписку.</span><span class="sxs-lookup"><span data-stu-id="b77c2-133">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="b77c2-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b77c2-134">-Name</span></span>
<span data-ttu-id="b77c2-135">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b77c2-135">Name of the resource.</span></span>

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

### <span data-ttu-id="b77c2-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b77c2-136">-ResourceId</span></span>
<span data-ttu-id="b77c2-137">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b77c2-137">The resource id.</span></span>

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

### <span data-ttu-id="b77c2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b77c2-138">-Confirm</span></span>
<span data-ttu-id="b77c2-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b77c2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b77c2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b77c2-140">-WhatIf</span></span>
<span data-ttu-id="b77c2-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b77c2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b77c2-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b77c2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b77c2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77c2-143">CommonParameters</span></span>
<span data-ttu-id="b77c2-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b77c2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77c2-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b77c2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77c2-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b77c2-146">INPUTS</span></span>

## <span data-ttu-id="b77c2-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b77c2-147">OUTPUTS</span></span>

### <span data-ttu-id="b77c2-148">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="b77c2-148">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="b77c2-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b77c2-149">NOTES</span></span>

## <span data-ttu-id="b77c2-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b77c2-150">RELATED LINKS</span></span>

