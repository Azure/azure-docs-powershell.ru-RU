---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076975"
---
# <span data-ttu-id="e709c-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="e709c-101">Close-AzsAlert</span></span>

## <span data-ttu-id="e709c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e709c-102">SYNOPSIS</span></span>
<span data-ttu-id="e709c-103">Закрывает заданное оповещение.</span><span class="sxs-lookup"><span data-stu-id="e709c-103">Closes the given alert.</span></span>

## <span data-ttu-id="e709c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e709c-104">SYNTAX</span></span>

### <span data-ttu-id="e709c-105">CloseExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e709c-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e709c-106">Неожиданно</span><span class="sxs-lookup"><span data-stu-id="e709c-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e709c-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e709c-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e709c-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e709c-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e709c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e709c-109">DESCRIPTION</span></span>
<span data-ttu-id="e709c-110">Закрывает заданное оповещение.</span><span class="sxs-lookup"><span data-stu-id="e709c-110">Closes the given alert.</span></span>

## <span data-ttu-id="e709c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e709c-111">EXAMPLES</span></span>

### <span data-ttu-id="e709c-112">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="e709c-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="e709c-113">Закрыть оповещение по имени.</span><span class="sxs-lookup"><span data-stu-id="e709c-113">Close an alert by Name.</span></span>

### <span data-ttu-id="e709c-114">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="e709c-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="e709c-115">Закрывайте оповещение с помощью трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="e709c-115">Close an alert through piping.</span></span>

## <span data-ttu-id="e709c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e709c-116">PARAMETERS</span></span>

### <span data-ttu-id="e709c-117">-Alert (оповещение)</span><span class="sxs-lookup"><span data-stu-id="e709c-117">-Alert</span></span>
<span data-ttu-id="e709c-118">Этот объект представляет собой предупредительный ресурс.</span><span class="sxs-lookup"><span data-stu-id="e709c-118">This object represents an alert resource.</span></span>
<span data-ttu-id="e709c-119">Для конструирования ознакомьтесь с разделом "Заметки" для свойств оповещения и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e709c-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="e709c-120">-AlertId</span></span>
<span data-ttu-id="e709c-121">Возвращает или задает идентификатор оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="e709c-122">-AlertProperty</span></span>
<span data-ttu-id="e709c-123">Свойства оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="e709c-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="e709c-125">Псевдоним пользователя, который закрыл оповещение.</span><span class="sxs-lookup"><span data-stu-id="e709c-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="e709c-126">-ClosedTimestamp</span></span>
<span data-ttu-id="e709c-127">Временная метка, когда оповещение было закрыто.</span><span class="sxs-lookup"><span data-stu-id="e709c-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="e709c-128">-CreatedTimestamp</span></span>
<span data-ttu-id="e709c-129">Метка времени создания оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e709c-130">-DefaultProfile</span></span>
<span data-ttu-id="e709c-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e709c-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e709c-132">-Описание</span><span class="sxs-lookup"><span data-stu-id="e709c-132">-Description</span></span>
<span data-ttu-id="e709c-133">Описание оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="e709c-134">-FaultId</span></span>
<span data-ttu-id="e709c-135">Возвращает или задает идентификатор ошибки оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="e709c-136">-FaultTypeId</span></span>
<span data-ttu-id="e709c-137">Возвращает или задает код типа ошибки для оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="e709c-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="e709c-139">Указывает, можно ли исправить это оповещение.</span><span class="sxs-lookup"><span data-stu-id="e709c-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="e709c-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="e709c-141">Отображаемое имя затронутого элемента.</span><span class="sxs-lookup"><span data-stu-id="e709c-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="e709c-142">-ImpactedResourceId</span></span>
<span data-ttu-id="e709c-143">Возвращает или задает идентификатор ресурса для затронутого элемента.</span><span class="sxs-lookup"><span data-stu-id="e709c-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e709c-144">-InputObject</span></span>
<span data-ttu-id="e709c-145">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="e709c-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="e709c-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="e709c-147">Метка времени последнего обновления оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-148">-Location</span><span class="sxs-lookup"><span data-stu-id="e709c-148">-Location</span></span>
<span data-ttu-id="e709c-149">Название региона</span><span class="sxs-lookup"><span data-stu-id="e709c-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="e709c-150">-Location1</span></span>
<span data-ttu-id="e709c-151">Регион Azure, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="e709c-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-152">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e709c-152">-Name</span></span>
<span data-ttu-id="e709c-153">Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-154">-Исправление</span><span class="sxs-lookup"><span data-stu-id="e709c-154">-Remediation</span></span>
<span data-ttu-id="e709c-155">Возвращает или задает понятные инструкции по исправлению для оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e709c-156">-ResourceGroupName</span></span>
<span data-ttu-id="e709c-157">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e709c-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="e709c-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="e709c-159">Возвращает или задает регистрационный идентификатор службы, которой принадлежит оповещение.</span><span class="sxs-lookup"><span data-stu-id="e709c-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="e709c-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="e709c-161">Возвращает или задает идентификатор регистрации ресурса, связанного с оповещением.</span><span class="sxs-lookup"><span data-stu-id="e709c-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="e709c-162">Если оповещение не связано с ресурсом, идентификатор регистрации ресурса равен null.</span><span class="sxs-lookup"><span data-stu-id="e709c-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-163">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="e709c-163">-Severity</span></span>
<span data-ttu-id="e709c-164">Уровень опасности оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-165">-State</span><span class="sxs-lookup"><span data-stu-id="e709c-165">-State</span></span>
<span data-ttu-id="e709c-166">Состояние оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e709c-167">-SubscriptionId</span></span>
<span data-ttu-id="e709c-168">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e709c-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e709c-169">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e709c-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-170">-Тег</span><span class="sxs-lookup"><span data-stu-id="e709c-170">-Tag</span></span>
<span data-ttu-id="e709c-171">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e709c-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-172">-Title</span><span class="sxs-lookup"><span data-stu-id="e709c-172">-Title</span></span>
<span data-ttu-id="e709c-173">Возвращает или задает идентификатор ресурса для затронутого элемента.</span><span class="sxs-lookup"><span data-stu-id="e709c-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-174">-Пользователь</span><span class="sxs-lookup"><span data-stu-id="e709c-174">-User</span></span>
<span data-ttu-id="e709c-175">Имя пользователя, используемое для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="e709c-175">The username used to perform the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e709c-176">-Confirm</span></span>
<span data-ttu-id="e709c-177">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e709c-177">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e709c-178">-WhatIf</span></span>
<span data-ttu-id="e709c-179">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e709c-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e709c-180">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e709c-180">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e709c-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e709c-181">CommonParameters</span></span>
<span data-ttu-id="e709c-182">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e709c-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e709c-183">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e709c-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e709c-184">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e709c-184">INPUTS</span></span>

