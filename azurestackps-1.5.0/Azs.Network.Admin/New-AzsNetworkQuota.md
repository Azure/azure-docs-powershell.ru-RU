---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc762c4b7d932f682f77e2df6586c773e0f22e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555883"
---
# <span data-ttu-id="6068e-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="6068e-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="6068e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6068e-102">SYNOPSIS</span></span>
<span data-ttu-id="6068e-103">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="6068e-103">Create or update a quota.</span></span>

## <span data-ttu-id="6068e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6068e-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6068e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6068e-105">DESCRIPTION</span></span>
<span data-ttu-id="6068e-106">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="6068e-106">Create or update a quota.</span></span>

## <span data-ttu-id="6068e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6068e-107">EXAMPLES</span></span>

### <span data-ttu-id="6068e-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6068e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="6068e-109">Создание новой сетевой квоты со всеми значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6068e-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="6068e-110">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6068e-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="6068e-111">Создание новой сетевой квоты с нестандартными значениями квоты.</span><span class="sxs-lookup"><span data-stu-id="6068e-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="6068e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6068e-112">PARAMETERS</span></span>

### <span data-ttu-id="6068e-113">-Location</span><span class="sxs-lookup"><span data-stu-id="6068e-113">-Location</span></span>
<span data-ttu-id="6068e-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6068e-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-115">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6068e-115">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="6068e-116">Максимально допустимое количество подсистем балансировки нагрузки для каждой подписки.</span><span class="sxs-lookup"><span data-stu-id="6068e-116">The maximum number of load balancers allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-117">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6068e-117">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="6068e-118">Максимальные сетевые адаптеры, разрешенные на подписку.</span><span class="sxs-lookup"><span data-stu-id="6068e-118">The maximum NICs allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-119">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6068e-119">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="6068e-120">Максимальное количество общедоступных IP-адресов, разрешенных для подписки.</span><span class="sxs-lookup"><span data-stu-id="6068e-120">The maximum public IP addresses allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-121">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6068e-121">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="6068e-122">Максимальное количество групп безопасности, разрешенных на подписку.</span><span class="sxs-lookup"><span data-stu-id="6068e-122">The maximum number of security groups allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6068e-123">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="6068e-124">Максимальное количество подключений к шлюзу виртуальной сети, разрешенных для одной подписки.</span><span class="sxs-lookup"><span data-stu-id="6068e-124">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-125">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6068e-125">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="6068e-126">Максимальное количество шлюзов виртуальных сетей, разрешенных для каждой подписки.</span><span class="sxs-lookup"><span data-stu-id="6068e-126">The maximum number of virtual network gateways allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-127">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="6068e-127">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="6068e-128">Максимальное число виртуальных сетей, разрешенных на подписку.</span><span class="sxs-lookup"><span data-stu-id="6068e-128">The maxium number of virtual networks allowed per subscription.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-129">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="6068e-129">-MigrationPhase</span></span>
<span data-ttu-id="6068e-130">Устаревшие.</span><span class="sxs-lookup"><span data-stu-id="6068e-130">Deprecated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: Prepare
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6068e-131">-Name</span></span>
<span data-ttu-id="6068e-132">Имя ресурса сетевой квоты.</span><span class="sxs-lookup"><span data-stu-id="6068e-132">Name of the network quota resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6068e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6068e-133">-Confirm</span></span>
<span data-ttu-id="6068e-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6068e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6068e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6068e-135">-WhatIf</span></span>
<span data-ttu-id="6068e-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6068e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6068e-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6068e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6068e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6068e-138">CommonParameters</span></span>
<span data-ttu-id="6068e-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6068e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6068e-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6068e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6068e-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6068e-141">INPUTS</span></span>

## <span data-ttu-id="6068e-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6068e-142">OUTPUTS</span></span>

### <span data-ttu-id="6068e-143">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="6068e-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="6068e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="6068e-144">NOTES</span></span>

## <span data-ttu-id="6068e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6068e-145">RELATED LINKS</span></span>

