---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 65d402f06770542265bd9b0a6e9e50cd943114f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015592"
---
# <span data-ttu-id="ee02e-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="ee02e-101">Set-AzActionRule</span></span>

## <span data-ttu-id="ee02e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee02e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee02e-103">Создайте или обновйте правило действия.</span><span class="sxs-lookup"><span data-stu-id="ee02e-103">Create or update an action rule.</span></span>

## <span data-ttu-id="ee02e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee02e-104">SYNTAX</span></span>

### <span data-ttu-id="ee02e-105">BySimplifiedFormatDiagnosticsActionRule (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee02e-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee02e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ee02e-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee02e-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="ee02e-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee02e-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="ee02e-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee02e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee02e-109">DESCRIPTION</span></span>
<span data-ttu-id="ee02e-110">**Set-AzActionRule** создает или обновляет правило действия.</span><span class="sxs-lookup"><span data-stu-id="ee02e-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="ee02e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee02e-111">EXAMPLES</span></span>

### <span data-ttu-id="ee02e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee02e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="ee02e-113">Этот cmdlet создает правило действия для использования supression с областью действия подписки.</span><span class="sxs-lookup"><span data-stu-id="ee02e-113">This cmdlet creates an action rule for supression, with a subscription scope.</span></span>

### <span data-ttu-id="ee02e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee02e-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="ee02e-115">Этот cmdlet создает правило действия для группы действий со списком области групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee02e-115">This cmdlet creates an action rule for action group, with a list of resource groups scope.</span></span>

### <span data-ttu-id="ee02e-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ee02e-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab/providers/microsoft.insights/metricAlerts/Total Requests Exceeded" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="ee02e-117">Этот cmdlet создает правило действия для параметров диагностики с областью ресурса.</span><span class="sxs-lookup"><span data-stu-id="ee02e-117">This cmdlet creates an action rule for diagnostics settings, with a resource scope.</span></span>

## <span data-ttu-id="ee02e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee02e-118">PARAMETERS</span></span>

### <span data-ttu-id="ee02e-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="ee02e-119">-ActionGroupId</span></span>
<span data-ttu-id="ee02e-120">ИД группы действий, о которой нужно получить уведомление.</span><span class="sxs-lookup"><span data-stu-id="ee02e-120">Action Group Id which is to be notified.</span></span>

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

### <span data-ttu-id="ee02e-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="ee02e-121">-ActionRuleType</span></span>
<span data-ttu-id="ee02e-122">Формат Json правила действия</span><span class="sxs-lookup"><span data-stu-id="ee02e-122">Action rule Json format</span></span>

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

### <span data-ttu-id="ee02e-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="ee02e-123">-AlertContextCondition</span></span>
<span data-ttu-id="ee02e-124">Ожидаемый формат - { \<operation\> : \<comma separated list of values\> } Для eg.</span><span class="sxs-lookup"><span data-stu-id="ee02e-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ee02e-125">Содержит:smartgroups</span><span class="sxs-lookup"><span data-stu-id="ee02e-125">Contains:smartgroups</span></span>

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

### <span data-ttu-id="ee02e-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="ee02e-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="ee02e-127">Ожидаемый формат - { \<operation\> : \<comma separated list of values\> } Для eg.</span><span class="sxs-lookup"><span data-stu-id="ee02e-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ee02e-128">Равно:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span><span class="sxs-lookup"><span data-stu-id="ee02e-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

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

### <span data-ttu-id="ee02e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee02e-129">-DefaultProfile</span></span>
<span data-ttu-id="ee02e-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee02e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee02e-131">-Description</span><span class="sxs-lookup"><span data-stu-id="ee02e-131">-Description</span></span>
<span data-ttu-id="ee02e-132">Описание правила действия</span><span class="sxs-lookup"><span data-stu-id="ee02e-132">Description of Action Rule</span></span>

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

### <span data-ttu-id="ee02e-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="ee02e-133">-DescriptionCondition</span></span>
<span data-ttu-id="ee02e-134">Ожидаемый формат - { \<operation\> : \<comma separated list of values\> } Для eg.</span><span class="sxs-lookup"><span data-stu-id="ee02e-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ee02e-135">Содержит:тестовая оповещение</span><span class="sxs-lookup"><span data-stu-id="ee02e-135">Contains:Test Alert</span></span>

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

### <span data-ttu-id="ee02e-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee02e-136">-InputObject</span></span>
<span data-ttu-id="ee02e-137">Ресурс правила действия</span><span class="sxs-lookup"><span data-stu-id="ee02e-137">The action rule resource</span></span>

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

### <span data-ttu-id="ee02e-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="ee02e-138">-MonitorCondition</span></span>
<span data-ttu-id="ee02e-139">Ожидаемый формат - { \<operation\> : \<comma separated list of values\> } Для eg.</span><span class="sxs-lookup"><span data-stu-id="ee02e-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ee02e-140">NotEquals:Resolved</span><span class="sxs-lookup"><span data-stu-id="ee02e-140">NotEquals:Resolved</span></span>

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

