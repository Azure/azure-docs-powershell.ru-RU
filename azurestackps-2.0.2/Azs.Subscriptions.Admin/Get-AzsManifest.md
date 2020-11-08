---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsmanifest
schema: 2.0.0
ms.openlocfilehash: 4e5ccedc67af31c19d35e5a91fad62ba46535ed7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076998"
---
# <span data-ttu-id="224ae-101">Get-AzsManifest</span><span class="sxs-lookup"><span data-stu-id="224ae-101">Get-AzsManifest</span></span>

## <span data-ttu-id="224ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="224ae-102">SYNOPSIS</span></span>
<span data-ttu-id="224ae-103">Получение указанного манифеста.</span><span class="sxs-lookup"><span data-stu-id="224ae-103">Get the specified manifest.</span></span>

## <span data-ttu-id="224ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="224ae-104">SYNTAX</span></span>

### <span data-ttu-id="224ae-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="224ae-105">List (Default)</span></span>
```
Get-AzsManifest [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="224ae-106">Получить</span><span class="sxs-lookup"><span data-stu-id="224ae-106">Get</span></span>
```
Get-AzsManifest -ManifestName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="224ae-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="224ae-107">GetViaIdentity</span></span>
```
Get-AzsManifest -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="224ae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="224ae-108">DESCRIPTION</span></span>
<span data-ttu-id="224ae-109">Получение указанного манифеста.</span><span class="sxs-lookup"><span data-stu-id="224ae-109">Get the specified manifest.</span></span>

## <span data-ttu-id="224ae-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="224ae-110">EXAMPLES</span></span>

### <span data-ttu-id="224ae-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="224ae-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsManifest

Name     : Microsoft-Authorization-Admin--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata

Name     : Microsoft-Authorization--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata
```

<span data-ttu-id="224ae-112">Список всех манифестов в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="224ae-112">Lists all the manifests under the current subscription.</span></span>

## <span data-ttu-id="224ae-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="224ae-113">PARAMETERS</span></span>

### <span data-ttu-id="224ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="224ae-114">-DefaultProfile</span></span>
<span data-ttu-id="224ae-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="224ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="224ae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="224ae-116">-InputObject</span></span>
<span data-ttu-id="224ae-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="224ae-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="224ae-118">-ManifestName</span><span class="sxs-lookup"><span data-stu-id="224ae-118">-ManifestName</span></span>
<span data-ttu-id="224ae-119">Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="224ae-119">The manifest name.</span></span>

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

### <span data-ttu-id="224ae-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="224ae-120">-SubscriptionId</span></span>
<span data-ttu-id="224ae-121">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="224ae-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="224ae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224ae-122">CommonParameters</span></span>
<span data-ttu-id="224ae-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="224ae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224ae-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="224ae-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224ae-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="224ae-125">INPUTS</span></span>

### <span data-ttu-id="224ae-126">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="224ae-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="224ae-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="224ae-127">OUTPUTS</span></span>

### <span data-ttu-id="224ae-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IManifest</span><span class="sxs-lookup"><span data-stu-id="224ae-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IManifest</span></span>

<span data-ttu-id="224ae-129">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="224ae-129">ALIASES</span></span>

## <span data-ttu-id="224ae-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="224ae-130">NOTES</span></span>

<span data-ttu-id="224ae-131">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="224ae-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="224ae-132">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="224ae-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="224ae-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="224ae-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="224ae-134">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="224ae-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="224ae-135">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="224ae-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="224ae-136">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="224ae-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="224ae-137">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="224ae-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="224ae-138">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="224ae-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="224ae-139">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="224ae-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="224ae-140">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="224ae-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="224ae-141">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="224ae-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="224ae-142">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="224ae-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="224ae-143">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="224ae-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="224ae-144">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="224ae-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="224ae-145">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="224ae-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="224ae-146">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="224ae-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="224ae-147">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="224ae-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="224ae-148">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="224ae-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="224ae-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="224ae-149">RELATED LINKS</span></span>

