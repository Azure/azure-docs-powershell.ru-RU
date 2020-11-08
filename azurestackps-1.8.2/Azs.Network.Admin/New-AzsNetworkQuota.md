---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: acda4a136b98a8a83190704a3635bd97ae97a7b2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076815"
---
# <span data-ttu-id="38a94-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="38a94-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="38a94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38a94-102">SYNOPSIS</span></span>
<span data-ttu-id="38a94-103">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="38a94-103">Create or update a quota.</span></span>

## <span data-ttu-id="38a94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38a94-104">SYNTAX</span></span>

```
New-AzsNetworkQuota [-Name] <String> [[-MaxNicsPerSubscription] <Int64>]
 [[-MaxPublicIpsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewayConnectionsPerSubscription] <Int64>]
 [[-MaxVnetsPerSubscription] <Int64>] [[-MaxVirtualNetworkGatewaysPerSubscription] <Int64>]
 [[-MaxSecurityGroupsPerSubscription] <Int64>] [[-MaxLoadBalancersPerSubscription] <Int64>]
 [[-Location] <String>] [[-MigrationPhase] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38a94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38a94-105">DESCRIPTION</span></span>
<span data-ttu-id="38a94-106">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="38a94-106">Create or update a quota.</span></span>

## <span data-ttu-id="38a94-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38a94-107">EXAMPLES</span></span>

### <span data-ttu-id="38a94-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="38a94-108">EXAMPLE 1</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="38a94-109">Создание новой сетевой квоты со всеми значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="38a94-109">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="38a94-110">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="38a94-110">EXAMPLE 2</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```

<span data-ttu-id="38a94-111">Создание новой сетевой квоты с нестандартными значениями квоты.</span><span class="sxs-lookup"><span data-stu-id="38a94-111">Create a new network quota with non default values for quota.</span></span>

## <span data-ttu-id="38a94-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38a94-112">PARAMETERS</span></span>

### <span data-ttu-id="38a94-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38a94-113">-Name</span></span>
<span data-ttu-id="38a94-114">Имя ресурса сетевой квоты.</span><span class="sxs-lookup"><span data-stu-id="38a94-114">Name of the network quota resource.</span></span>

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

### <span data-ttu-id="38a94-115">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="38a94-115">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="38a94-116">Максимальные сетевые адаптеры, разрешенные на подписку.</span><span class="sxs-lookup"><span data-stu-id="38a94-116">The maximum NICs allowed per subscription.</span></span>

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

### <span data-ttu-id="38a94-117">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="38a94-117">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="38a94-118">Максимальное количество общедоступных IP-адресов, разрешенных для подписки.</span><span class="sxs-lookup"><span data-stu-id="38a94-118">The maximum public IP addresses allowed per subscription.</span></span>

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

### <span data-ttu-id="38a94-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="38a94-119">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="38a94-120">Максимальное количество подключений к шлюзу виртуальной сети, разрешенных для одной подписки.</span><span class="sxs-lookup"><span data-stu-id="38a94-120">The maximum number of virtual network gateway connections allowed per subscription.</span></span>

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

### <span data-ttu-id="38a94-121">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="38a94-121">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="38a94-122">Максимальное число виртуальных сетей, разрешенных на подписку.</span><span class="sxs-lookup"><span data-stu-id="38a94-122">The maxium number of virtual networks allowed per subscription.</span></span>

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

### <span data-ttu-id="38a94-123">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="38a94-123">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="38a94-124">Максимальное количество шлюзов виртуальных сетей, разрешенных для каждой подписки.</span><span class="sxs-lookup"><span data-stu-id="38a94-124">The maximum number of virtual network gateways allowed per subscription.</span></span>

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

### <span data-ttu-id="38a94-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="38a94-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="38a94-126">Максимальное количество групп безопасности, разрешенных на подписку.</span><span class="sxs-lookup"><span data-stu-id="38a94-126">The maximum number of security groups allowed per subscription.</span></span>

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

### <span data-ttu-id="38a94-127">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="38a94-127">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="38a94-128">Максимально допустимое количество подсистем балансировки нагрузки для каждой подписки.</span><span class="sxs-lookup"><span data-stu-id="38a94-128">The maximum number of load balancers allowed per subscription.</span></span>

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

### <span data-ttu-id="38a94-129">-Location</span><span class="sxs-lookup"><span data-stu-id="38a94-129">-Location</span></span>
<span data-ttu-id="38a94-130">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="38a94-130">Location of the resource.</span></span>

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

### <span data-ttu-id="38a94-131">-MigrationPhase</span><span class="sxs-lookup"><span data-stu-id="38a94-131">-MigrationPhase</span></span>
<span data-ttu-id="38a94-132">Состояние миграции, например None, Prepare, Commit и Abort.</span><span class="sxs-lookup"><span data-stu-id="38a94-132">State of migration such as None, Prepare, Commit, and Abort.</span></span>

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

### <span data-ttu-id="38a94-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38a94-133">-WhatIf</span></span>
<span data-ttu-id="38a94-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38a94-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38a94-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38a94-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38a94-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38a94-136">-Confirm</span></span>
<span data-ttu-id="38a94-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38a94-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38a94-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a94-138">CommonParameters</span></span>
<span data-ttu-id="38a94-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38a94-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a94-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38a94-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a94-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38a94-141">INPUTS</span></span>

## <span data-ttu-id="38a94-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38a94-142">OUTPUTS</span></span>

### <span data-ttu-id="38a94-143">Microsoft. AzureStack. Management. Network. admin. Models. Quota</span><span class="sxs-lookup"><span data-stu-id="38a94-143">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="38a94-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="38a94-144">NOTES</span></span>

## <span data-ttu-id="38a94-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38a94-145">RELATED LINKS</span></span>