### <span data-ttu-id="e709c-185">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="e709c-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="e709c-186">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e709c-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="e709c-187">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e709c-187">OUTPUTS</span></span>

### <span data-ttu-id="e709c-188">Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="e709c-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="e709c-189">Пуск</span><span class="sxs-lookup"><span data-stu-id="e709c-189">NOTES</span></span>

<span data-ttu-id="e709c-190">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e709c-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e709c-191">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e709c-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e709c-192">ПРЕДУПРЕЖДЕНИЕ <IAlert> : этот объект представляет собой предупредительный ресурс.</span><span class="sxs-lookup"><span data-stu-id="e709c-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="e709c-193">`[Location <String>]`: Область Azure, в которой находится ресурс</span><span class="sxs-lookup"><span data-stu-id="e709c-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="e709c-194">`[Tag <ITrackedResourceTags>]`: Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e709c-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="e709c-195">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="e709c-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e709c-196">`[AlertId <String>]`: Получает или задает идентификатор оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="e709c-197">`[AlertProperty <IAlertModelAlertProperties>]`: Свойства оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="e709c-198">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="e709c-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e709c-199">`[ClosedByUserAlias <String>]`: Псевдоним пользователя, который закрыл оповещение.</span><span class="sxs-lookup"><span data-stu-id="e709c-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="e709c-200">`[ClosedTimestamp <String>]`: Метка времени закрытия оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="e709c-201">`[CreatedTimestamp <String>]`: Метка времени создания оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="e709c-202">`[Description <IDictionary[]>]`: Описание оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="e709c-203">`[FaultId <String>]`: Получает или задает идентификатор ошибки оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="e709c-204">`[FaultTypeId <String>]`: Получает или задает идентификатор типа ошибки для оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="e709c-205">`[HasValidRemediationAction <Boolean?>]`: Указывает, можно ли исправить предупреждение.</span><span class="sxs-lookup"><span data-stu-id="e709c-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="e709c-206">`[ImpactedResourceDisplayName <String>]`: Отображаемое имя затронутого элемента.</span><span class="sxs-lookup"><span data-stu-id="e709c-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="e709c-207">`[ImpactedResourceId <String>]`: Возвращает или задает идентификатор ресурса для затронутого элемента.</span><span class="sxs-lookup"><span data-stu-id="e709c-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="e709c-208">`[LastUpdatedTimestamp <String>]`: Метка времени последнего обновления оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="e709c-209">`[Remediation <IDictionary[]>]`: Получает или задает понятные инструкции по исправлению для оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="e709c-210">`[ResourceProviderRegistrationId <String>]`: Получает или задает идентификатор регистрации службы, которой принадлежит оповещение.</span><span class="sxs-lookup"><span data-stu-id="e709c-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="e709c-211">`[ResourceRegistrationId <String>]`: Возвращает или задает идентификатор регистрации ресурса, связанного с оповещением.</span><span class="sxs-lookup"><span data-stu-id="e709c-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="e709c-212">Если оповещение не связано с ресурсом, идентификатор регистрации ресурса равен null.</span><span class="sxs-lookup"><span data-stu-id="e709c-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="e709c-213">`[Severity <String>]`: Серьезность оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="e709c-214">`[State <String>]`: Состояние оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="e709c-215">`[Title <String>]`: Возвращает или задает идентификатор ресурса для затронутого элемента.</span><span class="sxs-lookup"><span data-stu-id="e709c-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="e709c-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="e709c-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e709c-217">`[AlertName <String>]`: Имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="e709c-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="e709c-218">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="e709c-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e709c-219">`[Location <String>]`: Имя области</span><span class="sxs-lookup"><span data-stu-id="e709c-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="e709c-220">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e709c-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e709c-221">`[ResourceRegistrationId <String>]`: Идентификатор регистрации ресурса.</span><span class="sxs-lookup"><span data-stu-id="e709c-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="e709c-222">`[ServiceHealth <String>]`: Имя работоспособности службы.</span><span class="sxs-lookup"><span data-stu-id="e709c-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="e709c-223">`[ServiceRegistrationId <String>]`: Регистрационный идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="e709c-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="e709c-224">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e709c-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e709c-225">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="e709c-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e709c-226">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e709c-226">RELATED LINKS</span></span>
