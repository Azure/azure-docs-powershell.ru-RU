---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910491"
---
# <span data-ttu-id="8f9a2-101">New-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="8f9a2-101">New-AzsNetworkQuota</span></span>

## <span data-ttu-id="8f9a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="8f9a2-103">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-103">Create or update a quota.</span></span>

## <span data-ttu-id="8f9a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f9a2-104">SYNTAX</span></span>

### <span data-ttu-id="8f9a2-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f9a2-105">CreateExpanded (Default)</span></span>
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f9a2-106">Заново</span><span class="sxs-lookup"><span data-stu-id="8f9a2-106">Create</span></span>
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f9a2-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8f9a2-107">CreateViaIdentity</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f9a2-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8f9a2-108">CreateViaIdentityExpanded</span></span>
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f9a2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f9a2-109">DESCRIPTION</span></span>
<span data-ttu-id="8f9a2-110">Создание или обновление квоты.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-110">Create or update a quota.</span></span>

## <span data-ttu-id="8f9a2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f9a2-111">EXAMPLES</span></span>

### <span data-ttu-id="8f9a2-112">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8f9a2-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

<span data-ttu-id="8f9a2-113">Создание новой сетевой квоты со всеми значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-113">Create a new network quota with all the default values.</span></span>

### <span data-ttu-id="8f9a2-114">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8f9a2-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
<span data-ttu-id="8f9a2-115">Создание новой сетевой квоты с нестандартными значениями квоты.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-115">Create a new network quota with non default values for quota.</span></span>



## <span data-ttu-id="8f9a2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f9a2-116">PARAMETERS</span></span>

### <span data-ttu-id="8f9a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f9a2-117">-DefaultProfile</span></span>
<span data-ttu-id="8f9a2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f9a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f9a2-119">-InputObject</span></span>
<span data-ttu-id="8f9a2-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-121">-Location</span><span class="sxs-lookup"><span data-stu-id="8f9a2-121">-Location</span></span>
<span data-ttu-id="8f9a2-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-123">-MaxLoadBalancersPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f9a2-123">-MaxLoadBalancersPerSubscription</span></span>
<span data-ttu-id="8f9a2-124">Максимальное количество подсистем балансировки нагрузки, которое может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-124">Maximum number of load balancers a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-125">-MaxNicsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f9a2-125">-MaxNicsPerSubscription</span></span>
<span data-ttu-id="8f9a2-126">Максимальное число сетевых адаптеров, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-126">Maximum number of NICs a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-127">-MaxPublicIpsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f9a2-127">-MaxPublicIpsPerSubscription</span></span>
<span data-ttu-id="8f9a2-128">Максимальное количество общедоступных IP-адресов, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-128">Maximum number of public IP addresses a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-129">-MaxSecurityGroupsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f9a2-129">-MaxSecurityGroupsPerSubscription</span></span>
<span data-ttu-id="8f9a2-130">Максимальное количество групп безопасности, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-130">Maximum number of security groups a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f9a2-131">-MaxVirtualNetworkGatewayConnectionsPerSubscription</span></span>
<span data-ttu-id="8f9a2-132">Максимальное количество подключений к шлюзу виртуальной сети, которое может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-132">Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-133">-MaxVirtualNetworkGatewaysPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f9a2-133">-MaxVirtualNetworkGatewaysPerSubscription</span></span>
<span data-ttu-id="8f9a2-134">Максимальное число шлюзов виртуальных сетей, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-134">Maximum number of virtual network gateways a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-135">-MaxVnetsPerSubscription</span><span class="sxs-lookup"><span data-stu-id="8f9a2-135">-MaxVnetsPerSubscription</span></span>
<span data-ttu-id="8f9a2-136">Максимальное количество виртуальных сетей, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-136">Maximum number of virtual networks a tenant subscription can provision.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f9a2-137">-Name</span></span>
<span data-ttu-id="8f9a2-138">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-138">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-139">-Quota</span><span class="sxs-lookup"><span data-stu-id="8f9a2-139">-Quota</span></span>
<span data-ttu-id="8f9a2-140">Ресурс "Сетевая квота".</span><span class="sxs-lookup"><span data-stu-id="8f9a2-140">Network quota resource.</span></span>
<span data-ttu-id="8f9a2-141">Для конструирования щелкните раздел "Заметки" для получения свойств квот и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-141">To construct, see NOTES section for QUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f9a2-142">-SubscriptionId</span></span>
<span data-ttu-id="8f9a2-143">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-143">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8f9a2-144">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-145">-Тег</span><span class="sxs-lookup"><span data-stu-id="8f9a2-145">-Tag</span></span>
<span data-ttu-id="8f9a2-146">Список пар "ключевые значения".</span><span class="sxs-lookup"><span data-stu-id="8f9a2-146">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8f9a2-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f9a2-147">-Confirm</span></span>
<span data-ttu-id="8f9a2-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f9a2-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f9a2-149">-WhatIf</span></span>
<span data-ttu-id="8f9a2-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f9a2-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f9a2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f9a2-152">CommonParameters</span></span>
<span data-ttu-id="8f9a2-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f9a2-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f9a2-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f9a2-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f9a2-155">INPUTS</span></span>

