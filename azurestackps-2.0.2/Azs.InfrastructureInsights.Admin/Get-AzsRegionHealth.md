---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076709"
---
# <span data-ttu-id="00015-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="00015-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="00015-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00015-102">SYNOPSIS</span></span>
<span data-ttu-id="00015-103">Возвращает запрошенное состояние работоспособности для региона.</span><span class="sxs-lookup"><span data-stu-id="00015-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="00015-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00015-104">SYNTAX</span></span>

### <span data-ttu-id="00015-105">Get (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00015-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="00015-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="00015-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="00015-107">Список</span><span class="sxs-lookup"><span data-stu-id="00015-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="00015-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00015-108">DESCRIPTION</span></span>
<span data-ttu-id="00015-109">Возвращает запрошенное состояние работоспособности для региона.</span><span class="sxs-lookup"><span data-stu-id="00015-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="00015-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00015-110">EXAMPLES</span></span>

### <span data-ttu-id="00015-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="00015-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="00015-112">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="00015-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="00015-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00015-113">PARAMETERS</span></span>

### <span data-ttu-id="00015-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00015-114">-DefaultProfile</span></span>
<span data-ttu-id="00015-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00015-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00015-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="00015-116">-Filter</span></span>
<span data-ttu-id="00015-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="00015-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="00015-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00015-118">-InputObject</span></span>
<span data-ttu-id="00015-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="00015-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="00015-120">-Location</span><span class="sxs-lookup"><span data-stu-id="00015-120">-Location</span></span>
<span data-ttu-id="00015-121">Название региона</span><span class="sxs-lookup"><span data-stu-id="00015-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="00015-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00015-122">-ResourceGroupName</span></span>
<span data-ttu-id="00015-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="00015-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="00015-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00015-124">-SubscriptionId</span></span>
<span data-ttu-id="00015-125">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="00015-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="00015-126">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="00015-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="00015-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00015-127">CommonParameters</span></span>
<span data-ttu-id="00015-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00015-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00015-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00015-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00015-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00015-130">INPUTS</span></span>

### <span data-ttu-id="00015-131">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="00015-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="00015-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00015-132">OUTPUTS</span></span>

### <span data-ttu-id="00015-133">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. Api20160501. IRegionHealth</span><span class="sxs-lookup"><span data-stu-id="00015-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="00015-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="00015-134">NOTES</span></span>

<span data-ttu-id="00015-135">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="00015-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="00015-136">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="00015-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="00015-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="00015-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="00015-138">`[AlertName <String>]`: Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="00015-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="00015-139">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="00015-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="00015-140">`[Location <String>]`: Имя области</span><span class="sxs-lookup"><span data-stu-id="00015-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="00015-141">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="00015-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="00015-142">`[ResourceRegistrationId <String>]`: Идентификатор регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="00015-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="00015-143">`[ServiceHealth <String>]`: Имя работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="00015-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="00015-144">`[ServiceRegistrationId <String>]`: Регистрационный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="00015-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="00015-145">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="00015-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="00015-146">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="00015-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="00015-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00015-147">RELATED LINKS</span></span>

