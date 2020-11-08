---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplanfromoffer
schema: 2.0.0
ms.openlocfilehash: c3a68c028abc9033cef9d9fd7e8fbd39e4066d2d
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94075110"
---
# <span data-ttu-id="5b5d1-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="5b5d1-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="5b5d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5d1-103">Удаление связи плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="5b5d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b5d1-104">SYNTAX</span></span>

### <span data-ttu-id="5b5d1-105">UnlinkExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b5d1-105">UnlinkExpanded (Default)</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5b5d1-106">Удалить связь</span><span class="sxs-lookup"><span data-stu-id="5b5d1-106">Unlink</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5b5d1-107">UnlinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5b5d1-107">UnlinkViaIdentity</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5b5d1-108">UnlinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5b5d1-108">UnlinkViaIdentityExpanded</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5b5d1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b5d1-109">DESCRIPTION</span></span>
<span data-ttu-id="5b5d1-110">Удаление связи плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-110">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="5b5d1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b5d1-111">EXAMPLES</span></span>

### <span data-ttu-id="5b5d1-112">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="5b5d1-112">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsPlanFromOffer -PlanName "testplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="5b5d1-113">Удаление связи плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-113">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="5b5d1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b5d1-114">PARAMETERS</span></span>

### <span data-ttu-id="5b5d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b5d1-115">-DefaultProfile</span></span>
<span data-ttu-id="5b5d1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b5d1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b5d1-117">-InputObject</span></span>
<span data-ttu-id="5b5d1-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: UnlinkViaIdentity, UnlinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5b5d1-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="5b5d1-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="5b5d1-120">Максимальное количество приобретений для подписчиков</span><span class="sxs-lookup"><span data-stu-id="5b5d1-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b5d1-121">-OfferName</span><span class="sxs-lookup"><span data-stu-id="5b5d1-121">-OfferName</span></span>
<span data-ttu-id="5b5d1-122">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b5d1-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="5b5d1-123">-PlanLink</span></span>
<span data-ttu-id="5b5d1-124">Определение для связывания и разрыва связей между планами и предложением.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="5b5d1-125">Для конструирования ознакомьтесь с разделом "Заметки" для свойств PLANLINK и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Unlink, UnlinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="5b5d1-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="5b5d1-126">-PlanLinkType</span></span>
<span data-ttu-id="5b5d1-127">Тип ссылки на план.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b5d1-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="5b5d1-128">-PlanName</span></span>
<span data-ttu-id="5b5d1-129">Название плана.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b5d1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b5d1-130">-ResourceGroupName</span></span>
<span data-ttu-id="5b5d1-131">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b5d1-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b5d1-132">-SubscriptionId</span></span>
<span data-ttu-id="5b5d1-133">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5b5d1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b5d1-134">-Confirm</span></span>
<span data-ttu-id="5b5d1-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b5d1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b5d1-136">-WhatIf</span></span>
<span data-ttu-id="5b5d1-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b5d1-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b5d1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b5d1-139">CommonParameters</span></span>
<span data-ttu-id="5b5d1-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b5d1-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b5d1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b5d1-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b5d1-142">INPUTS</span></span>

### <span data-ttu-id="5b5d1-143">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="5b5d1-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="5b5d1-144">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5b5d1-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="5b5d1-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b5d1-145">OUTPUTS</span></span>

### <span data-ttu-id="5b5d1-146">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="5b5d1-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="5b5d1-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5b5d1-147">ALIASES</span></span>

## <span data-ttu-id="5b5d1-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b5d1-148">NOTES</span></span>

<span data-ttu-id="5b5d1-149">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b5d1-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5b5d1-151">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="5b5d1-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b5d1-152">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="5b5d1-153">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="5b5d1-154">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="5b5d1-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b5d1-155">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="5b5d1-156">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="5b5d1-157">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="5b5d1-158">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="5b5d1-159">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="5b5d1-160">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="5b5d1-161">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="5b5d1-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="5b5d1-162">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="5b5d1-163">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="5b5d1-164">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5b5d1-165">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="5b5d1-166">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="5b5d1-167">PLANLINK <IPlanLinkDefinition> : определение для связывания и разрыва связей между планами и предложением.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="5b5d1-168">`[MaxAcquisitionCount <Int32?>]`: Максимальное количество приобретений для подписчиков</span><span class="sxs-lookup"><span data-stu-id="5b5d1-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="5b5d1-169">`[PlanLinkType <PlanLinkType?>]`: Тип ссылки на план.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="5b5d1-170">`[PlanName <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="5b5d1-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b5d1-171">RELATED LINKS</span></span>