### <span data-ttu-id="8f9a2-156">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="8f9a2-156">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>

### <span data-ttu-id="8f9a2-157">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8f9a2-157">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="8f9a2-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f9a2-158">OUTPUTS</span></span>

### <span data-ttu-id="8f9a2-159">Microsoft. Azure. PowerShell. командлеты. NetworkAdmin. Models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="8f9a2-159">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="8f9a2-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f9a2-160">NOTES</span></span>

<span data-ttu-id="8f9a2-161">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-161">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f9a2-162">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8f9a2-163">INPUTOBJECT <INetworkAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="8f9a2-163">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f9a2-164">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="8f9a2-164">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f9a2-165">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-165">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8f9a2-166">`[ResourceName <String>]`: Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-166">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="8f9a2-167">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-167">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8f9a2-168">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-168">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="8f9a2-169">КВОТа <IQuota> : ресурс "Сетевая квота".</span><span class="sxs-lookup"><span data-stu-id="8f9a2-169">QUOTA <IQuota>: Network quota resource.</span></span>
  - <span data-ttu-id="8f9a2-170">`[Tag <IResourceTags>]`: Список пар значений ключа.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-170">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="8f9a2-171">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8f9a2-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Максимальное количество подсистем балансировки нагрузки, которое может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-172">`[MaxLoadBalancersPerSubscription <Int64?>]`: Maximum number of load balancers a tenant subscription can provision.</span></span>
  - <span data-ttu-id="8f9a2-173">`[MaxNicsPerSubscription <Int64?>]`: Максимальное число сетевых адаптеров, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-173">`[MaxNicsPerSubscription <Int64?>]`: Maximum number of NICs a tenant subscription can provision.</span></span>
  - <span data-ttu-id="8f9a2-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Максимальное количество общедоступных IP-адресов, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-174">`[MaxPublicIpsPerSubscription <Int64?>]`: Maximum number of public IP addresses a tenant subscription can provision.</span></span>
  - <span data-ttu-id="8f9a2-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Максимальное количество групп безопасности, которые может подготовить подписка клиента.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-175">`[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximum number of security groups a tenant subscription can provision.</span></span>
  - <span data-ttu-id="8f9a2-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Максимальное количество подключений к шлюзу виртуальной сети, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-176">`[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximum number of virtual network gateway Connections a tenant subscription can provision.</span></span>
  - <span data-ttu-id="8f9a2-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Максимальное число шлюзов виртуальных сетей, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-177">`[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximum number of virtual network gateways a tenant subscription can provision.</span></span>
  - <span data-ttu-id="8f9a2-178">`[MaxVnetsPerSubscription <Int64?>]`: Максимальное количество виртуальных сетей, которые может предоставить подписка на клиент.</span><span class="sxs-lookup"><span data-stu-id="8f9a2-178">`[MaxVnetsPerSubscription <Int64?>]`: Maximum number of virtual networks a tenant subscription can provision.</span></span>

## <span data-ttu-id="8f9a2-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f9a2-179">RELATED LINKS</span></span>

