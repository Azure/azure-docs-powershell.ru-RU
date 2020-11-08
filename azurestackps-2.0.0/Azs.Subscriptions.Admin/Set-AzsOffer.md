---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94075108"
---
# <span data-ttu-id="d9f33-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="d9f33-101">Set-AzsOffer</span></span>

## <span data-ttu-id="d9f33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9f33-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f33-103">Создание или обновление предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-103">Create or update the offer.</span></span>

## <span data-ttu-id="d9f33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9f33-104">SYNTAX</span></span>

### <span data-ttu-id="d9f33-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9f33-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d9f33-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="d9f33-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9f33-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9f33-107">DESCRIPTION</span></span>
<span data-ttu-id="d9f33-108">Создание или обновление предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-108">Create or update the offer.</span></span>

## <span data-ttu-id="d9f33-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9f33-109">EXAMPLES</span></span>

### <span data-ttu-id="d9f33-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9f33-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="d9f33-111">Обновление предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-111">Update an offer.</span></span>

## <span data-ttu-id="d9f33-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9f33-112">PARAMETERS</span></span>

### <span data-ttu-id="d9f33-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="d9f33-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="d9f33-114">Ссылки на планы надстроек, с помощью которых клиент может дополнительно получить как часть предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="d9f33-115">Для конструирования ознакомьтесь с разделом "Заметки" для свойств ADDONPLANDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d9f33-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9f33-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="d9f33-116">-BasePlanIds</span></span>
<span data-ttu-id="d9f33-117">Идентификаторы базовых планов, которые будут доступны клиенту немедленно, когда клиент подписывается на предложение.</span><span class="sxs-lookup"><span data-stu-id="d9f33-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9f33-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f33-118">-DefaultProfile</span></span>
<span data-ttu-id="d9f33-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9f33-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9f33-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="d9f33-120">-Description</span></span>
<span data-ttu-id="d9f33-121">Описание предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-121">Description of offer.</span></span>

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

### <span data-ttu-id="d9f33-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d9f33-122">-DisplayName</span></span>
<span data-ttu-id="d9f33-123">Отображаемое имя предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-123">Display name of offer.</span></span>

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

### <span data-ttu-id="d9f33-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="d9f33-124">-ExternalReferenceId</span></span>
<span data-ttu-id="d9f33-125">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="d9f33-125">External reference identifier.</span></span>

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

### <span data-ttu-id="d9f33-126">-Location</span><span class="sxs-lookup"><span data-stu-id="d9f33-126">-Location</span></span>
<span data-ttu-id="d9f33-127">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="d9f33-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9f33-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="d9f33-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="d9f33-129">Максимальное количество подписок на одну учетную запись.</span><span class="sxs-lookup"><span data-stu-id="d9f33-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9f33-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d9f33-130">-Name</span></span>
<span data-ttu-id="d9f33-131">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-131">Name of an offer.</span></span>

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

### <span data-ttu-id="d9f33-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="d9f33-132">-OfferDefinition</span></span>
<span data-ttu-id="d9f33-133">Представляет предложение служб, для которых можно создать подписку.</span><span class="sxs-lookup"><span data-stu-id="d9f33-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="d9f33-134">Для конструирования ознакомьтесь с разделом "Заметки" для свойств OFFERDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d9f33-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d9f33-135">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="d9f33-135">-PropertiesName</span></span>
<span data-ttu-id="d9f33-136">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-136">Name of the Offer.</span></span>

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

### <span data-ttu-id="d9f33-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f33-137">-ResourceGroupName</span></span>
<span data-ttu-id="d9f33-138">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="d9f33-138">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d9f33-139">-State</span><span class="sxs-lookup"><span data-stu-id="d9f33-139">-State</span></span>
<span data-ttu-id="d9f33-140">Предоставление поддержки специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="d9f33-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9f33-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="d9f33-141">-SubscriptionCount</span></span>
<span data-ttu-id="d9f33-142">Текущее число подписок.</span><span class="sxs-lookup"><span data-stu-id="d9f33-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d9f33-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9f33-143">-SubscriptionId</span></span>
<span data-ttu-id="d9f33-144">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d9f33-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9f33-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9f33-145">-Confirm</span></span>
<span data-ttu-id="d9f33-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9f33-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f33-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9f33-147">-WhatIf</span></span>
<span data-ttu-id="d9f33-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9f33-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9f33-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9f33-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9f33-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f33-150">CommonParameters</span></span>
<span data-ttu-id="d9f33-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9f33-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f33-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9f33-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f33-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9f33-153">INPUTS</span></span>

### <span data-ttu-id="d9f33-154">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="d9f33-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="d9f33-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9f33-155">OUTPUTS</span></span>

### <span data-ttu-id="d9f33-156">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="d9f33-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="d9f33-157">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d9f33-157">ALIASES</span></span>

## <span data-ttu-id="d9f33-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9f33-158">NOTES</span></span>

<span data-ttu-id="d9f33-159">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d9f33-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d9f33-160">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d9f33-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d9f33-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: ссылки на планы надстроек, которые клиент может при необходимости получить как часть предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="d9f33-162">`[MaxAcquisitionCount <Int32?>]`: Максимальное количество экземпляров, которое может быть получено одной подпиской.</span><span class="sxs-lookup"><span data-stu-id="d9f33-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="d9f33-163">Если не указано, предполагается значение 1.</span><span class="sxs-lookup"><span data-stu-id="d9f33-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="d9f33-164">`[PlanId <String>]`: Идентификатор плана.</span><span class="sxs-lookup"><span data-stu-id="d9f33-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="d9f33-165">OFFERDEFINITION <IOffer> : предоставляет предложения служб, для которых можно создать подписку.</span><span class="sxs-lookup"><span data-stu-id="d9f33-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="d9f33-166">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="d9f33-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="d9f33-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Ссылки на планы надстроек, которые клиент может дополнительно получить в качестве части предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="d9f33-168">`[MaxAcquisitionCount <Int32?>]`: Максимальное количество экземпляров, которое может быть получено одной подпиской.</span><span class="sxs-lookup"><span data-stu-id="d9f33-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="d9f33-169">Если не указано, предполагается значение 1.</span><span class="sxs-lookup"><span data-stu-id="d9f33-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="d9f33-170">`[PlanId <String>]`: Идентификатор плана.</span><span class="sxs-lookup"><span data-stu-id="d9f33-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="d9f33-171">`[BasePlanIds <String[]>]`: Идентификаторы базовых планов, которые становятся доступными клиенту немедленно, когда клиент подписывается на предложение.</span><span class="sxs-lookup"><span data-stu-id="d9f33-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="d9f33-172">`[Description <String>]`: Описание предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="d9f33-173">`[DisplayName <String>]`: Отображаемое название предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="d9f33-174">`[ExternalReferenceId <String>]`: Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="d9f33-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="d9f33-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Максимальное количество подписок для одной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d9f33-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="d9f33-176">`[PropertiesName <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="d9f33-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="d9f33-177">`[State <AccessibilityState?>]`: Предлагается состояние специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="d9f33-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="d9f33-178">`[SubscriptionCount <Int32?>]`: Текущее число подписок.</span><span class="sxs-lookup"><span data-stu-id="d9f33-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="d9f33-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9f33-179">RELATED LINKS</span></span>

