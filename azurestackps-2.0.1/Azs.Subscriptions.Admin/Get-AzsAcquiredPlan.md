---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075157"
---
# <span data-ttu-id="d8460-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="d8460-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="d8460-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8460-102">SYNOPSIS</span></span>
<span data-ttu-id="d8460-103">Получает указанный план, полученный подпиской, которая потребляет предложение.</span><span class="sxs-lookup"><span data-stu-id="d8460-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="d8460-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8460-104">SYNTAX</span></span>

### <span data-ttu-id="d8460-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8460-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8460-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d8460-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d8460-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8460-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8460-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8460-108">DESCRIPTION</span></span>
<span data-ttu-id="d8460-109">Получает указанный план, полученный подпиской, которая потребляет предложение.</span><span class="sxs-lookup"><span data-stu-id="d8460-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="d8460-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8460-110">EXAMPLES</span></span>

### <span data-ttu-id="d8460-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8460-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="d8460-112">Получение коллекции всех приобретенных планов, к которым у подписки есть доступ.</span><span class="sxs-lookup"><span data-stu-id="d8460-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="d8460-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8460-113">PARAMETERS</span></span>

### <span data-ttu-id="d8460-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8460-114">-DefaultProfile</span></span>
<span data-ttu-id="d8460-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8460-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8460-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8460-116">-InputObject</span></span>
<span data-ttu-id="d8460-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d8460-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8460-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="d8460-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="d8460-119">Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="d8460-119">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="d8460-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8460-120">-SubscriptionId</span></span>
<span data-ttu-id="d8460-121">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d8460-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d8460-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8460-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="d8460-123">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d8460-123">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d8460-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8460-124">CommonParameters</span></span>
<span data-ttu-id="d8460-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8460-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8460-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8460-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8460-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8460-127">INPUTS</span></span>

### <span data-ttu-id="d8460-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d8460-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="d8460-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8460-129">OUTPUTS</span></span>

### <span data-ttu-id="d8460-130">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="d8460-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="d8460-131">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d8460-131">ALIASES</span></span>

<span data-ttu-id="d8460-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="d8460-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="d8460-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8460-133">NOTES</span></span>

<span data-ttu-id="d8460-134">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d8460-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8460-135">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8460-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d8460-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d8460-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8460-137">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="d8460-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="d8460-138">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="d8460-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="d8460-139">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d8460-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8460-140">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="d8460-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="d8460-141">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="d8460-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="d8460-142">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="d8460-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="d8460-143">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="d8460-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="d8460-144">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="d8460-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="d8460-145">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="d8460-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="d8460-146">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="d8460-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="d8460-147">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="d8460-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d8460-148">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="d8460-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="d8460-149">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d8460-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d8460-150">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d8460-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="d8460-151">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="d8460-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="d8460-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8460-152">RELATED LINKS</span></span>

