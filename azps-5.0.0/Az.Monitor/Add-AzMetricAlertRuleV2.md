---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 0317f21231edd2608492d37609ab4f4849ba9c20
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250055"
---
# <span data-ttu-id="628d1-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="628d1-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="628d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="628d1-102">SYNOPSIS</span></span>
<span data-ttu-id="628d1-103">Добавляет или обновляет правило оповещений на основе метрик v2 (не классический).</span><span class="sxs-lookup"><span data-stu-id="628d1-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="628d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="628d1-104">SYNTAX</span></span>

### <span data-ttu-id="628d1-105">CreateAlertByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="628d1-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="628d1-106">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="628d1-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="628d1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="628d1-107">DESCRIPTION</span></span>
<span data-ttu-id="628d1-108">Добавляет или обновляет **правило оповещений на основе метрик v2 (не классический)**.</span><span class="sxs-lookup"><span data-stu-id="628d1-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="628d1-109">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="628d1-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="628d1-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="628d1-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="628d1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="628d1-111">EXAMPLES</span></span>

### <span data-ttu-id="628d1-112">Пример 1: Добавление правила оповещения метрики для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="628d1-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="628d1-113">Эта команда создает правило оповещения метрик для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="628d1-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="628d1-114">$condition является выводом командлета [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) , а $ACT является результатом командлета [New-AzActionGroup](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup)</span><span class="sxs-lookup"><span data-stu-id="628d1-114">$condition is the output of [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria) cmdlet and $act is the output of [New-AzActionGroup](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup) cmdlet</span></span>

### <span data-ttu-id="628d1-115">Пример 2: Добавление правила оповещения метрики для всех виртуальных машин в подписке</span><span class="sxs-lookup"><span data-stu-id="628d1-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="628d1-116">Эта команда создает правило оповещения метрик для всех виртуальных машин в подписке, которые находятся в eastus</span><span class="sxs-lookup"><span data-stu-id="628d1-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="628d1-117">Пример 3: отключение правила оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="628d1-117">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="628d1-118">Эта команда отключает правило оповещения метрики.</span><span class="sxs-lookup"><span data-stu-id="628d1-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="628d1-119">Здесь мы выведем выходные данные [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) для [добавления AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span><span class="sxs-lookup"><span data-stu-id="628d1-119">Here, we are piping output of [Get-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricalertrulev2) to [Add-AzMetricAlertRuleV2](https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2)</span></span> 

### <span data-ttu-id="628d1-120">Пример 4: Добавление правила оповещения метрики с измерениями</span><span class="sxs-lookup"><span data-stu-id="628d1-120">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="628d1-121">Чтобы создать более сложное правило оповещения, например те, которые включают выделять значения измерения или задать несколько условий, можно использовать командлеты helper [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) и [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span><span class="sxs-lookup"><span data-stu-id="628d1-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets [New-AzMetricAlertRuleV2DimensionSelection](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2dimensionselection) and [New-AzMetricAlertRuleV2Criteria](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria).</span></span>

<span data-ttu-id="628d1-122">Над набором командлетов будет создано правило оповещения метрики с измерениями.</span><span class="sxs-lookup"><span data-stu-id="628d1-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="628d1-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="628d1-123">PARAMETERS</span></span>

### <span data-ttu-id="628d1-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="628d1-124">-ActionGroup</span></span>
<span data-ttu-id="628d1-125">Группа "действия" для правила</span><span class="sxs-lookup"><span data-stu-id="628d1-125">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-126">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="628d1-126">-ActionGroupId</span></span>
<span data-ttu-id="628d1-127">Идентификатор группы действий для правила.</span><span class="sxs-lookup"><span data-stu-id="628d1-127">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-128">-Условие</span><span class="sxs-lookup"><span data-stu-id="628d1-128">-Condition</span></span>
<span data-ttu-id="628d1-129">Условие для правила</span><span class="sxs-lookup"><span data-stu-id="628d1-129">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="628d1-130">-DefaultProfile</span></span>
<span data-ttu-id="628d1-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="628d1-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="628d1-132">-Описание</span><span class="sxs-lookup"><span data-stu-id="628d1-132">-Description</span></span>
<span data-ttu-id="628d1-133">Описание правила оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="628d1-133">The description of the metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="628d1-134">-DisableRule</span></span>
<span data-ttu-id="628d1-135">Флаг отключения правила (состояние)</span><span class="sxs-lookup"><span data-stu-id="628d1-135">The disable rule (status) flag</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-136">-Частота</span><span class="sxs-lookup"><span data-stu-id="628d1-136">-Frequency</span></span>
<span data-ttu-id="628d1-137">Периодичность оценки для правила</span><span class="sxs-lookup"><span data-stu-id="628d1-137">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="628d1-138">-Name</span></span>
<span data-ttu-id="628d1-139">Имя правила оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="628d1-139">The name of metric alert rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="628d1-140">-ResourceGroupName</span></span>
<span data-ttu-id="628d1-141">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="628d1-141">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-142">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="628d1-142">-Severity</span></span>
<span data-ttu-id="628d1-143">Уровень важности для правила оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="628d1-143">The severity for the metric alert rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="628d1-144">-TargetResourceId</span></span>
<span data-ttu-id="628d1-145">Идентификатор целевого ресурса для правила</span><span class="sxs-lookup"><span data-stu-id="628d1-145">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="628d1-146">-TargetResourceRegion</span></span>
<span data-ttu-id="628d1-147">Целевая область ресурсов для правила</span><span class="sxs-lookup"><span data-stu-id="628d1-147">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="628d1-148">-TargetResourceScope</span></span>
<span data-ttu-id="628d1-149">Целевая область ресурсов для правила</span><span class="sxs-lookup"><span data-stu-id="628d1-149">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="628d1-150">-TargetResourceType</span></span>
<span data-ttu-id="628d1-151">Тип целевого ресурса для правила</span><span class="sxs-lookup"><span data-stu-id="628d1-151">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="628d1-152">-WindowSize</span></span>
<span data-ttu-id="628d1-153">Размер окна для правила</span><span class="sxs-lookup"><span data-stu-id="628d1-153">The window size for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="628d1-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="628d1-154">-Confirm</span></span>
<span data-ttu-id="628d1-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="628d1-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="628d1-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="628d1-156">-WhatIf</span></span>
<span data-ttu-id="628d1-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="628d1-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="628d1-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="628d1-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="628d1-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628d1-159">CommonParameters</span></span>
<span data-ttu-id="628d1-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="628d1-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628d1-161">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="628d1-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628d1-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="628d1-162">INPUTS</span></span>

### <span data-ttu-id="628d1-163">System. String</span><span class="sxs-lookup"><span data-stu-id="628d1-163">System.String</span></span>

### <span data-ttu-id="628d1-164">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="628d1-164">System.TimeSpan</span></span>

### <span data-ttu-id="628d1-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="628d1-165">System.String[]</span></span>

### <span data-ttu-id="628d1-166">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. командлеты. Monitor, версия = 1.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="628d1-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="628d1-167">Microsoft. Azure. Management. Monitor. Models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="628d1-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="628d1-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="628d1-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="628d1-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="628d1-169">System.Int32</span></span>

## <span data-ttu-id="628d1-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="628d1-170">OUTPUTS</span></span>

### <span data-ttu-id="628d1-171">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="628d1-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="628d1-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="628d1-172">NOTES</span></span>

## <span data-ttu-id="628d1-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="628d1-173">RELATED LINKS</span></span>
