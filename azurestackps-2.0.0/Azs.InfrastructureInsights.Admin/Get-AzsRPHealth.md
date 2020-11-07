---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910509"
---
# <span data-ttu-id="eab96-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="eab96-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="eab96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eab96-102">SYNOPSIS</span></span>
<span data-ttu-id="eab96-103">Возвращает запрошенный объект работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="eab96-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="eab96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eab96-104">SYNTAX</span></span>

### <span data-ttu-id="eab96-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eab96-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eab96-106">Получить</span><span class="sxs-lookup"><span data-stu-id="eab96-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="eab96-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="eab96-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="eab96-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eab96-108">DESCRIPTION</span></span>
<span data-ttu-id="eab96-109">Возвращает запрошенный объект работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="eab96-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="eab96-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eab96-110">EXAMPLES</span></span>

### <span data-ttu-id="eab96-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="eab96-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="eab96-112">Возвращает список работоспособности каждой службы.</span><span class="sxs-lookup"><span data-stu-id="eab96-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="eab96-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="eab96-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="eab96-114">Возвращает состояние работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="eab96-114">Returns a service's health.</span></span>

## <span data-ttu-id="eab96-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eab96-115">PARAMETERS</span></span>

### <span data-ttu-id="eab96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab96-116">-DefaultProfile</span></span>
<span data-ttu-id="eab96-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eab96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eab96-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="eab96-118">-Filter</span></span>
<span data-ttu-id="eab96-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="eab96-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="eab96-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eab96-120">-InputObject</span></span>
<span data-ttu-id="eab96-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="eab96-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eab96-122">-Location</span><span class="sxs-lookup"><span data-stu-id="eab96-122">-Location</span></span>
<span data-ttu-id="eab96-123">Название региона</span><span class="sxs-lookup"><span data-stu-id="eab96-123">Name of the region</span></span>

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

### <span data-ttu-id="eab96-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eab96-124">-ResourceGroupName</span></span>
<span data-ttu-id="eab96-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eab96-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="eab96-126">-ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="eab96-126">-ServiceHealth</span></span>
<span data-ttu-id="eab96-127">Имя работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="eab96-127">Service Health name.</span></span>

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

### <span data-ttu-id="eab96-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eab96-128">-SubscriptionId</span></span>
<span data-ttu-id="eab96-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="eab96-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eab96-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="eab96-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eab96-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab96-131">CommonParameters</span></span>
<span data-ttu-id="eab96-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eab96-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab96-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eab96-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab96-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eab96-134">INPUTS</span></span>

### <span data-ttu-id="eab96-135">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="eab96-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="eab96-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eab96-136">OUTPUTS</span></span>

### <span data-ttu-id="eab96-137">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. Api20160501. IServiceHealth</span><span class="sxs-lookup"><span data-stu-id="eab96-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="eab96-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="eab96-138">NOTES</span></span>

<span data-ttu-id="eab96-139">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="eab96-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eab96-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eab96-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="eab96-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="eab96-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eab96-142">`[AlertName <String>]`: Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="eab96-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="eab96-143">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="eab96-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eab96-144">`[Location <String>]`: Имя области</span><span class="sxs-lookup"><span data-stu-id="eab96-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="eab96-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eab96-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="eab96-146">`[ResourceRegistrationId <String>]`: Идентификатор регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="eab96-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="eab96-147">`[ServiceHealth <String>]`: Имя работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="eab96-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="eab96-148">`[ServiceRegistrationId <String>]`: Регистрационный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="eab96-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="eab96-149">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="eab96-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eab96-150">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="eab96-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="eab96-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eab96-151">RELATED LINKS</span></span>

