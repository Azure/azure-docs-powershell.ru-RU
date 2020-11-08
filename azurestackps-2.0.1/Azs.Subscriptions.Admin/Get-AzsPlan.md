---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsplan
schema: 2.0.0
ms.openlocfilehash: 4aa59d41bc13d79e487465a6a0721ec19ed68bb8
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075202"
---
# <span data-ttu-id="23ff2-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="23ff2-101">Get-AzsPlan</span></span>

## <span data-ttu-id="23ff2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="23ff2-103">Получить указанный план.</span><span class="sxs-lookup"><span data-stu-id="23ff2-103">Get the specified plan.</span></span>

## <span data-ttu-id="23ff2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23ff2-104">SYNTAX</span></span>

### <span data-ttu-id="23ff2-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23ff2-105">List (Default)</span></span>
```
Get-AzsPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23ff2-106">Получить</span><span class="sxs-lookup"><span data-stu-id="23ff2-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23ff2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23ff2-107">GetViaIdentity</span></span>
```
Get-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23ff2-108">List1</span><span class="sxs-lookup"><span data-stu-id="23ff2-108">List1</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="23ff2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ff2-109">DESCRIPTION</span></span>
<span data-ttu-id="23ff2-110">Получить указанный план.</span><span class="sxs-lookup"><span data-stu-id="23ff2-110">Get the specified plan.</span></span>

## <span data-ttu-id="23ff2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23ff2-111">EXAMPLES</span></span>

### <span data-ttu-id="23ff2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23ff2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 1
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="23ff2-113">Получить план вложения в рамках этой подписки.</span><span class="sxs-lookup"><span data-stu-id="23ff2-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="23ff2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23ff2-114">PARAMETERS</span></span>

### <span data-ttu-id="23ff2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ff2-115">-DefaultProfile</span></span>
<span data-ttu-id="23ff2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23ff2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ff2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23ff2-117">-InputObject</span></span>
<span data-ttu-id="23ff2-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="23ff2-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="23ff2-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23ff2-119">-Name</span></span>
<span data-ttu-id="23ff2-120">Название плана.</span><span class="sxs-lookup"><span data-stu-id="23ff2-120">Name of the plan.</span></span>

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

### <span data-ttu-id="23ff2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ff2-121">-ResourceGroupName</span></span>
<span data-ttu-id="23ff2-122">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="23ff2-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="23ff2-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23ff2-123">-SubscriptionId</span></span>
<span data-ttu-id="23ff2-124">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="23ff2-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="23ff2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ff2-125">CommonParameters</span></span>
<span data-ttu-id="23ff2-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23ff2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ff2-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23ff2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ff2-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23ff2-128">INPUTS</span></span>

### <span data-ttu-id="23ff2-129">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="23ff2-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="23ff2-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ff2-130">OUTPUTS</span></span>

### <span data-ttu-id="23ff2-131">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="23ff2-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="23ff2-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="23ff2-132">ALIASES</span></span>

## <span data-ttu-id="23ff2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="23ff2-133">NOTES</span></span>

<span data-ttu-id="23ff2-134">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="23ff2-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23ff2-135">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23ff2-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="23ff2-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="23ff2-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23ff2-137">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="23ff2-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="23ff2-138">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="23ff2-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="23ff2-139">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="23ff2-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23ff2-140">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="23ff2-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="23ff2-141">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="23ff2-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="23ff2-142">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="23ff2-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="23ff2-143">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="23ff2-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="23ff2-144">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="23ff2-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="23ff2-145">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="23ff2-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="23ff2-146">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="23ff2-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="23ff2-147">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="23ff2-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="23ff2-148">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="23ff2-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="23ff2-149">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="23ff2-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="23ff2-150">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="23ff2-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="23ff2-151">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="23ff2-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="23ff2-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23ff2-152">RELATED LINKS</span></span>

