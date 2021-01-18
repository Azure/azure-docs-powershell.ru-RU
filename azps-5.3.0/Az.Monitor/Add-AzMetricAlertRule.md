---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: cb3669c955182e54b6ddd3623f732402a15ea906
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507670"
---
# <span data-ttu-id="4fc64-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="4fc64-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="4fc64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fc64-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc64-103">Добавляет или обновляет правило оповещения, основанное на метрической системе.</span><span class="sxs-lookup"><span data-stu-id="4fc64-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="4fc64-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4fc64-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc64-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fc64-105">DESCRIPTION</span></span>
<span data-ttu-id="4fc64-106">С **помощью cmdlet Add-AzMetricAlertRule** можно добавить или обновить правило оповещения на основе метрических данных.</span><span class="sxs-lookup"><span data-stu-id="4fc64-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="4fc64-107">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="4fc64-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="4fc64-108">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед созданием, изменением или удалением ресурса.</span><span class="sxs-lookup"><span data-stu-id="4fc64-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4fc64-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4fc64-109">EXAMPLES</span></span>

### <span data-ttu-id="4fc64-110">Пример 1. Добавление правила метрических оповещений на веб-сайт</span><span class="sxs-lookup"><span data-stu-id="4fc64-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="4fc64-111">Эта команда создает правило метрических оповещений для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="4fc64-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="4fc64-112">Пример 2. Отключение правила</span><span class="sxs-lookup"><span data-stu-id="4fc64-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="4fc64-113">Эта команда отключает правило.</span><span class="sxs-lookup"><span data-stu-id="4fc64-113">This command disables a rule.</span></span>
<span data-ttu-id="4fc64-114">Если такое правило не существует, оно отключит его.</span><span class="sxs-lookup"><span data-stu-id="4fc64-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="4fc64-115">Если правило существует, оно просто отключает его.</span><span class="sxs-lookup"><span data-stu-id="4fc64-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="4fc64-116">Пример 3. Добавление правила с действиями</span><span class="sxs-lookup"><span data-stu-id="4fc64-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="4fc64-117">Эта команда создает правило метрических оповещений для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="4fc64-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="4fc64-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fc64-118">PARAMETERS</span></span>

### <span data-ttu-id="4fc64-119">-Action</span><span class="sxs-lookup"><span data-stu-id="4fc64-119">-Action</span></span>
<span data-ttu-id="4fc64-120">Определяет список действий, разделенных запятой.</span><span class="sxs-lookup"><span data-stu-id="4fc64-120">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc64-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc64-121">-DefaultProfile</span></span>
<span data-ttu-id="4fc64-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4fc64-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fc64-123">-Description</span><span class="sxs-lookup"><span data-stu-id="4fc64-123">-Description</span></span>
<span data-ttu-id="4fc64-124">Описание правила.</span><span class="sxs-lookup"><span data-stu-id="4fc64-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="4fc64-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="4fc64-125">-DisableRule</span></span>
<span data-ttu-id="4fc64-126">Отключает правило.</span><span class="sxs-lookup"><span data-stu-id="4fc64-126">Disables the rule.</span></span>
<span data-ttu-id="4fc64-127">Если этот параметр не задан, правило включено.</span><span class="sxs-lookup"><span data-stu-id="4fc64-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="4fc64-128">-Location</span><span class="sxs-lookup"><span data-stu-id="4fc64-128">-Location</span></span>
<span data-ttu-id="4fc64-129">Определяет расположение, в котором определено правило.</span><span class="sxs-lookup"><span data-stu-id="4fc64-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="4fc64-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="4fc64-130">-MetricName</span></span>
<span data-ttu-id="4fc64-131">Указывает имя метрики, отслеживаемой правилом.</span><span class="sxs-lookup"><span data-stu-id="4fc64-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="4fc64-132">Укажите этот параметр только для правил на основе метрики.</span><span class="sxs-lookup"><span data-stu-id="4fc64-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="4fc64-133">-Name</span><span class="sxs-lookup"><span data-stu-id="4fc64-133">-Name</span></span>
<span data-ttu-id="4fc64-134">Указывает имя правила.</span><span class="sxs-lookup"><span data-stu-id="4fc64-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="4fc64-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="4fc64-135">-Operator</span></span>
<span data-ttu-id="4fc64-136">Определяет реляционный оператор для условия правила.</span><span class="sxs-lookup"><span data-stu-id="4fc64-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="4fc64-137">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="4fc64-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4fc64-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="4fc64-138">GreaterThan</span></span>
- <span data-ttu-id="4fc64-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="4fc64-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="4fc64-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="4fc64-140">LessThan</span></span>
- <span data-ttu-id="4fc64-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="4fc64-141">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc64-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc64-142">-ResourceGroupName</span></span>
<span data-ttu-id="4fc64-143">Имя группы ресурсов для правила.</span><span class="sxs-lookup"><span data-stu-id="4fc64-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="4fc64-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4fc64-144">-TargetResourceId</span></span>
<span data-ttu-id="4fc64-145">Указывает ИД ресурса, который отслеживается правилом.</span><span class="sxs-lookup"><span data-stu-id="4fc64-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="4fc64-146">ПРИМЕЧАНИЕ. Это свойство невозможно обновить для существующего правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="4fc64-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="4fc64-147">-Пороговое значение</span><span class="sxs-lookup"><span data-stu-id="4fc64-147">-Threshold</span></span>
<span data-ttu-id="4fc64-148">Пороговое значение правила.</span><span class="sxs-lookup"><span data-stu-id="4fc64-148">Specifies the threshold of the rule.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc64-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="4fc64-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="4fc64-150">Указывает оператор агрегирования, который будет применяться к периоду времени при оценке правила.</span><span class="sxs-lookup"><span data-stu-id="4fc64-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases:
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc64-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="4fc64-151">-WindowSize</span></span>
<span data-ttu-id="4fc64-152">Определяет размер окна времени, заданный правилом для вычисления данных.</span><span class="sxs-lookup"><span data-stu-id="4fc64-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="4fc64-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fc64-153">-Confirm</span></span>
<span data-ttu-id="4fc64-154">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4fc64-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc64-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc64-155">-WhatIf</span></span>
<span data-ttu-id="4fc64-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fc64-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fc64-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4fc64-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc64-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc64-158">CommonParameters</span></span>
<span data-ttu-id="4fc64-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc64-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc64-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fc64-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc64-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4fc64-161">INPUTS</span></span>

### <span data-ttu-id="4fc64-162">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="4fc64-162">System.TimeSpan</span></span>

### <span data-ttu-id="4fc64-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="4fc64-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="4fc64-164">System.Double</span><span class="sxs-lookup"><span data-stu-id="4fc64-164">System.Double</span></span>

### <span data-ttu-id="4fc64-165">System.String</span><span class="sxs-lookup"><span data-stu-id="4fc64-165">System.String</span></span>

### <span data-ttu-id="4fc64-166">System.Nullable'1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4fc64-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4fc64-167">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4fc64-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4fc64-168">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4fc64-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4fc64-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4fc64-169">OUTPUTS</span></span>

### <span data-ttu-id="4fc64-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4fc64-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="4fc64-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4fc64-171">NOTES</span></span>

## <span data-ttu-id="4fc64-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fc64-172">RELATED LINKS</span></span>

[<span data-ttu-id="4fc64-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4fc64-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="4fc64-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="4fc64-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="4fc64-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="4fc64-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="4fc64-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="4fc64-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="4fc64-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="4fc64-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="4fc64-178">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="4fc64-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="4fc64-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="4fc64-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


