---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076708"
---
# <span data-ttu-id="08764-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="08764-101">Get-AzsAlert</span></span>

## <span data-ttu-id="08764-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08764-102">SYNOPSIS</span></span>
<span data-ttu-id="08764-103">Возвращает запрошенное оповещение.</span><span class="sxs-lookup"><span data-stu-id="08764-103">Returns the requested alert.</span></span>

## <span data-ttu-id="08764-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08764-104">SYNTAX</span></span>

### <span data-ttu-id="08764-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08764-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="08764-106">Получить</span><span class="sxs-lookup"><span data-stu-id="08764-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="08764-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="08764-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="08764-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08764-108">DESCRIPTION</span></span>
<span data-ttu-id="08764-109">Возвращает запрошенное оповещение.</span><span class="sxs-lookup"><span data-stu-id="08764-109">Returns the requested alert.</span></span>

## <span data-ttu-id="08764-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08764-110">EXAMPLES</span></span>

### <span data-ttu-id="08764-111">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="08764-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="08764-112">Получить оповещение по имени.</span><span class="sxs-lookup"><span data-stu-id="08764-112">Get an alert by Name.</span></span>

### <span data-ttu-id="08764-113">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="08764-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="08764-114">Получение всех активных оповещений и отображение их ошибок и названий.</span><span class="sxs-lookup"><span data-stu-id="08764-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="08764-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08764-115">PARAMETERS</span></span>

### <span data-ttu-id="08764-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08764-116">-DefaultProfile</span></span>
<span data-ttu-id="08764-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08764-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08764-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="08764-118">-Filter</span></span>
<span data-ttu-id="08764-119">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="08764-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="08764-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08764-120">-InputObject</span></span>
<span data-ttu-id="08764-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="08764-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="08764-122">-Location</span><span class="sxs-lookup"><span data-stu-id="08764-122">-Location</span></span>
<span data-ttu-id="08764-123">Название региона</span><span class="sxs-lookup"><span data-stu-id="08764-123">Name of the region</span></span>

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

### <span data-ttu-id="08764-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="08764-124">-Name</span></span>
<span data-ttu-id="08764-125">Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="08764-125">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08764-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08764-126">-ResourceGroupName</span></span>
<span data-ttu-id="08764-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08764-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="08764-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08764-128">-SubscriptionId</span></span>
<span data-ttu-id="08764-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08764-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="08764-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="08764-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="08764-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08764-131">CommonParameters</span></span>
<span data-ttu-id="08764-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08764-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08764-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08764-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08764-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08764-134">INPUTS</span></span>

### <span data-ttu-id="08764-135">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="08764-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="08764-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08764-136">OUTPUTS</span></span>

### <span data-ttu-id="08764-137">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="08764-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="08764-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="08764-138">NOTES</span></span>

<span data-ttu-id="08764-139">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="08764-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08764-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="08764-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="08764-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="08764-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="08764-142">`[AlertName <String>]`: Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="08764-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="08764-143">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="08764-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="08764-144">`[Location <String>]`: Имя области</span><span class="sxs-lookup"><span data-stu-id="08764-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="08764-145">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08764-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="08764-146">`[ResourceRegistrationId <String>]`: Идентификатор регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="08764-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="08764-147">`[ServiceHealth <String>]`: Имя работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="08764-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="08764-148">`[ServiceRegistrationId <String>]`: Регистрационный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="08764-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="08764-149">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08764-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="08764-150">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="08764-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="08764-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08764-151">RELATED LINKS</span></span>

