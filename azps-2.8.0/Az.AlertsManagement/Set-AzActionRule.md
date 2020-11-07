---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 15b847034300d01df354cc7512305ffd3cab8279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728179"
---
# <span data-ttu-id="f9f73-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="f9f73-101">Set-AzActionRule</span></span>

## <span data-ttu-id="f9f73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9f73-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f73-103">Создание или обновление правила действия.</span><span class="sxs-lookup"><span data-stu-id="f9f73-103">Create or update an action rule.</span></span>

## <span data-ttu-id="f9f73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9f73-104">SYNTAX</span></span>

### <span data-ttu-id="f9f73-105">BySimplifiedFormatDiagnosticsActionRule (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f9f73-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9f73-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f9f73-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9f73-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="f9f73-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9f73-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="f9f73-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9f73-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9f73-109">DESCRIPTION</span></span>
<span data-ttu-id="f9f73-110">**Set-AzActionRule** создает или обновляет правило действия.</span><span class="sxs-lookup"><span data-stu-id="f9f73-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="f9f73-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9f73-111">EXAMPLES</span></span>

### <span data-ttu-id="f9f73-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9f73-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="f9f73-113">Этот командлет создает правило действия для supression.</span><span class="sxs-lookup"><span data-stu-id="f9f73-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="f9f73-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f9f73-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="f9f73-115">Этот командлет создает правило действия для группы действий.</span><span class="sxs-lookup"><span data-stu-id="f9f73-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="f9f73-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f9f73-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="f9f73-117">Этот командлет создает правило действия для параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="f9f73-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="f9f73-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9f73-118">PARAMETERS</span></span>

### <span data-ttu-id="f9f73-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="f9f73-119">-ActionGroupId</span></span>
<span data-ttu-id="f9f73-120">Идентификатор группы действий, для которой необходимо получать уведомления.</span><span class="sxs-lookup"><span data-stu-id="f9f73-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="f9f73-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="f9f73-121">-ActionRuleType</span></span>
<span data-ttu-id="f9f73-122">Формат JSON правила действия</span><span class="sxs-lookup"><span data-stu-id="f9f73-122">Action rule Json format</span></span>

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

