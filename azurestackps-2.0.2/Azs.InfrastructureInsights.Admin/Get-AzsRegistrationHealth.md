---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076706"
---
# <span data-ttu-id="e650c-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="e650c-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="e650c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e650c-102">SYNOPSIS</span></span>
<span data-ttu-id="e650c-103">Возвращает запрошенные сведения о работоспособности ресурса.</span><span class="sxs-lookup"><span data-stu-id="e650c-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="e650c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e650c-104">SYNTAX</span></span>

### <span data-ttu-id="e650c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e650c-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e650c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="e650c-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e650c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e650c-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e650c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e650c-108">DESCRIPTION</span></span>
<span data-ttu-id="e650c-109">Возвращает запрошенные сведения о работоспособности ресурса.</span><span class="sxs-lookup"><span data-stu-id="e650c-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="e650c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e650c-110">EXAMPLES</span></span>

### <span data-ttu-id="e650c-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="e650c-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="e650c-112">Возвращает список работоспособности каждого ресурса в рамках службы.</span><span class="sxs-lookup"><span data-stu-id="e650c-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="e650c-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="e650c-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="e650c-114">Возвращает состояние работоспособности под заголовком "для Microsoft. Fabric. admin".</span><span class="sxs-lookup"><span data-stu-id="e650c-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="e650c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e650c-115">PARAMETERS</span></span>

### <span data-ttu-id="e650c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e650c-116">-DefaultProfile</span></span>
<span data-ttu-id="e650c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e650c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e650c-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="e650c-118">-Filter</span></span>
<span data-ttu-id="e650c-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="e650c-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e650c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e650c-120">-InputObject</span></span>
<span data-ttu-id="e650c-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e650c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e650c-122">-Location</span><span class="sxs-lookup"><span data-stu-id="e650c-122">-Location</span></span>
<span data-ttu-id="e650c-123">Название региона</span><span class="sxs-lookup"><span data-stu-id="e650c-123">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e650c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e650c-124">-ResourceGroupName</span></span>
<span data-ttu-id="e650c-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e650c-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="e650c-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="e650c-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="e650c-127">ИДЕНТИФИКАТОР регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="e650c-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="e650c-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="e650c-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="e650c-129">Регистрационный код службы.</span><span class="sxs-lookup"><span data-stu-id="e650c-129">Service registration ID.</span></span>

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

### <span data-ttu-id="e650c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e650c-130">-SubscriptionId</span></span>
<span data-ttu-id="e650c-131">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e650c-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e650c-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e650c-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e650c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e650c-133">CommonParameters</span></span>
<span data-ttu-id="e650c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e650c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e650c-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e650c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e650c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e650c-136">INPUTS</span></span>

### <span data-ttu-id="e650c-137">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e650c-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="e650c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e650c-138">OUTPUTS</span></span>

### <span data-ttu-id="e650c-139">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. Api20160501. IResourceHealth</span><span class="sxs-lookup"><span data-stu-id="e650c-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="e650c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e650c-140">NOTES</span></span>

<span data-ttu-id="e650c-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e650c-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e650c-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e650c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e650c-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e650c-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e650c-144">`[AlertName <String>]`: Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="e650c-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="e650c-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e650c-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e650c-146">`[Location <String>]`: Имя области</span><span class="sxs-lookup"><span data-stu-id="e650c-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="e650c-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e650c-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e650c-148">`[ResourceRegistrationId <String>]`: Идентификатор регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="e650c-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="e650c-149">`[ServiceHealth <String>]`: Имя работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="e650c-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="e650c-150">`[ServiceRegistrationId <String>]`: Регистрационный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="e650c-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="e650c-151">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e650c-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e650c-152">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e650c-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e650c-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e650c-153">RELATED LINKS</span></span>

