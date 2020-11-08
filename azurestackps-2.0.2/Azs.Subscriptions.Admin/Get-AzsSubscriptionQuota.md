---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azssubscriptionquota
schema: 2.0.0
ms.openlocfilehash: 8e1c03393c1d276f5c93425250bf7202e49022d8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077065"
---
# <span data-ttu-id="01b48-101">Get-AzsSubscriptionQuota</span><span class="sxs-lookup"><span data-stu-id="01b48-101">Get-AzsSubscriptionQuota</span></span>

## <span data-ttu-id="01b48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01b48-102">SYNOPSIS</span></span>
<span data-ttu-id="01b48-103">Получает квоту по имени.</span><span class="sxs-lookup"><span data-stu-id="01b48-103">Gets a quota by name.</span></span>

## <span data-ttu-id="01b48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01b48-104">SYNTAX</span></span>

### <span data-ttu-id="01b48-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01b48-105">List (Default)</span></span>
```
Get-AzsSubscriptionQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="01b48-106">Получить</span><span class="sxs-lookup"><span data-stu-id="01b48-106">Get</span></span>
```
Get-AzsSubscriptionQuota -Quota <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="01b48-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="01b48-107">GetViaIdentity</span></span>
```
Get-AzsSubscriptionQuota -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="01b48-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01b48-108">DESCRIPTION</span></span>
<span data-ttu-id="01b48-109">Получает квоту по имени.</span><span class="sxs-lookup"><span data-stu-id="01b48-109">Gets a quota by name.</span></span>

## <span data-ttu-id="01b48-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01b48-110">EXAMPLES</span></span>

### <span data-ttu-id="01b48-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01b48-111">Example 1</span></span>
```powershell

```

<span data-ttu-id="01b48-112">Получите список квот поставщиков ресурсов подписки.</span><span class="sxs-lookup"><span data-stu-id="01b48-112">Get the list of subscription resource provider quotas.</span></span>

## <span data-ttu-id="01b48-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01b48-113">PARAMETERS</span></span>

### <span data-ttu-id="01b48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b48-114">-DefaultProfile</span></span>
<span data-ttu-id="01b48-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01b48-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01b48-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01b48-116">-InputObject</span></span>
<span data-ttu-id="01b48-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="01b48-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="01b48-118">-Location</span><span class="sxs-lookup"><span data-stu-id="01b48-118">-Location</span></span>
<span data-ttu-id="01b48-119">Расположение AzureStack.</span><span class="sxs-lookup"><span data-stu-id="01b48-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="01b48-120">-Quota</span><span class="sxs-lookup"><span data-stu-id="01b48-120">-Quota</span></span>
<span data-ttu-id="01b48-121">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="01b48-121">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="01b48-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01b48-122">-SubscriptionId</span></span>
<span data-ttu-id="01b48-123">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="01b48-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="01b48-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b48-124">CommonParameters</span></span>
<span data-ttu-id="01b48-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01b48-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b48-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01b48-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b48-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01b48-127">INPUTS</span></span>

### <span data-ttu-id="01b48-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="01b48-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="01b48-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01b48-129">OUTPUTS</span></span>

### <span data-ttu-id="01b48-130">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IQuota</span><span class="sxs-lookup"><span data-stu-id="01b48-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IQuota</span></span>

<span data-ttu-id="01b48-131">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="01b48-131">ALIASES</span></span>

<span data-ttu-id="01b48-132">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="01b48-132">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="01b48-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="01b48-133">NOTES</span></span>

<span data-ttu-id="01b48-134">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="01b48-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01b48-135">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01b48-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="01b48-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="01b48-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01b48-137">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="01b48-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="01b48-138">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="01b48-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="01b48-139">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="01b48-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01b48-140">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="01b48-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="01b48-141">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="01b48-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="01b48-142">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="01b48-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="01b48-143">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="01b48-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="01b48-144">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="01b48-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="01b48-145">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="01b48-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="01b48-146">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="01b48-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="01b48-147">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="01b48-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="01b48-148">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="01b48-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="01b48-149">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="01b48-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="01b48-150">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="01b48-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="01b48-151">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="01b48-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="01b48-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01b48-152">RELATED LINKS</span></span>

