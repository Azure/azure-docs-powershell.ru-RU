---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 0351d6920c4af7f781ef27f4dfbc36a13e0c50cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244417"
---
# <span data-ttu-id="65a5d-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="65a5d-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="65a5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="65a5d-103">Обновляет правило оповещения в журнале</span><span class="sxs-lookup"><span data-stu-id="65a5d-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="65a5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65a5d-104">SYNTAX</span></span>

### <span data-ttu-id="65a5d-105">ByRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65a5d-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65a5d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="65a5d-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65a5d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65a5d-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65a5d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65a5d-108">DESCRIPTION</span></span>
<span data-ttu-id="65a5d-109">Обновляет правило оповещения в журнале, переключая семантику.</span><span class="sxs-lookup"><span data-stu-id="65a5d-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="65a5d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65a5d-110">EXAMPLES</span></span>

### <span data-ttu-id="65a5d-111">Пример 1: Настройка по имени правила</span><span class="sxs-lookup"><span data-stu-id="65a5d-111">Example 1: Set by rule name</span></span>
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

### <span data-ttu-id="65a5d-112">Пример 2: Настройка с помощью объекта ввода</span><span class="sxs-lookup"><span data-stu-id="65a5d-112">Example 2: Set by Input Object</span></span>
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

### <span data-ttu-id="65a5d-113">Пример 3: Настройка по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="65a5d-113">Example 3: Set by resource Id</span></span>
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

## <span data-ttu-id="65a5d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65a5d-114">PARAMETERS</span></span>

### <span data-ttu-id="65a5d-115">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="65a5d-115">-Action</span></span>
<span data-ttu-id="65a5d-116">Действие предупреждения запланированного правила запроса</span><span class="sxs-lookup"><span data-stu-id="65a5d-116">The scheduled query rule Alerting Action</span></span>

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

### <span data-ttu-id="65a5d-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65a5d-117">-AsJob</span></span>
<span data-ttu-id="65a5d-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="65a5d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65a5d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a5d-119">-DefaultProfile</span></span>
<span data-ttu-id="65a5d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65a5d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65a5d-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="65a5d-121">-Description</span></span>
<span data-ttu-id="65a5d-122">Описание этого оповещения</span><span class="sxs-lookup"><span data-stu-id="65a5d-122">The description for this alert</span></span>

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

### <span data-ttu-id="65a5d-123">-Включено</span><span class="sxs-lookup"><span data-stu-id="65a5d-123">-Enabled</span></span>
<span data-ttu-id="65a5d-124">Состояние оповещения Azure — допустимые значения: $true, $false</span><span class="sxs-lookup"><span data-stu-id="65a5d-124">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="65a5d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65a5d-125">-InputObject</span></span>
<span data-ttu-id="65a5d-126">Запланированный ресурс правила запроса</span><span class="sxs-lookup"><span data-stu-id="65a5d-126">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="65a5d-127">-Location</span><span class="sxs-lookup"><span data-stu-id="65a5d-127">-Location</span></span>
<span data-ttu-id="65a5d-128">Расположение для этого оповещения.</span><span class="sxs-lookup"><span data-stu-id="65a5d-128">The location for this alert</span></span>

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

### <span data-ttu-id="65a5d-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="65a5d-129">-Name</span></span>
<span data-ttu-id="65a5d-130">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="65a5d-130">The alert name</span></span>

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

### <span data-ttu-id="65a5d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65a5d-131">-ResourceGroupName</span></span>
<span data-ttu-id="65a5d-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="65a5d-132">The resource group name</span></span>

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

### <span data-ttu-id="65a5d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65a5d-133">-ResourceId</span></span>
<span data-ttu-id="65a5d-134">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="65a5d-134">The resource Id</span></span>

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

### <span data-ttu-id="65a5d-135">-Планирование</span><span class="sxs-lookup"><span data-stu-id="65a5d-135">-Schedule</span></span>
<span data-ttu-id="65a5d-136">Запланированное расписание для правила запроса</span><span class="sxs-lookup"><span data-stu-id="65a5d-136">The scheduled query rule schedule</span></span>

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

### <span data-ttu-id="65a5d-137">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="65a5d-137">-Source</span></span>
<span data-ttu-id="65a5d-138">Запланированный источник правил запроса</span><span class="sxs-lookup"><span data-stu-id="65a5d-138">The scheduled query rule source</span></span>

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

### <span data-ttu-id="65a5d-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="65a5d-139">-Tag</span></span>
<span data-ttu-id="65a5d-140">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="65a5d-140">Resource tags</span></span>

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

### <span data-ttu-id="65a5d-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65a5d-141">-Confirm</span></span>
<span data-ttu-id="65a5d-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="65a5d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65a5d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a5d-143">-WhatIf</span></span>
<span data-ttu-id="65a5d-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="65a5d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65a5d-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="65a5d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65a5d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a5d-146">CommonParameters</span></span>
<span data-ttu-id="65a5d-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65a5d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a5d-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65a5d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a5d-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65a5d-149">INPUTS</span></span>

### <span data-ttu-id="65a5d-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="65a5d-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="65a5d-151">System. String</span><span class="sxs-lookup"><span data-stu-id="65a5d-151">System.String</span></span>

### <span data-ttu-id="65a5d-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="65a5d-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="65a5d-153">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="65a5d-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="65a5d-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="65a5d-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="65a5d-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65a5d-155">OUTPUTS</span></span>

### <span data-ttu-id="65a5d-156">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="65a5d-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="65a5d-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="65a5d-157">NOTES</span></span>

## <span data-ttu-id="65a5d-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65a5d-158">RELATED LINKS</span></span>