### <span data-ttu-id="ee02e-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="ee02e-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="ee02e-142">Ожидаемый формат - { \<operation\> : \<comma separated list of values\> } Для eg.</span><span class="sxs-lookup"><span data-stu-id="ee02e-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ee02e-143">Equals:Platform,Log Analytics</span><span class="sxs-lookup"><span data-stu-id="ee02e-143">Equals:Platform,Log Analytics</span></span>

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

### <span data-ttu-id="ee02e-144">-Name</span><span class="sxs-lookup"><span data-stu-id="ee02e-144">-Name</span></span>
<span data-ttu-id="ee02e-145">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="ee02e-145">Action rule Name</span></span>

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

### <span data-ttu-id="ee02e-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="ee02e-146">-ReccurenceType</span></span>
<span data-ttu-id="ee02e-147">Определяет продолжительность, когда следует применить подавляние.</span><span class="sxs-lookup"><span data-stu-id="ee02e-147">Specifies the duration when the suppression should be applied.</span></span>

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

### <span data-ttu-id="ee02e-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="ee02e-148">-ReccurentValue</span></span>
<span data-ttu-id="ee02e-149">Reccurent values, if applicable. Для еженедельного 1,2 в случае с ежемесячной \[ \] - \[ 1,3,5,30\]</span><span class="sxs-lookup"><span data-stu-id="ee02e-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

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

### <span data-ttu-id="ee02e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee02e-150">-ResourceGroupName</span></span>
<span data-ttu-id="ee02e-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ee02e-151">Resource Group Name</span></span>

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

### <span data-ttu-id="ee02e-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="ee02e-152">-Scope</span></span>
<span data-ttu-id="ee02e-153">Список значений, разделенных запятой</span><span class="sxs-lookup"><span data-stu-id="ee02e-153">Comma separated list of values</span></span>

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

### <span data-ttu-id="ee02e-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="ee02e-154">-SeverityCondition</span></span>
<span data-ttu-id="ee02e-155">Ожидаемый формат - { \<operation\> : \<comma separated list of values\> } Для eg.</span><span class="sxs-lookup"><span data-stu-id="ee02e-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ee02e-156">Равно:Сев0,Сев1</span><span class="sxs-lookup"><span data-stu-id="ee02e-156">Equals:Sev0,Sev1</span></span>

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

### <span data-ttu-id="ee02e-157">-Status</span><span class="sxs-lookup"><span data-stu-id="ee02e-157">-Status</span></span>
<span data-ttu-id="ee02e-158">Состояние правила действия.</span><span class="sxs-lookup"><span data-stu-id="ee02e-158">Status of Action Rule.</span></span>

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

### <span data-ttu-id="ee02e-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="ee02e-159">-SuppressionEndTime</span></span>
<span data-ttu-id="ee02e-160">Время окончания подавления.</span><span class="sxs-lookup"><span data-stu-id="ee02e-160">Suppression End Time.</span></span>
<span data-ttu-id="ee02e-161">Формат 09.12.2018 06:00:00 +следует упомянуть в случае с календарным расписанием сукурсии : один раз, ежедневно, еженедельно или ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="ee02e-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="ee02e-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="ee02e-162">-SuppressionStartTime</span></span>
<span data-ttu-id="ee02e-163">Время начала подавления.</span><span class="sxs-lookup"><span data-stu-id="ee02e-163">Suppression Start Time.</span></span>
<span data-ttu-id="ee02e-164">Формат 09.12.2018 06:00:00 +следует упомянуть в случае с календарным расписанием сукурсии : один раз, ежедневно, еженедельно или ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="ee02e-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

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

### <span data-ttu-id="ee02e-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="ee02e-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="ee02e-166">Ожидаемый формат - { \<operation\> : \<comma separated list of values\> } Для eg.</span><span class="sxs-lookup"><span data-stu-id="ee02e-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="ee02e-167">Contains:Virtual Machines,Storage Account</span><span class="sxs-lookup"><span data-stu-id="ee02e-167">Contains:Virtual Machines,Storage Account</span></span>

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

### <span data-ttu-id="ee02e-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee02e-168">-Confirm</span></span>
<span data-ttu-id="ee02e-169">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ee02e-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee02e-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee02e-170">-WhatIf</span></span>
<span data-ttu-id="ee02e-171">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee02e-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee02e-172">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ee02e-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee02e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee02e-173">CommonParameters</span></span>
<span data-ttu-id="ee02e-174">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee02e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee02e-175">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee02e-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee02e-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee02e-176">INPUTS</span></span>

### <span data-ttu-id="ee02e-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="ee02e-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="ee02e-178">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee02e-178">OUTPUTS</span></span>

### <span data-ttu-id="ee02e-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="ee02e-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="ee02e-180">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee02e-180">NOTES</span></span>

## <span data-ttu-id="ee02e-181">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee02e-181">RELATED LINKS</span></span>
