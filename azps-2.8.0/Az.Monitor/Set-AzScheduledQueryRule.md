---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 142dfbf1e2a0868581d30aba344395cf264bb352
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903201"
---
# <span data-ttu-id="0e912-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e912-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="0e912-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e912-102">SYNOPSIS</span></span>
<span data-ttu-id="0e912-103">Обновляет правило оповещения в журнале</span><span class="sxs-lookup"><span data-stu-id="0e912-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="0e912-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e912-104">SYNTAX</span></span>

### <span data-ttu-id="0e912-105">ByRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e912-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e912-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0e912-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e912-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e912-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e912-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e912-108">DESCRIPTION</span></span>
<span data-ttu-id="0e912-109">Обновляет правило оповещения в журнале, переключая семантику.</span><span class="sxs-lookup"><span data-stu-id="0e912-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="0e912-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e912-110">EXAMPLES</span></span>

### <span data-ttu-id="0e912-111">Пример 1: задается именем правила</span><span class="sxs-lookup"><span data-stu-id="0e912-111">Example 1 - Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="0e912-112">Пример 2: Настройка с помощью объекта input</span><span class="sxs-lookup"><span data-stu-id="0e912-112">Example 2 - Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="0e912-113">Пример 3: Настройка по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="0e912-113">Example 3 - Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="0e912-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e912-114">PARAMETERS</span></span>

### <span data-ttu-id="0e912-115">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="0e912-115">-Action</span></span>
<span data-ttu-id="0e912-116">Действие предупреждения запланированного правила запроса</span><span class="sxs-lookup"><span data-stu-id="0e912-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e912-117">-AsJob</span></span>
<span data-ttu-id="0e912-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0e912-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e912-119">-DefaultProfile</span></span>
<span data-ttu-id="0e912-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e912-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e912-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="0e912-121">-Description</span></span>
<span data-ttu-id="0e912-122">Описание этого оповещения</span><span class="sxs-lookup"><span data-stu-id="0e912-122">The description for this alert</span></span>

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

### <span data-ttu-id="0e912-123">-Включено</span><span class="sxs-lookup"><span data-stu-id="0e912-123">-Enabled</span></span>
<span data-ttu-id="0e912-124">Состояние оповещения Azure — допустимые значения: $true, $false</span><span class="sxs-lookup"><span data-stu-id="0e912-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e912-125">-InputObject</span></span>
<span data-ttu-id="0e912-126">Запланированный ресурс правила запроса</span><span class="sxs-lookup"><span data-stu-id="0e912-126">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-127">-Location</span><span class="sxs-lookup"><span data-stu-id="0e912-127">-Location</span></span>
<span data-ttu-id="0e912-128">Расположение для этого оповещения.</span><span class="sxs-lookup"><span data-stu-id="0e912-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e912-129">-Name</span></span>
<span data-ttu-id="0e912-130">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="0e912-130">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e912-131">-ResourceGroupName</span></span>
<span data-ttu-id="0e912-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0e912-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e912-133">-ResourceId</span></span>
<span data-ttu-id="0e912-134">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="0e912-134">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-135">-Планирование</span><span class="sxs-lookup"><span data-stu-id="0e912-135">-Schedule</span></span>
<span data-ttu-id="0e912-136">Запланированное расписание для правила запроса</span><span class="sxs-lookup"><span data-stu-id="0e912-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-137">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="0e912-137">-Source</span></span>
<span data-ttu-id="0e912-138">Запланированный источник правил запроса</span><span class="sxs-lookup"><span data-stu-id="0e912-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="0e912-139">-Tag</span></span>
<span data-ttu-id="0e912-140">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="0e912-140">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e912-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e912-141">-Confirm</span></span>
<span data-ttu-id="0e912-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e912-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e912-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e912-143">-WhatIf</span></span>
<span data-ttu-id="0e912-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e912-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e912-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e912-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e912-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e912-146">CommonParameters</span></span>
<span data-ttu-id="0e912-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e912-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e912-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e912-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e912-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e912-149">INPUTS</span></span>

### <span data-ttu-id="0e912-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="0e912-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="0e912-151">System. String</span><span class="sxs-lookup"><span data-stu-id="0e912-151">System.String</span></span>

### <span data-ttu-id="0e912-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0e912-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="0e912-153">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0e912-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="0e912-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0e912-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="0e912-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e912-155">OUTPUTS</span></span>

### <span data-ttu-id="0e912-156">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="0e912-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="0e912-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e912-157">NOTES</span></span>

## <span data-ttu-id="0e912-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e912-158">RELATED LINKS</span></span>
