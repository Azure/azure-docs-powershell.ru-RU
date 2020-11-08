---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077157"
---
# <span data-ttu-id="9790c-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="9790c-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="9790c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9790c-102">SYNOPSIS</span></span>
<span data-ttu-id="9790c-103">Создает или обновляет указанную подписку.</span><span class="sxs-lookup"><span data-stu-id="9790c-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="9790c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9790c-104">SYNTAX</span></span>

### <span data-ttu-id="9790c-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9790c-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9790c-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="9790c-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9790c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9790c-107">DESCRIPTION</span></span>
<span data-ttu-id="9790c-108">Создает или обновляет указанную подписку.</span><span class="sxs-lookup"><span data-stu-id="9790c-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="9790c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9790c-109">EXAMPLES</span></span>

### <span data-ttu-id="9790c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9790c-110">Example 1</span></span>
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

<span data-ttu-id="9790c-111">Обновляет подписку</span><span class="sxs-lookup"><span data-stu-id="9790c-111">Updates a subscription</span></span>

## <span data-ttu-id="9790c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9790c-112">PARAMETERS</span></span>

### <span data-ttu-id="9790c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9790c-113">-DefaultProfile</span></span>
<span data-ttu-id="9790c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9790c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9790c-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9790c-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="9790c-116">Идентификатор родительской подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="9790c-116">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="9790c-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9790c-117">-DisplayName</span></span>
<span data-ttu-id="9790c-118">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="9790c-118">Subscription name.</span></span>

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

### <span data-ttu-id="9790c-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="9790c-119">-ExternalReferenceId</span></span>
<span data-ttu-id="9790c-120">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="9790c-120">External reference identifier.</span></span>

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

### <span data-ttu-id="9790c-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9790c-121">-Id</span></span>
<span data-ttu-id="9790c-122">Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9790c-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="9790c-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="9790c-123">-OfferId</span></span>
<span data-ttu-id="9790c-124">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="9790c-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="9790c-125">-Владелец</span><span class="sxs-lookup"><span data-stu-id="9790c-125">-Owner</span></span>
<span data-ttu-id="9790c-126">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="9790c-126">Subscription owner.</span></span>

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

### <span data-ttu-id="9790c-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="9790c-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="9790c-128">Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="9790c-128">Routing resource manager type.</span></span>

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

### <span data-ttu-id="9790c-129">-State</span><span class="sxs-lookup"><span data-stu-id="9790c-129">-State</span></span>
<span data-ttu-id="9790c-130">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="9790c-130">Subscription state.</span></span>

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

### <span data-ttu-id="9790c-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="9790c-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="9790c-132">Свойства объекта подписку.</span><span class="sxs-lookup"><span data-stu-id="9790c-132">Subscription object properties.</span></span>
<span data-ttu-id="9790c-133">Для конструирования ознакомьтесь с разделом "Заметки" для свойств SUBSCRIPTIONDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9790c-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

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

### <span data-ttu-id="9790c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9790c-134">-SubscriptionId</span></span>
<span data-ttu-id="9790c-135">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="9790c-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9790c-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="9790c-136">-SubscriptionId1</span></span>
<span data-ttu-id="9790c-137">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="9790c-137">Subscription identifier.</span></span>

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

### <span data-ttu-id="9790c-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9790c-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="9790c-139">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9790c-139">The target subscription ID.</span></span>

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

### <span data-ttu-id="9790c-140">-TenantId</span><span class="sxs-lookup"><span data-stu-id="9790c-140">-TenantId</span></span>
<span data-ttu-id="9790c-141">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="9790c-141">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="9790c-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9790c-142">-Confirm</span></span>
<span data-ttu-id="9790c-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9790c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9790c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9790c-144">-WhatIf</span></span>
<span data-ttu-id="9790c-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9790c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9790c-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9790c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9790c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9790c-147">CommonParameters</span></span>
<span data-ttu-id="9790c-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9790c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9790c-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9790c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9790c-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9790c-150">INPUTS</span></span>

### <span data-ttu-id="9790c-151">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="9790c-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="9790c-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9790c-152">OUTPUTS</span></span>

### <span data-ttu-id="9790c-153">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="9790c-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="9790c-154">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9790c-154">ALIASES</span></span>

## <span data-ttu-id="9790c-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="9790c-155">NOTES</span></span>

<span data-ttu-id="9790c-156">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9790c-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9790c-157">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9790c-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9790c-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : свойства объекта Subscription.</span><span class="sxs-lookup"><span data-stu-id="9790c-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="9790c-159">`[DelegatedProviderSubscriptionId <String>]`: Родительский идентификатор подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="9790c-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="9790c-160">`[DisplayName <String>]`: Имя подписки.</span><span class="sxs-lookup"><span data-stu-id="9790c-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="9790c-161">`[ExternalReferenceId <String>]`: Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="9790c-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="9790c-162">`[Id <String>]`: Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="9790c-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="9790c-163">`[OfferId <String>]`: Идентификатор предложения в рамках области поставщика с делегированными полномочиями.</span><span class="sxs-lookup"><span data-stu-id="9790c-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="9790c-164">`[Owner <String>]`: Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="9790c-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="9790c-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="9790c-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="9790c-166">`[State <SubscriptionState?>]`: Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="9790c-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="9790c-167">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="9790c-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="9790c-168">`[TenantId <String>]`: Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="9790c-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="9790c-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9790c-169">RELATED LINKS</span></span>

