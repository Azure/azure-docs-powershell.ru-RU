---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovider
schema: 2.0.0
ms.openlocfilehash: 2c6c87ce0b40fae228756d4a9dd452b49ce1aad2
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94075135"
---
# <span data-ttu-id="23ea0-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="23ea0-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="23ea0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="23ea0-103">Получение указанного делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="23ea0-103">Get the specified delegated provider.</span></span>

## <span data-ttu-id="23ea0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23ea0-104">SYNTAX</span></span>

### <span data-ttu-id="23ea0-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23ea0-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23ea0-106">Получить</span><span class="sxs-lookup"><span data-stu-id="23ea0-106">Get</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23ea0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23ea0-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProvider -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="23ea0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ea0-108">DESCRIPTION</span></span>
<span data-ttu-id="23ea0-109">Получение указанного делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="23ea0-109">Get the specified delegated provider.</span></span>

## <span data-ttu-id="23ea0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23ea0-110">EXAMPLES</span></span>

### <span data-ttu-id="23ea0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23ea0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProvider -DelegatedProviderId "ed3e275b-87d1-4e94-9962-b3700287bdbc" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : cnur4866tenantresellersubscription843
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/cnur4866resellersubscrrg843/providers/Microsoft.Subscriptions.Admin/offers/cnur4866tenantsubsvcoffe
                                  r843
Owner                           : tenantadmin1@msazurestack.onmicrosoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="23ea0-112">Получение определенного делегируемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="23ea0-112">Get a specific delegated provider.</span></span>

## <span data-ttu-id="23ea0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23ea0-113">PARAMETERS</span></span>

### <span data-ttu-id="23ea0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ea0-114">-DefaultProfile</span></span>
<span data-ttu-id="23ea0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23ea0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ea0-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="23ea0-116">-DelegatedProviderId</span></span>
<span data-ttu-id="23ea0-117">Идентификатор DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="23ea0-117">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="23ea0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23ea0-118">-InputObject</span></span>
<span data-ttu-id="23ea0-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="23ea0-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="23ea0-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23ea0-120">-SubscriptionId</span></span>
<span data-ttu-id="23ea0-121">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="23ea0-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="23ea0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ea0-122">CommonParameters</span></span>
<span data-ttu-id="23ea0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23ea0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ea0-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23ea0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ea0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23ea0-125">INPUTS</span></span>

### <span data-ttu-id="23ea0-126">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="23ea0-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="23ea0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ea0-127">OUTPUTS</span></span>

### <span data-ttu-id="23ea0-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="23ea0-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="23ea0-129">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="23ea0-129">ALIASES</span></span>

## <span data-ttu-id="23ea0-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="23ea0-130">NOTES</span></span>

<span data-ttu-id="23ea0-131">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="23ea0-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23ea0-132">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23ea0-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="23ea0-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="23ea0-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23ea0-134">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="23ea0-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="23ea0-135">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="23ea0-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="23ea0-136">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="23ea0-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23ea0-137">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="23ea0-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="23ea0-138">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="23ea0-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="23ea0-139">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="23ea0-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="23ea0-140">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="23ea0-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="23ea0-141">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="23ea0-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="23ea0-142">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="23ea0-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="23ea0-143">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="23ea0-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="23ea0-144">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="23ea0-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="23ea0-145">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="23ea0-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="23ea0-146">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="23ea0-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="23ea0-147">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="23ea0-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="23ea0-148">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="23ea0-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="23ea0-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23ea0-149">RELATED LINKS</span></span>

