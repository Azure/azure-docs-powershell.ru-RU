---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 25854c3432f0ea28ee5eb267013992fce977b06a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94075019"
---
# <span data-ttu-id="803a7-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="803a7-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="803a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="803a7-102">SYNOPSIS</span></span>
<span data-ttu-id="803a7-103">Добавляет или обновляет правило оповещений на основе метрик v2 (не классический).</span><span class="sxs-lookup"><span data-stu-id="803a7-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="803a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="803a7-104">SYNTAX</span></span>

### <span data-ttu-id="803a7-105">CreateAlertByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="803a7-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="803a7-106">CreateAlertByResourceIdAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="803a7-106">CreateAlertByResourceIdAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="803a7-107">CreateAlertByResourceIdAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="803a7-107">CreateAlertByResourceIdAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="803a7-108">CreateAlertByScopes</span><span class="sxs-lookup"><span data-stu-id="803a7-108">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="803a7-109">CreateAlertByScopesAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="803a7-109">CreateAlertByScopesAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="803a7-110">CreateAlertByScopesAndActionGroupId</span><span class="sxs-lookup"><span data-stu-id="803a7-110">CreateAlertByScopesAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="803a7-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="803a7-111">DESCRIPTION</span></span>
<span data-ttu-id="803a7-112">Добавляет или обновляет **правило оповещений на основе метрик v2 (не классический)**.</span><span class="sxs-lookup"><span data-stu-id="803a7-112">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="803a7-113">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="803a7-113">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="803a7-114">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="803a7-114">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="803a7-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="803a7-115">EXAMPLES</span></span>

### <span data-ttu-id="803a7-116">Пример 1: Добавление правила оповещения метрики для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="803a7-116">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="803a7-117">Эта команда создает правило оповещения метрик для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="803a7-117">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="803a7-118">$condition является выводом New-AzMetricAlertRuleV2Criteria командлета, а $act является выводом командлета New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="803a7-118">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="803a7-119">Пример 2: Добавление правила оповещения метрики для всех виртуальных машин в подписке</span><span class="sxs-lookup"><span data-stu-id="803a7-119">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="803a7-120">Эта команда создает правило оповещения метрик для всех виртуальных машин в подписке, которые находятся в eastus</span><span class="sxs-lookup"><span data-stu-id="803a7-120">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="803a7-121">Пример 3: отключение правила оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="803a7-121">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="803a7-122">Эта команда отключает правило оповещения метрики.</span><span class="sxs-lookup"><span data-stu-id="803a7-122">This command disables a metric alert rule.</span></span> <span data-ttu-id="803a7-123">Здесь мы выведем вывод Get-AzMetricAlertRuleV2 в Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="803a7-123">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="803a7-124">Пример 4: Добавление правила оповещения метрики с измерениями</span><span class="sxs-lookup"><span data-stu-id="803a7-124">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="803a7-125">Чтобы создать более сложное правило оповещения, например те, которые включают выделять значения измерения или задать несколько условий, можно использовать вспомогательные командлеты New-AzMetricAlertRuleV2DimensionSelection и New-AzMetricAlertRuleV2Criteria.</span><span class="sxs-lookup"><span data-stu-id="803a7-125">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="803a7-126">Над набором командлетов будет создано правило оповещения метрики с измерениями.</span><span class="sxs-lookup"><span data-stu-id="803a7-126">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="803a7-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="803a7-127">PARAMETERS</span></span>

### <span data-ttu-id="803a7-128">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="803a7-128">-ActionGroup</span></span>
<span data-ttu-id="803a7-129">Группа "действия" для правила</span><span class="sxs-lookup"><span data-stu-id="803a7-129">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: CreateAlertByResourceIdAndActionGroup, CreateAlertByScopesAndActionGroup
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803a7-130">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="803a7-130">-ActionGroupId</span></span>
<span data-ttu-id="803a7-131">Идентификатор группы действий для правила.</span><span class="sxs-lookup"><span data-stu-id="803a7-131">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByResourceIdAndActionGroupId, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803a7-132">-Условие</span><span class="sxs-lookup"><span data-stu-id="803a7-132">-Condition</span></span>
<span data-ttu-id="803a7-133">Условие для правила</span><span class="sxs-lookup"><span data-stu-id="803a7-133">The condition for rule</span></span>

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

