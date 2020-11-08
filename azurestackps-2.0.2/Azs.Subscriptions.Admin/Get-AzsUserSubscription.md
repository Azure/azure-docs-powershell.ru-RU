---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077067"
---
# <span data-ttu-id="1b36c-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="1b36c-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="1b36c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b36c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b36c-103">Получить указанную подписку.</span><span class="sxs-lookup"><span data-stu-id="1b36c-103">Get a specified subscription.</span></span>

## <span data-ttu-id="1b36c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b36c-104">SYNTAX</span></span>

### <span data-ttu-id="1b36c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b36c-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b36c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="1b36c-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1b36c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1b36c-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b36c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b36c-108">DESCRIPTION</span></span>
<span data-ttu-id="1b36c-109">Получить указанную подписку.</span><span class="sxs-lookup"><span data-stu-id="1b36c-109">Get a specified subscription.</span></span>

## <span data-ttu-id="1b36c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b36c-110">EXAMPLES</span></span>

### <span data-ttu-id="1b36c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b36c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="1b36c-112">Получение списка подписок на пользователя в качестве оператора.</span><span class="sxs-lookup"><span data-stu-id="1b36c-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="1b36c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b36c-113">PARAMETERS</span></span>

### <span data-ttu-id="1b36c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b36c-114">-DefaultProfile</span></span>
<span data-ttu-id="1b36c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b36c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b36c-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="1b36c-116">-Filter</span></span>
<span data-ttu-id="1b36c-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="1b36c-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1b36c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b36c-118">-InputObject</span></span>
<span data-ttu-id="1b36c-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="1b36c-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1b36c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b36c-120">-SubscriptionId</span></span>
<span data-ttu-id="1b36c-121">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1b36c-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1b36c-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b36c-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="1b36c-123">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1b36c-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="1b36c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b36c-124">CommonParameters</span></span>
<span data-ttu-id="1b36c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b36c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b36c-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b36c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b36c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b36c-127">INPUTS</span></span>

### <span data-ttu-id="1b36c-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1b36c-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="1b36c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b36c-129">OUTPUTS</span></span>

### <span data-ttu-id="1b36c-130">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="1b36c-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="1b36c-131">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="1b36c-131">ALIASES</span></span>

## <span data-ttu-id="1b36c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b36c-132">NOTES</span></span>

<span data-ttu-id="1b36c-133">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1b36c-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1b36c-134">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1b36c-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1b36c-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="1b36c-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1b36c-136">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1b36c-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="1b36c-137">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="1b36c-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="1b36c-138">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="1b36c-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1b36c-139">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="1b36c-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="1b36c-140">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="1b36c-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="1b36c-141">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="1b36c-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="1b36c-142">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="1b36c-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="1b36c-143">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="1b36c-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="1b36c-144">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="1b36c-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="1b36c-145">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="1b36c-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="1b36c-146">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="1b36c-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="1b36c-147">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="1b36c-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="1b36c-148">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="1b36c-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1b36c-149">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="1b36c-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="1b36c-150">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="1b36c-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="1b36c-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b36c-151">RELATED LINKS</span></span>

