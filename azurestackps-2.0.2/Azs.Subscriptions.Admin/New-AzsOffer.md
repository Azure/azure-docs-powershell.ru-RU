---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsoffer
schema: 2.0.0
ms.openlocfilehash: 10fbcaf6a8286bf0d7bdeb801ff8797418c91f0f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076665"
---
# <span data-ttu-id="3ab5b-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="3ab5b-101">New-AzsOffer</span></span>

## <span data-ttu-id="3ab5b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ab5b-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab5b-103">Создание или обновление предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-103">Create or update the offer.</span></span>

## <span data-ttu-id="3ab5b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ab5b-104">SYNTAX</span></span>

### <span data-ttu-id="3ab5b-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ab5b-105">CreateExpanded (Default)</span></span>
```
New-AzsOffer -Name <String> -ResourceGroupName <String> -BasePlanIds <String[]> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-Description <String>] [-DisplayName <String>]
 [-ExternalReferenceId <String>] [-Location <String>] [-MaxSubscriptionsPerAccount <Int32>]
 [-PropertiesName <String>] [-State <AccessibilityState>] [-SubscriptionCount <Int32>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ab5b-106">Заново</span><span class="sxs-lookup"><span data-stu-id="3ab5b-106">Create</span></span>
```
New-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ab5b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ab5b-107">DESCRIPTION</span></span>
<span data-ttu-id="3ab5b-108">Создание или обновление предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-108">Create or update the offer.</span></span>

## <span data-ttu-id="3ab5b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ab5b-109">EXAMPLES</span></span>

### <span data-ttu-id="3ab5b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ab5b-110">Example 1</span></span>
```powershell
PS C:\> New-AzsOffer -Name "testoffer" -ResourceGroupName "testrg" -BasePlanIds "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan"

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="3ab5b-111">Создание нового предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-111">Creates a new offer.</span></span>

## <span data-ttu-id="3ab5b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ab5b-112">PARAMETERS</span></span>

### <span data-ttu-id="3ab5b-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="3ab5b-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="3ab5b-114">Ссылки на планы надстроек, с помощью которых клиент может дополнительно получить как часть предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="3ab5b-115">Для конструирования ознакомьтесь с разделом "Заметки" для свойств ADDONPLANDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3ab5b-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="3ab5b-116">-BasePlanIds</span></span>
<span data-ttu-id="3ab5b-117">Идентификаторы базовых планов, которые будут доступны клиенту немедленно, когда клиент подписывается на предложение.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3ab5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab5b-118">-DefaultProfile</span></span>
<span data-ttu-id="3ab5b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ab5b-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="3ab5b-120">-Description</span></span>
<span data-ttu-id="3ab5b-121">Описание предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-121">Description of offer.</span></span>

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

### <span data-ttu-id="3ab5b-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3ab5b-122">-DisplayName</span></span>
<span data-ttu-id="3ab5b-123">Отображаемое имя предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-123">Display name of offer.</span></span>

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

### <span data-ttu-id="3ab5b-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="3ab5b-124">-ExternalReferenceId</span></span>
<span data-ttu-id="3ab5b-125">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-125">External reference identifier.</span></span>

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

### <span data-ttu-id="3ab5b-126">-Location</span><span class="sxs-lookup"><span data-stu-id="3ab5b-126">-Location</span></span>
<span data-ttu-id="3ab5b-127">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="3ab5b-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3ab5b-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="3ab5b-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="3ab5b-129">Максимальное количество подписок на одну учетную запись.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3ab5b-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ab5b-130">-Name</span></span>
<span data-ttu-id="3ab5b-131">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-131">Name of an offer.</span></span>

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

### <span data-ttu-id="3ab5b-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="3ab5b-132">-OfferDefinition</span></span>
<span data-ttu-id="3ab5b-133">Представляет предложение служб, для которых можно создать подписку.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="3ab5b-134">Для конструирования ознакомьтесь с разделом "Заметки" для свойств OFFERDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3ab5b-135">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="3ab5b-135">-PropertiesName</span></span>
<span data-ttu-id="3ab5b-136">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-136">Name of the Offer.</span></span>

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

### <span data-ttu-id="3ab5b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab5b-137">-ResourceGroupName</span></span>
<span data-ttu-id="3ab5b-138">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-138">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3ab5b-139">-State</span><span class="sxs-lookup"><span data-stu-id="3ab5b-139">-State</span></span>
<span data-ttu-id="3ab5b-140">Предоставление поддержки специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Private"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3ab5b-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="3ab5b-141">-SubscriptionCount</span></span>
<span data-ttu-id="3ab5b-142">Текущее число подписок.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3ab5b-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ab5b-143">-SubscriptionId</span></span>
<span data-ttu-id="3ab5b-144">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3ab5b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ab5b-145">-Confirm</span></span>
<span data-ttu-id="3ab5b-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab5b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab5b-147">-WhatIf</span></span>
<span data-ttu-id="3ab5b-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ab5b-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab5b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab5b-150">CommonParameters</span></span>
<span data-ttu-id="3ab5b-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab5b-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ab5b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab5b-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ab5b-153">INPUTS</span></span>

### <span data-ttu-id="3ab5b-154">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="3ab5b-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="3ab5b-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ab5b-155">OUTPUTS</span></span>

### <span data-ttu-id="3ab5b-156">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="3ab5b-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="3ab5b-157">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3ab5b-157">ALIASES</span></span>

## <span data-ttu-id="3ab5b-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ab5b-158">NOTES</span></span>

<span data-ttu-id="3ab5b-159">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ab5b-160">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3ab5b-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: ссылки на планы надстроек, которые клиент может при необходимости получить как часть предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="3ab5b-162">`[MaxAcquisitionCount <Int32?>]`: Максимальное количество экземпляров, которое может быть получено одной подпиской.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="3ab5b-163">Если не указано, предполагается значение 1.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="3ab5b-164">`[PlanId <String>]`: Идентификатор плана.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="3ab5b-165">OFFERDEFINITION <IOffer> : предоставляет предложения служб, для которых можно создать подписку.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="3ab5b-166">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="3ab5b-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="3ab5b-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Ссылки на планы надстроек, которые клиент может дополнительно получить в качестве части предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="3ab5b-168">`[MaxAcquisitionCount <Int32?>]`: Максимальное количество экземпляров, которое может быть получено одной подпиской.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="3ab5b-169">Если не указано, предполагается значение 1.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="3ab5b-170">`[PlanId <String>]`: Идентификатор плана.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="3ab5b-171">`[BasePlanIds <String[]>]`: Идентификаторы базовых планов, которые становятся доступными клиенту немедленно, когда клиент подписывается на предложение.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="3ab5b-172">`[Description <String>]`: Описание предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="3ab5b-173">`[DisplayName <String>]`: Отображаемое название предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="3ab5b-174">`[ExternalReferenceId <String>]`: Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="3ab5b-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Максимальное количество подписок для одной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="3ab5b-176">`[PropertiesName <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="3ab5b-177">`[State <AccessibilityState?>]`: Предлагается состояние специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="3ab5b-178">`[SubscriptionCount <Int32?>]`: Текущее число подписок.</span><span class="sxs-lookup"><span data-stu-id="3ab5b-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="3ab5b-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ab5b-179">RELATED LINKS</span></span>

