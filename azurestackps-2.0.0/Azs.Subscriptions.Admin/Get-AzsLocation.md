---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94075131"
---
# <span data-ttu-id="c9a52-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="c9a52-101">Get-AzsLocation</span></span>

## <span data-ttu-id="c9a52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9a52-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a52-103">Получить указанное расположение.</span><span class="sxs-lookup"><span data-stu-id="c9a52-103">Get the specified location.</span></span>

## <span data-ttu-id="c9a52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9a52-104">SYNTAX</span></span>

### <span data-ttu-id="c9a52-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9a52-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9a52-106">Получить</span><span class="sxs-lookup"><span data-stu-id="c9a52-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9a52-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c9a52-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9a52-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9a52-108">DESCRIPTION</span></span>
<span data-ttu-id="c9a52-109">Получить указанное расположение.</span><span class="sxs-lookup"><span data-stu-id="c9a52-109">Get the specified location.</span></span>

## <span data-ttu-id="c9a52-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9a52-110">EXAMPLES</span></span>

### <span data-ttu-id="c9a52-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9a52-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="c9a52-112">Получение списка всех AzureStackных местоположений.</span><span class="sxs-lookup"><span data-stu-id="c9a52-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="c9a52-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9a52-113">PARAMETERS</span></span>

### <span data-ttu-id="c9a52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a52-114">-DefaultProfile</span></span>
<span data-ttu-id="c9a52-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9a52-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a52-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9a52-116">-InputObject</span></span>
<span data-ttu-id="c9a52-117">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c9a52-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9a52-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c9a52-118">-Name</span></span>
<span data-ttu-id="c9a52-119">Расположение AzureStack.</span><span class="sxs-lookup"><span data-stu-id="c9a52-119">The AzureStack location.</span></span>

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

### <span data-ttu-id="c9a52-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9a52-120">-SubscriptionId</span></span>
<span data-ttu-id="c9a52-121">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c9a52-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c9a52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a52-122">CommonParameters</span></span>
<span data-ttu-id="c9a52-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9a52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a52-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9a52-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a52-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9a52-125">INPUTS</span></span>

### <span data-ttu-id="c9a52-126">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c9a52-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="c9a52-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9a52-127">OUTPUTS</span></span>

### <span data-ttu-id="c9a52-128">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. ILocation</span><span class="sxs-lookup"><span data-stu-id="c9a52-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="c9a52-129">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c9a52-129">ALIASES</span></span>

## <span data-ttu-id="c9a52-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9a52-130">NOTES</span></span>

<span data-ttu-id="c9a52-131">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c9a52-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9a52-132">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9a52-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c9a52-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="c9a52-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9a52-134">`[DelegatedProvider <String>]`: DelegatedProvider идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c9a52-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="c9a52-135">`[DelegatedProviderSubscriptionId <String>]`: Идентификатор подписки для делегированного поставщика.</span><span class="sxs-lookup"><span data-stu-id="c9a52-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="c9a52-136">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="c9a52-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9a52-137">`[Location <String>]`: Расположение в AzureStack.</span><span class="sxs-lookup"><span data-stu-id="c9a52-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="c9a52-138">`[ManifestName <String>]`: Имя манифеста.</span><span class="sxs-lookup"><span data-stu-id="c9a52-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="c9a52-139">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="c9a52-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="c9a52-140">`[OfferDelegationName <String>]`: Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="c9a52-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="c9a52-141">`[OperationsStatusName <String>]`: Имя состояния операции.</span><span class="sxs-lookup"><span data-stu-id="c9a52-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="c9a52-142">`[Plan <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="c9a52-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="c9a52-143">`[PlanAcquisitionId <String>]`: Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="c9a52-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="c9a52-144">`[Quota <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="c9a52-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c9a52-145">`[ResourceGroupName <String>]`: Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="c9a52-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="c9a52-146">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c9a52-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c9a52-147">`[TargetSubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c9a52-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="c9a52-148">`[Tenant <String>]`: Имя клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="c9a52-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="c9a52-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9a52-149">RELATED LINKS</span></span>