### <span data-ttu-id="f9f73-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="f9f73-123">-AlertContextCondition</span></span>
<span data-ttu-id="f9f73-124">Ожидаемый формат — { \< операция \> : \< список значений, разделенных запятыми, для типа " \> Пример".</span><span class="sxs-lookup"><span data-stu-id="f9f73-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="f9f73-125">Contains: smartgroups</span><span class="sxs-lookup"><span data-stu-id="f9f73-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="f9f73-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="f9f73-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="f9f73-127">Ожидаемый формат — { \< операция \> : \< список значений, разделенных запятыми, для типа " \> Пример".</span><span class="sxs-lookup"><span data-stu-id="f9f73-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="f9f73-128">Equals:/Subscriptions/ad825170-845c-47dB-8f00-11978947b089/resourceGroups/abvarma/providers/metricAlerts/Test-mrmc-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="f9f73-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="f9f73-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f73-129">-DefaultProfile</span></span>
<span data-ttu-id="f9f73-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9f73-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9f73-131">-Описание</span><span class="sxs-lookup"><span data-stu-id="f9f73-131">-Description</span></span>
<span data-ttu-id="f9f73-132">Описание правила действия</span><span class="sxs-lookup"><span data-stu-id="f9f73-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="f9f73-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="f9f73-133">-DescriptionCondition</span></span>
<span data-ttu-id="f9f73-134">Ожидаемый формат — { \< операция \> : \< список значений, разделенных запятыми, для типа " \> Пример".</span><span class="sxs-lookup"><span data-stu-id="f9f73-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="f9f73-135">Contains: тестовое оповещение</span><span class="sxs-lookup"><span data-stu-id="f9f73-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="f9f73-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9f73-136">-InputObject</span></span>
<span data-ttu-id="f9f73-137">Ресурс правила действий</span><span class="sxs-lookup"><span data-stu-id="f9f73-137">The action rule resource</span></span>

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

### <span data-ttu-id="f9f73-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="f9f73-138">-MonitorCondition</span></span>
<span data-ttu-id="f9f73-139">Ожидаемый формат — { \< операция \> : \< список значений, разделенных запятыми, для типа " \> Пример".</span><span class="sxs-lookup"><span data-stu-id="f9f73-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="f9f73-140">NotEquals: разрешено</span><span class="sxs-lookup"><span data-stu-id="f9f73-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="f9f73-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="f9f73-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="f9f73-142">Ожидаемый формат — { \< операция \> : \< список значений, разделенных запятыми, для типа " \> Пример".</span><span class="sxs-lookup"><span data-stu-id="f9f73-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="f9f73-143">Equals: Platform, Analytics log</span><span class="sxs-lookup"><span data-stu-id="f9f73-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="f9f73-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9f73-144">-Name</span></span>
<span data-ttu-id="f9f73-145">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="f9f73-145">Action rule Name</span></span>

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

### <span data-ttu-id="f9f73-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="f9f73-146">-ReccurenceType</span></span>
<span data-ttu-id="f9f73-147">Указывает продолжительность применения подавления.</span><span class="sxs-lookup"><span data-stu-id="f9f73-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="f9f73-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="f9f73-148">-ReccurentValue</span></span>
<span data-ttu-id="f9f73-149">Reccurent значения, если это применимо. В случае еженедельных – \[ 1, 2 \] в случае ежемесячных – \[ 1, 3, 5, 30\]</span><span class="sxs-lookup"><span data-stu-id="f9f73-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="f9f73-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f73-150">-ResourceGroupName</span></span>
<span data-ttu-id="f9f73-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9f73-151">Resource Group Name</span></span>

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

### <span data-ttu-id="f9f73-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="f9f73-152">-Scope</span></span>
<span data-ttu-id="f9f73-153">Список значений, разделенных запятыми</span><span class="sxs-lookup"><span data-stu-id="f9f73-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="f9f73-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="f9f73-154">-SeverityCondition</span></span>
<span data-ttu-id="f9f73-155">Ожидаемый формат — { \< операция \> : \< список значений, разделенных запятыми, для типа " \> Пример".</span><span class="sxs-lookup"><span data-stu-id="f9f73-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="f9f73-156">Equals: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="f9f73-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="f9f73-157">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="f9f73-157">-Status</span></span>
<span data-ttu-id="f9f73-158">Состояние правила действия.</span><span class="sxs-lookup"><span data-stu-id="f9f73-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="f9f73-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="f9f73-159">-SuppressionEndTime</span></span>
<span data-ttu-id="f9f73-160">Время окончания подавления.</span><span class="sxs-lookup"><span data-stu-id="f9f73-160">Suppression End Time.</span></span>
<span data-ttu-id="f9f73-161">Формат 12/09/2018 06:00:00 + должен быть указан в случае расписания Reccurent Supression-once, Daily, еженедельно или ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="f9f73-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="f9f73-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="f9f73-162">-SuppressionStartTime</span></span>
<span data-ttu-id="f9f73-163">Время начала подавления.</span><span class="sxs-lookup"><span data-stu-id="f9f73-163">Suppression Start Time.</span></span>
<span data-ttu-id="f9f73-164">Формат 12/09/2018 06:00:00 + должен быть указан в случае расписания Reccurent Supression-once, Daily, еженедельно или ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="f9f73-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="f9f73-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="f9f73-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="f9f73-166">Ожидаемый формат — { \< операция \> : \< список значений, разделенных запятыми, для типа " \> Пример".</span><span class="sxs-lookup"><span data-stu-id="f9f73-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="f9f73-167">Contains: виртуальные машины, учетная запись хранилища</span><span class="sxs-lookup"><span data-stu-id="f9f73-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="f9f73-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9f73-168">-Confirm</span></span>
<span data-ttu-id="f9f73-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9f73-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f73-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f73-170">-WhatIf</span></span>
<span data-ttu-id="f9f73-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9f73-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9f73-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9f73-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f73-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f73-173">CommonParameters</span></span>
<span data-ttu-id="f9f73-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9f73-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f73-175">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9f73-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f73-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9f73-176">INPUTS</span></span>

### <span data-ttu-id="f9f73-177">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="f9f73-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="f9f73-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9f73-178">OUTPUTS</span></span>

### <span data-ttu-id="f9f73-179">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="f9f73-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="f9f73-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9f73-180">NOTES</span></span>

## <span data-ttu-id="f9f73-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9f73-181">RELATED LINKS</span></span>