### <span data-ttu-id="803a7-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="803a7-134">-DefaultProfile</span></span>
<span data-ttu-id="803a7-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="803a7-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="803a7-136">-Описание</span><span class="sxs-lookup"><span data-stu-id="803a7-136">-Description</span></span>
<span data-ttu-id="803a7-137">Описание правила оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="803a7-137">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="803a7-138">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="803a7-138">-DisableRule</span></span>
<span data-ttu-id="803a7-139">Флаг отключения правила (состояние)</span><span class="sxs-lookup"><span data-stu-id="803a7-139">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="803a7-140">-Частота</span><span class="sxs-lookup"><span data-stu-id="803a7-140">-Frequency</span></span>
<span data-ttu-id="803a7-141">Периодичность оценки для правила</span><span class="sxs-lookup"><span data-stu-id="803a7-141">The evaluation frequency for rule</span></span>

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

### <span data-ttu-id="803a7-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="803a7-142">-Name</span></span>
<span data-ttu-id="803a7-143">Имя правила оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="803a7-143">The name of metric alert rule</span></span>

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

### <span data-ttu-id="803a7-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="803a7-144">-ResourceGroupName</span></span>
<span data-ttu-id="803a7-145">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="803a7-145">The Resource Group Name</span></span>

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

### <span data-ttu-id="803a7-146">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="803a7-146">-Severity</span></span>
<span data-ttu-id="803a7-147">Уровень важности для правила оповещения метрики</span><span class="sxs-lookup"><span data-stu-id="803a7-147">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="803a7-148">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="803a7-148">-TargetResourceId</span></span>
<span data-ttu-id="803a7-149">Идентификатор целевого ресурса для правила</span><span class="sxs-lookup"><span data-stu-id="803a7-149">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId, CreateAlertByResourceIdAndActionGroup, CreateAlertByResourceIdAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803a7-150">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="803a7-150">-TargetResourceRegion</span></span>
<span data-ttu-id="803a7-151">Целевая область ресурсов для правила</span><span class="sxs-lookup"><span data-stu-id="803a7-151">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803a7-152">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="803a7-152">-TargetResourceScope</span></span>
<span data-ttu-id="803a7-153">Целевая область ресурсов для правила</span><span class="sxs-lookup"><span data-stu-id="803a7-153">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803a7-154">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="803a7-154">-TargetResourceType</span></span>
<span data-ttu-id="803a7-155">Тип целевого ресурса для правила</span><span class="sxs-lookup"><span data-stu-id="803a7-155">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803a7-156">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="803a7-156">-WindowSize</span></span>
<span data-ttu-id="803a7-157">Размер окна для правила</span><span class="sxs-lookup"><span data-stu-id="803a7-157">The window size for rule</span></span>

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

### <span data-ttu-id="803a7-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="803a7-158">-Confirm</span></span>
<span data-ttu-id="803a7-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="803a7-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="803a7-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="803a7-160">-WhatIf</span></span>
<span data-ttu-id="803a7-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="803a7-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="803a7-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="803a7-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="803a7-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803a7-163">CommonParameters</span></span>
<span data-ttu-id="803a7-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="803a7-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803a7-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="803a7-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803a7-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="803a7-166">INPUTS</span></span>

### <span data-ttu-id="803a7-167">System. String</span><span class="sxs-lookup"><span data-stu-id="803a7-167">System.String</span></span>

### <span data-ttu-id="803a7-168">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="803a7-168">System.TimeSpan</span></span>

### <span data-ttu-id="803a7-169">System. String []</span><span class="sxs-lookup"><span data-stu-id="803a7-169">System.String[]</span></span>

### <span data-ttu-id="803a7-170">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. IPSMultiMetricCriteria, Microsoft. Azure. PowerShell. командлеты. Monitor, версия = 1.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="803a7-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="803a7-171">Microsoft. Azure. Management. Monitor. Models. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="803a7-171">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="803a7-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="803a7-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="803a7-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="803a7-173">System.Int32</span></span>

## <span data-ttu-id="803a7-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="803a7-174">OUTPUTS</span></span>

### <span data-ttu-id="803a7-175">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="803a7-175">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="803a7-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="803a7-176">NOTES</span></span>

## <span data-ttu-id="803a7-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="803a7-177">RELATED LINKS</span></span>
