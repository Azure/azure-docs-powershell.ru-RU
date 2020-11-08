---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94075132"
---
# <span data-ttu-id="164a1-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="164a1-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="164a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="164a1-102">SYNOPSIS</span></span>
<span data-ttu-id="164a1-103">Получение клиента службы каталогов по имени.</span><span class="sxs-lookup"><span data-stu-id="164a1-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="164a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="164a1-104">SYNTAX</span></span>

### <span data-ttu-id="164a1-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="164a1-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="164a1-106">Получить</span><span class="sxs-lookup"><span data-stu-id="164a1-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="164a1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="164a1-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="164a1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="164a1-108">DESCRIPTION</span></span>
<span data-ttu-id="164a1-109">Получение клиента службы каталогов по имени.</span><span class="sxs-lookup"><span data-stu-id="164a1-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="164a1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="164a1-110">EXAMPLES</span></span>

### <span data-ttu-id="164a1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="164a1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="164a1-112">Список всех клиентов каталогов в текущей подписке и указанным именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="164a1-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="164a1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="164a1-113">PARAMETERS</span></span>

### <span data-ttu-id="164a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="164a1-114">-DefaultProfile</span></span>
<span data-ttu-id="164a1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="164a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="164a1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="164a1-116">-InputObject</span></span>
<span data-ttu-id="164a1-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="164a1-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="164a1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="164a1-118">-Name</span></span>
<span data-ttu-id="164a1-119">Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="164a1-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="164a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="164a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="164a1-121">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="164a1-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="164a1-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="164a1-122">-SubscriptionId</span></span>
<span data-ttu-id="164a1-123">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="164a1-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="164a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="164a1-124">CommonParameters</span></span>
<span data-ttu-id="164a1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="164a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="164a1-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="164a1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="164a1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="164a1-127">INPUTS</span></span>

### <span data-ttu-id="164a1-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="164a1-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="164a1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="164a1-129">OUTPUTS</span></span>

### <span data-ttu-id="164a1-130">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="164a1-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="164a1-131">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="164a1-131">ALIASES</span></span>

## <span data-ttu-id="164a1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="164a1-132">NOTES</span></span>

<span data-ttu-id="164a1-133">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="164a1-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="164a1-134">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="164a1-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="164a1-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="164a1-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="164a1-136">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="164a1-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="164a1-137">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="164a1-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="164a1-138">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="164a1-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="164a1-139">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="164a1-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="164a1-140">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="164a1-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="164a1-141">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="164a1-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="164a1-142">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="164a1-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="164a1-143">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="164a1-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="164a1-144">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="164a1-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="164a1-145">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="164a1-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="164a1-146">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="164a1-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="164a1-147">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="164a1-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="164a1-148">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="164a1-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="164a1-149">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="164a1-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="164a1-150">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="164a1-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="164a1-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="164a1-151">RELATED LINKS</span></span>

