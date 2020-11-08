---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075251"
---
# <span data-ttu-id="139d4-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="139d4-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="139d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="139d4-102">SYNOPSIS</span></span>
<span data-ttu-id="139d4-103">Создает или обновляет указанную подписку.</span><span class="sxs-lookup"><span data-stu-id="139d4-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="139d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="139d4-104">SYNTAX</span></span>

### <span data-ttu-id="139d4-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="139d4-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="139d4-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="139d4-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="139d4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="139d4-107">DESCRIPTION</span></span>
<span data-ttu-id="139d4-108">Создает или обновляет указанную подписку.</span><span class="sxs-lookup"><span data-stu-id="139d4-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="139d4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="139d4-109">EXAMPLES</span></span>

### <span data-ttu-id="139d4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="139d4-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="139d4-111">Обновляет подписку</span><span class="sxs-lookup"><span data-stu-id="139d4-111">Updates a subscription</span></span>

## <span data-ttu-id="139d4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="139d4-112">PARAMETERS</span></span>

### <span data-ttu-id="139d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="139d4-113">-DefaultProfile</span></span>
<span data-ttu-id="139d4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="139d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="139d4-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="139d4-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="139d4-116">Идентификатор родительской подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="139d4-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="139d4-117">-DisplayName</span></span>
<span data-ttu-id="139d4-118">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="139d4-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="139d4-119">-ExternalReferenceId</span></span>
<span data-ttu-id="139d4-120">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="139d4-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-121">-ID</span><span class="sxs-lookup"><span data-stu-id="139d4-121">-Id</span></span>
<span data-ttu-id="139d4-122">Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="139d4-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="139d4-123">-OfferId</span></span>
<span data-ttu-id="139d4-124">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="139d4-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-125">-Владелец</span><span class="sxs-lookup"><span data-stu-id="139d4-125">-Owner</span></span>
<span data-ttu-id="139d4-126">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="139d4-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="139d4-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="139d4-128">Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="139d4-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-129">-State</span><span class="sxs-lookup"><span data-stu-id="139d4-129">-State</span></span>
<span data-ttu-id="139d4-130">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="139d4-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="139d4-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="139d4-132">Свойства объекта подписку.</span><span class="sxs-lookup"><span data-stu-id="139d4-132">Subscription object properties.</span></span>
<span data-ttu-id="139d4-133">Для конструирования ознакомьтесь с разделом "Заметки" для свойств SUBSCRIPTIONDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="139d4-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="139d4-134">-SubscriptionId</span></span>
<span data-ttu-id="139d4-135">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="139d4-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="139d4-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="139d4-136">-SubscriptionId1</span></span>
<span data-ttu-id="139d4-137">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="139d4-137">Subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="139d4-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="139d4-139">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="139d4-139">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-140">-TenantId</span><span class="sxs-lookup"><span data-stu-id="139d4-140">-TenantId</span></span>
<span data-ttu-id="139d4-141">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="139d4-141">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="139d4-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="139d4-142">-Confirm</span></span>
<span data-ttu-id="139d4-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="139d4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="139d4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="139d4-144">-WhatIf</span></span>
<span data-ttu-id="139d4-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="139d4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="139d4-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="139d4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="139d4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="139d4-147">CommonParameters</span></span>
<span data-ttu-id="139d4-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="139d4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="139d4-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="139d4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="139d4-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="139d4-150">INPUTS</span></span>

### <span data-ttu-id="139d4-151">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="139d4-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="139d4-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="139d4-152">OUTPUTS</span></span>

### <span data-ttu-id="139d4-153">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="139d4-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="139d4-154">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="139d4-154">ALIASES</span></span>

## <span data-ttu-id="139d4-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="139d4-155">NOTES</span></span>

<span data-ttu-id="139d4-156">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="139d4-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="139d4-157">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="139d4-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="139d4-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : свойства объекта Subscription.</span><span class="sxs-lookup"><span data-stu-id="139d4-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="139d4-159">`[DelegatedProviderSubscriptionId <String>]`: Родительский идентификатор подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="139d4-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="139d4-160">`[DisplayName <String>]`: Имя подписки.</span><span class="sxs-lookup"><span data-stu-id="139d4-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="139d4-161">`[ExternalReferenceId <String>]`: Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="139d4-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="139d4-162">`[Id <String>]`: Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="139d4-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="139d4-163">`[OfferId <String>]`: Идентификатор предложения в рамках области поставщика с делегированными полномочиями.</span><span class="sxs-lookup"><span data-stu-id="139d4-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="139d4-164">`[Owner <String>]`: Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="139d4-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="139d4-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="139d4-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="139d4-166">`[State <SubscriptionState?>]`: Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="139d4-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="139d4-167">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="139d4-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="139d4-168">`[TenantId <String>]`: Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="139d4-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="139d4-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="139d4-169">RELATED LINKS</span></span>

