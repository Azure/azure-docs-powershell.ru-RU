---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 75a2071e8f60ed15420b69815eba22d6f82e9f82
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312125"
---
# <span data-ttu-id="c879d-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="c879d-101">Set-AzActionRule</span></span>

## <span data-ttu-id="c879d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c879d-102">SYNOPSIS</span></span>
<span data-ttu-id="c879d-103">Создание или обновление правила действия.</span><span class="sxs-lookup"><span data-stu-id="c879d-103">Create or update an action rule.</span></span>

## <span data-ttu-id="c879d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c879d-104">SYNTAX</span></span>

### <span data-ttu-id="c879d-105">BySimplifiedFormatDiagnosticsActionRule (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c879d-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c879d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c879d-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c879d-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="c879d-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c879d-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="c879d-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c879d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c879d-109">DESCRIPTION</span></span>
<span data-ttu-id="c879d-110">**Set-AzActionRule** создает или обновляет правило действия.</span><span class="sxs-lookup"><span data-stu-id="c879d-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="c879d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c879d-111">EXAMPLES</span></span>

### <span data-ttu-id="c879d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c879d-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="c879d-113">Этот командлет создает правило действия для supression с областью действия подписки.</span><span class="sxs-lookup"><span data-stu-id="c879d-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="c879d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c879d-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="c879d-115">Этот командлет создает правило действия для группы действий со списком области групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c879d-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="c879d-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c879d-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="c879d-117">Этот командлет создает правило действия для параметров диагностики с областью ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c879d-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="c879d-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c879d-118">PARAMETERS</span></span>

### <span data-ttu-id="c879d-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="c879d-119">-ActionGroupId</span></span>
<span data-ttu-id="c879d-120">Идентификатор группы действий, для которой необходимо получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="c879d-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="c879d-121">-ActionRuleType</span></span>
<span data-ttu-id="c879d-122">Формат JSON правила действия</span><span class="sxs-lookup"><span data-stu-id="c879d-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="c879d-123">-AlertContextCondition</span></span>
<span data-ttu-id="c879d-124">Ожидаемый формат — { \<operation\> :} для "например" \<comma separated list of values\> .</span><span class="sxs-lookup"><span data-stu-id="c879d-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c879d-125">Contains: smartgroups</span><span class="sxs-lookup"><span data-stu-id="c879d-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="c879d-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="c879d-127">Ожидаемый формат — { \<operation\> :} для "например" \<comma separated list of values\> .</span><span class="sxs-lookup"><span data-stu-id="c879d-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c879d-128">Equals:/Subscriptions/ad825170-845c-47dB-8f00-11978947b089/resourceGroups/abvarma/providers/metricAlerts/Test-mrmc-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="c879d-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c879d-129">-DefaultProfile</span></span>
<span data-ttu-id="c879d-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c879d-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-131">-Описание</span><span class="sxs-lookup"><span data-stu-id="c879d-131">-Description</span></span>
<span data-ttu-id="c879d-132">Описание правила действия</span><span class="sxs-lookup"><span data-stu-id="c879d-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="c879d-133">-DescriptionCondition</span></span>
<span data-ttu-id="c879d-134">Ожидаемый формат — { \<operation\> :} для "например" \<comma separated list of values\> .</span><span class="sxs-lookup"><span data-stu-id="c879d-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c879d-135">Contains: тестовое оповещение</span><span class="sxs-lookup"><span data-stu-id="c879d-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c879d-136">-InputObject</span></span>
<span data-ttu-id="c879d-137">Ресурс правила действий</span><span class="sxs-lookup"><span data-stu-id="c879d-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="c879d-138">-MonitorCondition</span></span>
<span data-ttu-id="c879d-139">Ожидаемый формат — { \<operation\> :} для "например" \<comma separated list of values\> .</span><span class="sxs-lookup"><span data-stu-id="c879d-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c879d-140">NotEquals: разрешено</span><span class="sxs-lookup"><span data-stu-id="c879d-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="c879d-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="c879d-142">Ожидаемый формат — { \<operation\> :} для "например" \<comma separated list of values\> .</span><span class="sxs-lookup"><span data-stu-id="c879d-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c879d-143">Equals: Platform, Analytics log</span><span class="sxs-lookup"><span data-stu-id="c879d-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c879d-144">-Name</span></span>
<span data-ttu-id="c879d-145">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="c879d-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="c879d-146">-ReccurenceType</span></span>
<span data-ttu-id="c879d-147">Указывает продолжительность применения подавления.</span><span class="sxs-lookup"><span data-stu-id="c879d-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="c879d-148">-ReccurentValue</span></span>
<span data-ttu-id="c879d-149">Reccurent значения, если это применимо. В случае еженедельных – \[ 1, 2 \] в случае ежемесячных – \[ 1, 3, 5, 30\]</span><span class="sxs-lookup"><span data-stu-id="c879d-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c879d-150">-ResourceGroupName</span></span>
<span data-ttu-id="c879d-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c879d-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="c879d-152">-Scope</span></span>
<span data-ttu-id="c879d-153">Список значений, разделенных запятыми</span><span class="sxs-lookup"><span data-stu-id="c879d-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="c879d-154">-SeverityCondition</span></span>
<span data-ttu-id="c879d-155">Ожидаемый формат — { \<operation\> :} для "например" \<comma separated list of values\> .</span><span class="sxs-lookup"><span data-stu-id="c879d-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c879d-156">Equals: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="c879d-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-157">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="c879d-157">-Status</span></span>
<span data-ttu-id="c879d-158">Состояние правила действия.</span><span class="sxs-lookup"><span data-stu-id="c879d-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="c879d-159">-SuppressionEndTime</span></span>
<span data-ttu-id="c879d-160">Время окончания подавления.</span><span class="sxs-lookup"><span data-stu-id="c879d-160">Suppression End Time.</span></span>
<span data-ttu-id="c879d-161">Формат 12/09/2018 06:00:00 + должен быть указан в случае расписания Reccurent Supression-once, Daily, еженедельно или ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="c879d-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="c879d-162">-SuppressionStartTime</span></span>
<span data-ttu-id="c879d-163">Время начала подавления.</span><span class="sxs-lookup"><span data-stu-id="c879d-163">Suppression Start Time.</span></span>
<span data-ttu-id="c879d-164">Формат 12/09/2018 06:00:00 + должен быть указан в случае расписания Reccurent Supression-once, Daily, еженедельно или ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="c879d-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="c879d-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="c879d-166">Ожидаемый формат — { \<operation\> :} для "например" \<comma separated list of values\> .</span><span class="sxs-lookup"><span data-stu-id="c879d-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c879d-167">Contains: виртуальные машины, учетная запись хранилища</span><span class="sxs-lookup"><span data-stu-id="c879d-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c879d-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c879d-168">-Confirm</span></span>
<span data-ttu-id="c879d-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c879d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c879d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c879d-170">-WhatIf</span></span>
<span data-ttu-id="c879d-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c879d-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c879d-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c879d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c879d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c879d-173">CommonParameters</span></span>
<span data-ttu-id="c879d-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c879d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c879d-175">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c879d-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c879d-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c879d-176">INPUTS</span></span>

### <span data-ttu-id="c879d-177">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="c879d-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="c879d-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c879d-178">OUTPUTS</span></span>

### <span data-ttu-id="c879d-179">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="c879d-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="c879d-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="c879d-180">NOTES</span></span>

## <span data-ttu-id="c879d-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c879d-181">RELATED LINKS</span></span>
