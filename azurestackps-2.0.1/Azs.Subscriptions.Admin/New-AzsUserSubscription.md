---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075179"
---
# <span data-ttu-id="c264e-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="c264e-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="c264e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c264e-102">SYNOPSIS</span></span>
<span data-ttu-id="c264e-103">Создает или обновляет указанную подписку.</span><span class="sxs-lookup"><span data-stu-id="c264e-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="c264e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c264e-104">SYNTAX</span></span>

### <span data-ttu-id="c264e-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c264e-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c264e-106">Заново</span><span class="sxs-lookup"><span data-stu-id="c264e-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c264e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c264e-107">DESCRIPTION</span></span>
<span data-ttu-id="c264e-108">Создает или обновляет указанную подписку.</span><span class="sxs-lookup"><span data-stu-id="c264e-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="c264e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c264e-109">EXAMPLES</span></span>

### <span data-ttu-id="c264e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c264e-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="c264e-111">Создает новую подписку пользователя</span><span class="sxs-lookup"><span data-stu-id="c264e-111">Creates a new user subscription</span></span>

## <span data-ttu-id="c264e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c264e-112">PARAMETERS</span></span>

### <span data-ttu-id="c264e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c264e-113">-DefaultProfile</span></span>
<span data-ttu-id="c264e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c264e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c264e-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c264e-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="c264e-116">Идентификатор родительской подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="c264e-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c264e-117">-DisplayName</span></span>
<span data-ttu-id="c264e-118">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="c264e-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="c264e-119">-ExternalReferenceId</span></span>
<span data-ttu-id="c264e-120">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="c264e-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-121">-ID</span><span class="sxs-lookup"><span data-stu-id="c264e-121">-Id</span></span>
<span data-ttu-id="c264e-122">Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c264e-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="c264e-123">-OfferId</span></span>
<span data-ttu-id="c264e-124">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="c264e-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-125">-Владелец</span><span class="sxs-lookup"><span data-stu-id="c264e-125">-Owner</span></span>
<span data-ttu-id="c264e-126">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="c264e-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="c264e-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="c264e-128">Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c264e-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-129">-State</span><span class="sxs-lookup"><span data-stu-id="c264e-129">-State</span></span>
<span data-ttu-id="c264e-130">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="c264e-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="c264e-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="c264e-132">Свойства объекта подписку.</span><span class="sxs-lookup"><span data-stu-id="c264e-132">Subscription object properties.</span></span>
<span data-ttu-id="c264e-133">Для конструирования ознакомьтесь с разделом "Заметки" для свойств SUBSCRIPTIONDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c264e-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c264e-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="c264e-135">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c264e-135">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="c264e-136">-TenantId</span></span>
<span data-ttu-id="c264e-137">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="c264e-137">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c264e-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c264e-138">-Confirm</span></span>
<span data-ttu-id="c264e-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c264e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c264e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c264e-140">-WhatIf</span></span>
<span data-ttu-id="c264e-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c264e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c264e-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c264e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c264e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c264e-143">CommonParameters</span></span>
<span data-ttu-id="c264e-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c264e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c264e-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c264e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c264e-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c264e-146">INPUTS</span></span>

### <span data-ttu-id="c264e-147">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="c264e-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="c264e-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c264e-148">OUTPUTS</span></span>

### <span data-ttu-id="c264e-149">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="c264e-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="c264e-150">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c264e-150">ALIASES</span></span>

## <span data-ttu-id="c264e-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="c264e-151">NOTES</span></span>

<span data-ttu-id="c264e-152">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c264e-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c264e-153">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c264e-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c264e-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : свойства объекта Subscription.</span><span class="sxs-lookup"><span data-stu-id="c264e-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="c264e-155">`[DelegatedProviderSubscriptionId <String>]`: Родительский идентификатор подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="c264e-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="c264e-156">`[DisplayName <String>]`: Имя подписки.</span><span class="sxs-lookup"><span data-stu-id="c264e-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="c264e-157">`[ExternalReferenceId <String>]`: Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="c264e-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="c264e-158">`[Id <String>]`: Полный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c264e-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="c264e-159">`[OfferId <String>]`: Идентификатор предложения в рамках области поставщика с делегированными полномочиями.</span><span class="sxs-lookup"><span data-stu-id="c264e-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="c264e-160">`[Owner <String>]`: Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="c264e-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="c264e-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c264e-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="c264e-162">`[State <SubscriptionState?>]`: Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="c264e-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="c264e-163">`[SubscriptionId <String>]`: Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="c264e-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="c264e-164">`[TenantId <String>]`: Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="c264e-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="c264e-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c264e-165">RELATED LINKS</span></span>

