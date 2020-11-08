---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076733"
---
# <span data-ttu-id="a3bd7-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="a3bd7-101">Get-AzsLocation</span></span>

## <span data-ttu-id="a3bd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="a3bd7-103">Получить указанное расположение.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-103">Get the specified location.</span></span>

## <span data-ttu-id="a3bd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3bd7-104">SYNTAX</span></span>

### <span data-ttu-id="a3bd7-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3bd7-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3bd7-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a3bd7-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3bd7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a3bd7-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a3bd7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3bd7-108">DESCRIPTION</span></span>
<span data-ttu-id="a3bd7-109">Получить указанное расположение.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-109">Get the specified location.</span></span>

## <span data-ttu-id="a3bd7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3bd7-110">EXAMPLES</span></span>

### <span data-ttu-id="a3bd7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3bd7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="a3bd7-112">Получение списка всех AzureStackных местоположений.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="a3bd7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3bd7-113">PARAMETERS</span></span>

### <span data-ttu-id="a3bd7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3bd7-114">-DefaultProfile</span></span>
<span data-ttu-id="a3bd7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3bd7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3bd7-116">-InputObject</span></span>
<span data-ttu-id="a3bd7-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3bd7-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3bd7-118">-Name</span></span>
<span data-ttu-id="a3bd7-119">Расположение AzureStack.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a3bd7-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3bd7-120">-SubscriptionId</span></span>
<span data-ttu-id="a3bd7-121">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a3bd7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3bd7-122">CommonParameters</span></span>
<span data-ttu-id="a3bd7-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3bd7-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3bd7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3bd7-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3bd7-125">INPUTS</span></span>

### <span data-ttu-id="a3bd7-126">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a3bd7-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="a3bd7-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3bd7-127">OUTPUTS</span></span>

### <span data-ttu-id="a3bd7-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ILocation</span><span class="sxs-lookup"><span data-stu-id="a3bd7-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="a3bd7-129">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a3bd7-129">ALIASES</span></span>

## <span data-ttu-id="a3bd7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3bd7-130">NOTES</span></span>

<span data-ttu-id="a3bd7-131">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3bd7-132">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a3bd7-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="a3bd7-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3bd7-134">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="a3bd7-135">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="a3bd7-136">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="a3bd7-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3bd7-137">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="a3bd7-138">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="a3bd7-139">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="a3bd7-140">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="a3bd7-141">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="a3bd7-142">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="a3bd7-143">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="a3bd7-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="a3bd7-144">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="a3bd7-145">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="a3bd7-146">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a3bd7-147">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="a3bd7-148">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="a3bd7-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="a3bd7-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3bd7-149">RELATED LINKS</span></span>

