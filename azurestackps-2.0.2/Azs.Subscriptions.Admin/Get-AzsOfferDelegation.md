---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 995d7296ef1e5b6f846d5343fd072909a877b1ec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076849"
---
# <span data-ttu-id="91c48-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="91c48-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="91c48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91c48-102">SYNOPSIS</span></span>
<span data-ttu-id="91c48-103">Получение указанного делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="91c48-103">Get the specified offer delegation.</span></span>

## <span data-ttu-id="91c48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91c48-104">SYNTAX</span></span>

### <span data-ttu-id="91c48-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91c48-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91c48-106">Получить</span><span class="sxs-lookup"><span data-stu-id="91c48-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91c48-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="91c48-107">GetViaIdentity</span></span>
```
Get-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="91c48-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91c48-108">DESCRIPTION</span></span>
<span data-ttu-id="91c48-109">Получение указанного делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="91c48-109">Get the specified offer delegation.</span></span>

## <span data-ttu-id="91c48-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91c48-110">EXAMPLES</span></span>

### <span data-ttu-id="91c48-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="91c48-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferDelegation -OfferName "delegatedoffer" -ResourceGroupName "testrg"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/delegatedoffer/offerDelegations/offerdelegation
Location       : redmond
Name           : delegatedoffer/offerdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cbb018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="91c48-112">Получение списка делегированных разрешений.</span><span class="sxs-lookup"><span data-stu-id="91c48-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="91c48-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91c48-113">PARAMETERS</span></span>

### <span data-ttu-id="91c48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c48-114">-DefaultProfile</span></span>
<span data-ttu-id="91c48-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91c48-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c48-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91c48-116">-InputObject</span></span>
<span data-ttu-id="91c48-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="91c48-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="91c48-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91c48-118">-Name</span></span>
<span data-ttu-id="91c48-119">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="91c48-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="91c48-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="91c48-120">-OfferName</span></span>
<span data-ttu-id="91c48-121">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="91c48-121">Name of an offer.</span></span>

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

### <span data-ttu-id="91c48-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c48-122">-ResourceGroupName</span></span>
<span data-ttu-id="91c48-123">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="91c48-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="91c48-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91c48-124">-SubscriptionId</span></span>
<span data-ttu-id="91c48-125">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="91c48-125">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="91c48-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c48-126">CommonParameters</span></span>
<span data-ttu-id="91c48-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91c48-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c48-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91c48-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c48-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91c48-129">INPUTS</span></span>

### <span data-ttu-id="91c48-130">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="91c48-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="91c48-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91c48-131">OUTPUTS</span></span>

### <span data-ttu-id="91c48-132">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="91c48-132">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="91c48-133">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="91c48-133">ALIASES</span></span>

## <span data-ttu-id="91c48-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="91c48-134">NOTES</span></span>

<span data-ttu-id="91c48-135">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="91c48-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91c48-136">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="91c48-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="91c48-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="91c48-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91c48-138">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="91c48-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="91c48-139">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="91c48-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="91c48-140">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="91c48-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91c48-141">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="91c48-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="91c48-142">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="91c48-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="91c48-143">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="91c48-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="91c48-144">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="91c48-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="91c48-145">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="91c48-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="91c48-146">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="91c48-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="91c48-147">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="91c48-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="91c48-148">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="91c48-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="91c48-149">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="91c48-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="91c48-150">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="91c48-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="91c48-151">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="91c48-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="91c48-152">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="91c48-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="91c48-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91c48-153">RELATED LINKS</span></span>

