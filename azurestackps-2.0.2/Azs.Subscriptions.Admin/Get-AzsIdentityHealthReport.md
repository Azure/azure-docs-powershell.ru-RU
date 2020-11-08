---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077117"
---
# <span data-ttu-id="feec2-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="feec2-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="feec2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="feec2-102">SYNOPSIS</span></span>
<span data-ttu-id="feec2-103">Проверка работоспособности удостоверения</span><span class="sxs-lookup"><span data-stu-id="feec2-103">Checks the identity health</span></span>

## <span data-ttu-id="feec2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="feec2-104">SYNTAX</span></span>

### <span data-ttu-id="feec2-105">Проверка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="feec2-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="feec2-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="feec2-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="feec2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="feec2-107">DESCRIPTION</span></span>
<span data-ttu-id="feec2-108">Проверка работоспособности удостоверения</span><span class="sxs-lookup"><span data-stu-id="feec2-108">Checks the identity health</span></span>

## <span data-ttu-id="feec2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="feec2-109">EXAMPLES</span></span>

### <span data-ttu-id="feec2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="feec2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="feec2-111">Получение состояния работоспособности удостоверения.</span><span class="sxs-lookup"><span data-stu-id="feec2-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="feec2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="feec2-112">PARAMETERS</span></span>

### <span data-ttu-id="feec2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feec2-113">-DefaultProfile</span></span>
<span data-ttu-id="feec2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="feec2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feec2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feec2-115">-InputObject</span></span>
<span data-ttu-id="feec2-116">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="feec2-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="feec2-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="feec2-117">-SubscriptionId</span></span>
<span data-ttu-id="feec2-118">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="feec2-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="feec2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="feec2-119">-Confirm</span></span>
<span data-ttu-id="feec2-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="feec2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feec2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feec2-121">-WhatIf</span></span>
<span data-ttu-id="feec2-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="feec2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feec2-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="feec2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feec2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feec2-124">CommonParameters</span></span>
<span data-ttu-id="feec2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="feec2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feec2-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="feec2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feec2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="feec2-127">INPUTS</span></span>

### <span data-ttu-id="feec2-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="feec2-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="feec2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="feec2-129">OUTPUTS</span></span>

### <span data-ttu-id="feec2-130">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IIdentityHealthCheckReportDefinition</span><span class="sxs-lookup"><span data-stu-id="feec2-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="feec2-131">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="feec2-131">ALIASES</span></span>

## <span data-ttu-id="feec2-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="feec2-132">NOTES</span></span>

<span data-ttu-id="feec2-133">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="feec2-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="feec2-134">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="feec2-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="feec2-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="feec2-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="feec2-136">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="feec2-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="feec2-137">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="feec2-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="feec2-138">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="feec2-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="feec2-139">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="feec2-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="feec2-140">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="feec2-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="feec2-141">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="feec2-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="feec2-142">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="feec2-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="feec2-143">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="feec2-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="feec2-144">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="feec2-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="feec2-145">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="feec2-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="feec2-146">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="feec2-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="feec2-147">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="feec2-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="feec2-148">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="feec2-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="feec2-149">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="feec2-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="feec2-150">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="feec2-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="feec2-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="feec2-151">RELATED LINKS</span></span>
