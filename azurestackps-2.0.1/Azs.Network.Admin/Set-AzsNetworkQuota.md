---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/set-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: c2cc0e7a22d7e581eece9004950b54bc0151fad3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075262"
---
# <span data-ttu-id="4da1a-101">Set-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="4da1a-101">Set-AzsNetworkQuota</span></span>

## <span data-ttu-id="4da1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4da1a-102">SYNOPSIS</span></span>
<span data-ttu-id="4da1a-103">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="4da1a-103">Create or update a quota.</span></span>

## <span data-ttu-id="4da1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4da1a-104">SYNTAX</span></span>

### <span data-ttu-id="4da1a-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4da1a-105">UpdateExpanded (Default)</span></span>
```
Set-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4da1a-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="4da1a-106">Update</span></span>
```
Set-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4da1a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4da1a-107">DESCRIPTION</span></span>
<span data-ttu-id="4da1a-108">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="4da1a-108">Create or update a quota.</span></span>

## <span data-ttu-id="4da1a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4da1a-109">EXAMPLES</span></span>

### <span data-ttu-id="4da1a-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4da1a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxVnetsPerSubscription 20
```

<span data-ttu-id="4da1a-111">Обновление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="4da1a-111">Update a network quota by name.</span></span>

### <span data-ttu-id="4da1a-112">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4da1a-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Set-AzsNetworkQuota -Name NetworkQuota1 -MaxPublicIpsPerSubscription 75 -MaxNicsPerSubscription 100
```

<span data-ttu-id="4da1a-113">Обновление сетевой квоты по имени.</span><span class="sxs-lookup"><span data-stu-id="4da1a-113">Update a network quota by name.</span></span>

## <span data-ttu-id="4da1a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4da1a-114">PARAMETERS</span></span>

### <span data-ttu-id="4da1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da1a-115">-DefaultProfile</span></span>
<span data-ttu-id="4da1a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4da1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="4da1a-117">-Location</span></span>
<span data-ttu-id="4da1a-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="4da1a-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-119">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="4da1a-119">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="4da1a-120">Максимальное количество подсистем балансировки нагрузки, которое может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="4da1a-120">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-121">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="4da1a-121">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="4da1a-122">Максимальное число сетевых адаптеров, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="4da1a-122">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-123">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="4da1a-123">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="4da1a-124">Максимальное количество общедоступных IP-адресов, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="4da1a-124">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-125">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="4da1a-125">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="4da1a-126">Максимальное количество групп безопасности, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="4da1a-126">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="4da1a-127">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="4da1a-128">Максимальное количество подключений к шлюзу виртуальной сети, которое может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="4da1a-128">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-129">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="4da1a-129">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="4da1a-130">Максимальное число шлюзов виртуальных сетей, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="4da1a-130">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-131">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="4da1a-131">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="4da1a-132">Максимальное количество виртуальных сетей, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="4da1a-132">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4da1a-133">-Name</span></span>
<span data-ttu-id="4da1a-134">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="4da1a-134">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-135">-Quota</span><span class="sxs-lookup"><span data-stu-id="4da1a-135">-Quota</span></span>
<span data-ttu-id="4da1a-136">Ресурс "Сетевая квота".</span><span class="sxs-lookup"><span data-stu-id="4da1a-136">Network quota resource.</span></span>
<span data-ttu-id="4da1a-137">Для конструирования щелкните раздел "Заметки" для получения свойств квот и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4da1a-137">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4da1a-138">-SubscriptionId</span></span>
<span data-ttu-id="4da1a-139">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4da1a-139">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4da1a-140">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4da1a-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="4da1a-141">-Tag</span></span>
<span data-ttu-id="4da1a-142">Список пар "ключевые значения".</span><span class="sxs-lookup"><span data-stu-id="4da1a-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4da1a-143">-Confirm</span></span>
<span data-ttu-id="4da1a-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4da1a-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da1a-145">-WhatIf</span></span>
<span data-ttu-id="4da1a-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4da1a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4da1a-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4da1a-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4da1a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da1a-148">CommonParameters</span></span>
<span data-ttu-id="4da1a-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4da1a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da1a-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4da1a-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da1a-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4da1a-151">INPUTS</span></span>

### <span data-ttu-id="4da1a-152">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="4da1a-152">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

## <span data-ttu-id="4da1a-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4da1a-153">OUTPUTS</span></span>

### <span data-ttu-id="4da1a-154">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="4da1a-154">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="4da1a-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="4da1a-155">NOTES</span></span>

<span data-ttu-id="4da1a-156">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4da1a-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4da1a-157">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4da1a-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4da1a-158">КВОТа <IQuota> : ресурс "Сетевая квота".</span><span class="sxs-lookup"><span data-stu-id="4da1a-158">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="4da1a-159">`[Tag <IResourceTags>]`: Список пар значений ключа.</span><span class="sxs-lookup"><span data-stu-id="4da1a-159">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="4da1a-160">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="4da1a-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4da1a-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Максимальное количество подсистем балансировки нагрузки, которое может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="4da1a-161">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="4da1a-162">`[MaxNicsPerSubscription <Int64?>]`: Максимальное число сетевых адаптеров, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="4da1a-162">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="4da1a-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Максимальное количество общедоступных IP-адресов, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="4da1a-163">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="4da1a-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Максимальное количество групп безопасности, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="4da1a-164">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="4da1a-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Максимальное количество подключений к шлюзу виртуальной сети, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="4da1a-165">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="4da1a-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Максимальное число шлюзов виртуальных сетей, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="4da1a-166">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="4da1a-167">`[MaxVnetsPerSubscription <Int64?>]`: Максимальное количество виртуальных сетей, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="4da1a-167">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="4da1a-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4da1a-168">RELATED LINKS</span></span>

