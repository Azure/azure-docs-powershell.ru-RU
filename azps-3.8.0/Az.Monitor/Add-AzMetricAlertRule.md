---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: cb3669c955182e54b6ddd3623f732402a15ea906
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072988"
---
# <span data-ttu-id="eeb4c-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="eeb4c-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="eeb4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eeb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb4c-103">Добавляет или обновляет правило оповещения на основе метрики.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="eeb4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eeb4c-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb4c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeb4c-105">DESCRIPTION</span></span>
<span data-ttu-id="eeb4c-106">Командлет **Add-AzMetricAlertRule** добавляет или обновляет правило оповещения на основе метрики.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="eeb4c-107">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="eeb4c-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="eeb4c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eeb4c-109">EXAMPLES</span></span>

### <span data-ttu-id="eeb4c-110">Пример 1: Добавление правила оповещения метрики на веб-сайт</span><span class="sxs-lookup"><span data-stu-id="eeb4c-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="eeb4c-111">Эта команда создает правило оповещения метрики для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="eeb4c-112">Пример 2: отключение правила</span><span class="sxs-lookup"><span data-stu-id="eeb4c-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="eeb4c-113">Эта команда отключает правило.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-113">This command disables a rule.</span></span>
<span data-ttu-id="eeb4c-114">Если правило не существует, оно будет отключено.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="eeb4c-115">Если правило существует, оно просто отключается.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="eeb4c-116">Пример 3: Добавление правила с действиями</span><span class="sxs-lookup"><span data-stu-id="eeb4c-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="eeb4c-117">Эта команда создает правило оповещения метрики для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="eeb4c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eeb4c-118">PARAMETERS</span></span>

### <span data-ttu-id="eeb4c-119">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="eeb4c-119">-Action</span></span>
<span data-ttu-id="eeb4c-120">Указывает список действий, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="eeb4c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb4c-121">-DefaultProfile</span></span>
<span data-ttu-id="eeb4c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eeb4c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eeb4c-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="eeb4c-123">-Description</span></span>
<span data-ttu-id="eeb4c-124">Задает описание правила.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="eeb4c-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="eeb4c-125">-DisableRule</span></span>
<span data-ttu-id="eeb4c-126">Отключение правила.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-126">Disables the rule.</span></span>
<span data-ttu-id="eeb4c-127">Если этот параметр не указан, правило разрешено.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="eeb4c-128">-Location</span><span class="sxs-lookup"><span data-stu-id="eeb4c-128">-Location</span></span>
<span data-ttu-id="eeb4c-129">Указывает расположение, в котором определено правило.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="eeb4c-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="eeb4c-130">-MetricName</span></span>
<span data-ttu-id="eeb4c-131">Указывает имя метрики, которое отслеживает правило.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="eeb4c-132">Указывайте этот параметр только для правил на основе метрик.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="eeb4c-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eeb4c-133">-Name</span></span>
<span data-ttu-id="eeb4c-134">Задает имя правила.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="eeb4c-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="eeb4c-135">-Operator</span></span>
<span data-ttu-id="eeb4c-136">Указывает оператор отношения для условия правила.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="eeb4c-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eeb4c-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eeb4c-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="eeb4c-138">GreaterThan</span></span>
- <span data-ttu-id="eeb4c-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="eeb4c-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="eeb4c-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="eeb4c-140">LessThan</span></span>
- <span data-ttu-id="eeb4c-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="eeb4c-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="eeb4c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb4c-142">-ResourceGroupName</span></span>
<span data-ttu-id="eeb4c-143">Указывает имя группы ресурсов для правила.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="eeb4c-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="eeb4c-144">-TargetResourceId</span></span>
<span data-ttu-id="eeb4c-145">Указывает идентификатор ресурса, отслеживаемого правилом.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="eeb4c-146">Примечание. это свойство не может быть обновлено для существующего правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="eeb4c-147">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="eeb4c-147">-Threshold</span></span>
<span data-ttu-id="eeb4c-148">Указывает пороговое значение для правила.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="eeb4c-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="eeb4c-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="eeb4c-150">Задает оператор агрегирования, который будет применяться к окну времени при вычислении правила.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="eeb4c-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="eeb4c-151">-WindowSize</span></span>
<span data-ttu-id="eeb4c-152">Задает размер временного интервала для вычисления данных в правиле.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="eeb4c-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eeb4c-153">-Confirm</span></span>
<span data-ttu-id="eeb4c-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb4c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb4c-155">-WhatIf</span></span>
<span data-ttu-id="eeb4c-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eeb4c-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb4c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb4c-158">CommonParameters</span></span>
<span data-ttu-id="eeb4c-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eeb4c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb4c-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeb4c-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb4c-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eeb4c-161">INPUTS</span></span>

### <span data-ttu-id="eeb4c-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="eeb4c-162">System.TimeSpan</span></span>

### <span data-ttu-id="eeb4c-163">Microsoft. Azure. Management. Monitor. Management. Models. ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="eeb4c-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="eeb4c-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="eeb4c-164">System.Double</span></span>

### <span data-ttu-id="eeb4c-165">System. String</span><span class="sxs-lookup"><span data-stu-id="eeb4c-165">System.String</span></span>

### <span data-ttu-id="eeb4c-166">System. Nullable "1 [[Microsoft. Azure. Management. Monitor. Management. TimeAggregationOperator, Microsoft. Azure. PowerShell. командлеты: Monitor, версия = 1.0.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="eeb4c-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eeb4c-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eeb4c-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="eeb4c-168">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. RuleAction; Microsoft. Azure. PowerShell. командлеты. Monitor, версия = 1.0.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="eeb4c-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="eeb4c-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeb4c-169">OUTPUTS</span></span>

### <span data-ttu-id="eeb4c-170">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eeb4c-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="eeb4c-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="eeb4c-171">NOTES</span></span>

## <span data-ttu-id="eeb4c-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eeb4c-172">RELATED LINKS</span></span>

[<span data-ttu-id="eeb4c-173">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="eeb4c-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="eeb4c-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="eeb4c-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="eeb4c-175">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="eeb4c-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="eeb4c-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="eeb4c-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="eeb4c-177">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="eeb4c-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="eeb4c-178">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="eeb4c-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="eeb4c-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="eeb4c-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


