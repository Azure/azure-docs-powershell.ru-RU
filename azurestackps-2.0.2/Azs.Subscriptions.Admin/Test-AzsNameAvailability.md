---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077144"
---
# <span data-ttu-id="93727-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="93727-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="93727-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93727-102">SYNOPSIS</span></span>
<span data-ttu-id="93727-103">Получение списка подписок.</span><span class="sxs-lookup"><span data-stu-id="93727-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="93727-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93727-104">SYNTAX</span></span>

### <span data-ttu-id="93727-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93727-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93727-106">Определить</span><span class="sxs-lookup"><span data-stu-id="93727-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93727-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93727-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93727-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="93727-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93727-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93727-109">DESCRIPTION</span></span>
<span data-ttu-id="93727-110">Получение списка подписок.</span><span class="sxs-lookup"><span data-stu-id="93727-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="93727-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93727-111">EXAMPLES</span></span>

### <span data-ttu-id="93727-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93727-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="93727-113">Возвращает доступность указанного типа и имени ресурса подписки.</span><span class="sxs-lookup"><span data-stu-id="93727-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="93727-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93727-114">PARAMETERS</span></span>

### <span data-ttu-id="93727-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93727-115">-DefaultProfile</span></span>
<span data-ttu-id="93727-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93727-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93727-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93727-117">-InputObject</span></span>
<span data-ttu-id="93727-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="93727-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="93727-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93727-119">-Name</span></span>
<span data-ttu-id="93727-120">Имя проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="93727-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="93727-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="93727-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="93727-122">Определение действия "Проверка наличия имени".</span><span class="sxs-lookup"><span data-stu-id="93727-122">The check name availability action definition.</span></span>
<span data-ttu-id="93727-123">Для конструирования ознакомьтесь с разделом "Заметки" для свойств NAMEAVAILABILITYDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="93727-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="93727-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="93727-124">-ResourceType</span></span>
<span data-ttu-id="93727-125">Тип проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="93727-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="93727-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93727-126">-SubscriptionId</span></span>
<span data-ttu-id="93727-127">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="93727-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="93727-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93727-128">-Confirm</span></span>
<span data-ttu-id="93727-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93727-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93727-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93727-130">-WhatIf</span></span>
<span data-ttu-id="93727-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93727-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93727-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93727-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93727-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93727-133">CommonParameters</span></span>
<span data-ttu-id="93727-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93727-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93727-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93727-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93727-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93727-136">INPUTS</span></span>

### <span data-ttu-id="93727-137">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="93727-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="93727-138">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="93727-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="93727-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93727-139">OUTPUTS</span></span>

### <span data-ttu-id="93727-140">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="93727-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="93727-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="93727-141">ALIASES</span></span>

## <span data-ttu-id="93727-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="93727-142">NOTES</span></span>

<span data-ttu-id="93727-143">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="93727-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93727-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93727-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="93727-145">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="93727-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93727-146">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="93727-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="93727-147">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="93727-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="93727-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="93727-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93727-149">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="93727-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="93727-150">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="93727-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="93727-151">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="93727-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="93727-152">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="93727-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="93727-153">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="93727-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="93727-154">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="93727-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="93727-155">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="93727-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="93727-156">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="93727-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="93727-157">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="93727-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="93727-158">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="93727-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="93727-159">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="93727-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="93727-160">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="93727-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="93727-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> : определение действия "Проверка наличия имени".</span><span class="sxs-lookup"><span data-stu-id="93727-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="93727-162">`[Name <String>]`: Имя ресурса для проверки.</span><span class="sxs-lookup"><span data-stu-id="93727-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="93727-163">`[ResourceType <String>]`: Тип проверяемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="93727-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="93727-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93727-164">RELATED LINKS</span></span>
