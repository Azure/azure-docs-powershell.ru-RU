---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075159"
---
# <span data-ttu-id="e1f41-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="e1f41-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="e1f41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1f41-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f41-103">Получить указанное предложение.</span><span class="sxs-lookup"><span data-stu-id="e1f41-103">Get the specified offer.</span></span>

## <span data-ttu-id="e1f41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1f41-104">SYNTAX</span></span>

### <span data-ttu-id="e1f41-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1f41-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1f41-106">Получить</span><span class="sxs-lookup"><span data-stu-id="e1f41-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e1f41-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e1f41-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f41-108">List1</span><span class="sxs-lookup"><span data-stu-id="e1f41-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1f41-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1f41-109">DESCRIPTION</span></span>
<span data-ttu-id="e1f41-110">Получить указанное предложение.</span><span class="sxs-lookup"><span data-stu-id="e1f41-110">Get the specified offer.</span></span>

## <span data-ttu-id="e1f41-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1f41-111">EXAMPLES</span></span>

### <span data-ttu-id="e1f41-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1f41-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
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

<span data-ttu-id="e1f41-113">Получение предложения по имени и ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f41-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="e1f41-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1f41-114">PARAMETERS</span></span>

### <span data-ttu-id="e1f41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f41-115">-DefaultProfile</span></span>
<span data-ttu-id="e1f41-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f41-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1f41-117">-InputObject</span></span>
<span data-ttu-id="e1f41-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e1f41-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e1f41-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1f41-119">-Name</span></span>
<span data-ttu-id="e1f41-120">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="e1f41-120">Name of an offer.</span></span>

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

### <span data-ttu-id="e1f41-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f41-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1f41-122">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="e1f41-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e1f41-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1f41-123">-SubscriptionId</span></span>
<span data-ttu-id="e1f41-124">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e1f41-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e1f41-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f41-125">CommonParameters</span></span>
<span data-ttu-id="e1f41-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1f41-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f41-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1f41-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f41-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1f41-128">INPUTS</span></span>

### <span data-ttu-id="e1f41-129">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e1f41-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e1f41-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1f41-130">OUTPUTS</span></span>

### <span data-ttu-id="e1f41-131">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="e1f41-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="e1f41-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="e1f41-132">ALIASES</span></span>

<span data-ttu-id="e1f41-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="e1f41-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="e1f41-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1f41-134">NOTES</span></span>

<span data-ttu-id="e1f41-135">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e1f41-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1f41-136">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e1f41-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e1f41-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e1f41-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e1f41-138">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e1f41-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e1f41-139">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="e1f41-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e1f41-140">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e1f41-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e1f41-141">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="e1f41-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e1f41-142">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="e1f41-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e1f41-143">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="e1f41-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e1f41-144">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="e1f41-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e1f41-145">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="e1f41-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e1f41-146">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="e1f41-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e1f41-147">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="e1f41-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e1f41-148">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="e1f41-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e1f41-149">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="e1f41-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e1f41-150">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e1f41-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e1f41-151">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e1f41-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e1f41-152">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1f41-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="e1f41-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1f41-153">RELATED LINKS</span></span>

