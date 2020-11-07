---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910506"
---
# <span data-ttu-id="7009f-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="7009f-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="7009f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7009f-102">SYNOPSIS</span></span>
<span data-ttu-id="7009f-103">Возвращает запрошенные сведения о работоспособности ресурса.</span><span class="sxs-lookup"><span data-stu-id="7009f-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="7009f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7009f-104">SYNTAX</span></span>

### <span data-ttu-id="7009f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7009f-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7009f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="7009f-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7009f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7009f-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7009f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7009f-108">DESCRIPTION</span></span>
<span data-ttu-id="7009f-109">Возвращает запрошенные сведения о работоспособности ресурса.</span><span class="sxs-lookup"><span data-stu-id="7009f-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="7009f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7009f-110">EXAMPLES</span></span>

### <span data-ttu-id="7009f-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="7009f-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="7009f-112">Возвращает список работоспособности каждого ресурса в рамках службы.</span><span class="sxs-lookup"><span data-stu-id="7009f-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="7009f-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="7009f-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="7009f-114">Возвращает состояние работоспособности под заголовком "для Microsoft. Fabric. admin".</span><span class="sxs-lookup"><span data-stu-id="7009f-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="7009f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7009f-115">PARAMETERS</span></span>

### <span data-ttu-id="7009f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7009f-116">-DefaultProfile</span></span>
<span data-ttu-id="7009f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7009f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7009f-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="7009f-118">-Filter</span></span>
<span data-ttu-id="7009f-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="7009f-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="7009f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7009f-120">-InputObject</span></span>
<span data-ttu-id="7009f-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="7009f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7009f-122">-Location</span><span class="sxs-lookup"><span data-stu-id="7009f-122">-Location</span></span>
<span data-ttu-id="7009f-123">Название региона</span><span class="sxs-lookup"><span data-stu-id="7009f-123">Name of the region</span></span>

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

### <span data-ttu-id="7009f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7009f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7009f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7009f-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="7009f-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="7009f-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="7009f-127">ИДЕНТИФИКАТОР регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="7009f-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="7009f-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="7009f-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="7009f-129">Регистрационный код службы.</span><span class="sxs-lookup"><span data-stu-id="7009f-129">Service registration ID.</span></span>

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

### <span data-ttu-id="7009f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7009f-130">-SubscriptionId</span></span>
<span data-ttu-id="7009f-131">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7009f-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7009f-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="7009f-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7009f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7009f-133">CommonParameters</span></span>
<span data-ttu-id="7009f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7009f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7009f-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7009f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7009f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7009f-136">INPUTS</span></span>

### <span data-ttu-id="7009f-137">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7009f-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="7009f-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7009f-138">OUTPUTS</span></span>

### <span data-ttu-id="7009f-139">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. Api20160501. IResourceHealth</span><span class="sxs-lookup"><span data-stu-id="7009f-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="7009f-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="7009f-140">NOTES</span></span>

<span data-ttu-id="7009f-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7009f-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7009f-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7009f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7009f-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="7009f-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7009f-144">`[AlertName <String>]`: Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="7009f-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="7009f-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="7009f-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7009f-146">`[Location <String>]`: Имя области</span><span class="sxs-lookup"><span data-stu-id="7009f-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="7009f-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7009f-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7009f-148">`[ResourceRegistrationId <String>]`: Идентификатор регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="7009f-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="7009f-149">`[ServiceHealth <String>]`: Имя работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="7009f-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="7009f-150">`[ServiceRegistrationId <String>]`: Регистрационный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="7009f-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="7009f-151">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7009f-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7009f-152">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="7009f-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="7009f-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7009f-153">RELATED LINKS</span></span>

