---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077153"
---
# <span data-ttu-id="88554-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="88554-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="88554-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88554-102">SYNOPSIS</span></span>
<span data-ttu-id="88554-103">Получите указанное предложение делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="88554-103">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="88554-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88554-104">SYNTAX</span></span>

### <span data-ttu-id="88554-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88554-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="88554-106">Получить</span><span class="sxs-lookup"><span data-stu-id="88554-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="88554-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="88554-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="88554-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88554-108">DESCRIPTION</span></span>
<span data-ttu-id="88554-109">Получите указанное предложение делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="88554-109">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="88554-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88554-110">EXAMPLES</span></span>

### <span data-ttu-id="88554-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88554-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

<span data-ttu-id="88554-112">Получение списка предлагаемых провайдеров делегирования.</span><span class="sxs-lookup"><span data-stu-id="88554-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="88554-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88554-113">PARAMETERS</span></span>

### <span data-ttu-id="88554-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88554-114">-DefaultProfile</span></span>
<span data-ttu-id="88554-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88554-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88554-116">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88554-116">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="88554-117">Идентификатор подписки на делегированный поставщик.</span><span class="sxs-lookup"><span data-stu-id="88554-117">Delegated provider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="88554-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88554-118">-InputObject</span></span>
<span data-ttu-id="88554-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="88554-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88554-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88554-120">-Name</span></span>
<span data-ttu-id="88554-121">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="88554-121">Name of an offer.</span></span>

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

### <span data-ttu-id="88554-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88554-122">-SubscriptionId</span></span>
<span data-ttu-id="88554-123">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="88554-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="88554-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88554-124">CommonParameters</span></span>
<span data-ttu-id="88554-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88554-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88554-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88554-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88554-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88554-127">INPUTS</span></span>

### <span data-ttu-id="88554-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="88554-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="88554-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88554-129">OUTPUTS</span></span>

### <span data-ttu-id="88554-130">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="88554-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDelegatedProviderOffer</span></span>

<span data-ttu-id="88554-131">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="88554-131">ALIASES</span></span>

## <span data-ttu-id="88554-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="88554-132">NOTES</span></span>

<span data-ttu-id="88554-133">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88554-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88554-134">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88554-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="88554-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="88554-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88554-136">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="88554-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="88554-137">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="88554-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="88554-138">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="88554-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88554-139">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="88554-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="88554-140">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="88554-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="88554-141">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="88554-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="88554-142">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="88554-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="88554-143">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="88554-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="88554-144">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="88554-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="88554-145">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="88554-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="88554-146">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="88554-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="88554-147">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="88554-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="88554-148">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="88554-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="88554-149">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="88554-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="88554-150">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="88554-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="88554-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88554-151">RELATED LINKS</span></span>
