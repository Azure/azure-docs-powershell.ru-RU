---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 155a34133b9fa03c1f056fd65a0ec202fc0aed72
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732482"
---
# <span data-ttu-id="e7eda-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e7eda-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="e7eda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7eda-102">SYNOPSIS</span></span>
<span data-ttu-id="e7eda-103">Добавляет или обновляет правило оповещения на основе метрики.</span><span class="sxs-lookup"><span data-stu-id="e7eda-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7eda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7eda-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7eda-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7eda-105">DESCRIPTION</span></span>
<span data-ttu-id="e7eda-106">Командлет **Add-AzureRmMetricAlertRule** добавляет или обновляет правило оповещения на основе метрики.</span><span class="sxs-lookup"><span data-stu-id="e7eda-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="e7eda-107">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="e7eda-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="e7eda-108">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="e7eda-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e7eda-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7eda-109">EXAMPLES</span></span>

### <span data-ttu-id="e7eda-110">Пример 1: Добавление правила оповещения метрики на веб-сайт</span><span class="sxs-lookup"><span data-stu-id="e7eda-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="e7eda-111">Эта команда создает правило оповещения метрики для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="e7eda-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="e7eda-112">Пример 2: отключение правила</span><span class="sxs-lookup"><span data-stu-id="e7eda-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="e7eda-113">Эта команда отключает правило.</span><span class="sxs-lookup"><span data-stu-id="e7eda-113">This command disables a rule.</span></span>
<span data-ttu-id="e7eda-114">Если правило не существует, оно будет отключено.</span><span class="sxs-lookup"><span data-stu-id="e7eda-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="e7eda-115">Если правило существует, оно просто отключается.</span><span class="sxs-lookup"><span data-stu-id="e7eda-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="e7eda-116">Пример 3: Добавление правила с действиями</span><span class="sxs-lookup"><span data-stu-id="e7eda-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="e7eda-117">Эта команда создает правило оповещения метрики для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="e7eda-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="e7eda-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7eda-118">PARAMETERS</span></span>

### <span data-ttu-id="e7eda-119">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="e7eda-119">-Action</span></span>
<span data-ttu-id="e7eda-120">Указывает список действий, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="e7eda-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="e7eda-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7eda-121">-DefaultProfile</span></span>
<span data-ttu-id="e7eda-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e7eda-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7eda-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="e7eda-123">-Description</span></span>
<span data-ttu-id="e7eda-124">Задает описание правила.</span><span class="sxs-lookup"><span data-stu-id="e7eda-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="e7eda-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="e7eda-125">-DisableRule</span></span>
<span data-ttu-id="e7eda-126">Отключение правила.</span><span class="sxs-lookup"><span data-stu-id="e7eda-126">Disables the rule.</span></span>
<span data-ttu-id="e7eda-127">Если этот параметр не указан, правило разрешено.</span><span class="sxs-lookup"><span data-stu-id="e7eda-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="e7eda-128">-Location</span><span class="sxs-lookup"><span data-stu-id="e7eda-128">-Location</span></span>
<span data-ttu-id="e7eda-129">Указывает расположение, в котором определено правило.</span><span class="sxs-lookup"><span data-stu-id="e7eda-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="e7eda-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="e7eda-130">-MetricName</span></span>
<span data-ttu-id="e7eda-131">Указывает имя метрики, которое отслеживает правило.</span><span class="sxs-lookup"><span data-stu-id="e7eda-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="e7eda-132">Указывайте этот параметр только для правил на основе метрик.</span><span class="sxs-lookup"><span data-stu-id="e7eda-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="e7eda-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7eda-133">-Name</span></span>
<span data-ttu-id="e7eda-134">Задает имя правила.</span><span class="sxs-lookup"><span data-stu-id="e7eda-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="e7eda-135">-Operator</span><span class="sxs-lookup"><span data-stu-id="e7eda-135">-Operator</span></span>
<span data-ttu-id="e7eda-136">Указывает оператор отношения для условия правила.</span><span class="sxs-lookup"><span data-stu-id="e7eda-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="e7eda-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e7eda-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7eda-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="e7eda-138">GreaterThan</span></span>
- <span data-ttu-id="e7eda-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="e7eda-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="e7eda-140">LessThan</span><span class="sxs-lookup"><span data-stu-id="e7eda-140">LessThan</span></span>
- <span data-ttu-id="e7eda-141">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="e7eda-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="e7eda-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7eda-142">-ResourceGroupName</span></span>
<span data-ttu-id="e7eda-143">Указывает имя группы ресурсов для правила.</span><span class="sxs-lookup"><span data-stu-id="e7eda-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="e7eda-144">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e7eda-144">-TargetResourceId</span></span>
<span data-ttu-id="e7eda-145">Указывает идентификатор ресурса, отслеживаемого правилом.</span><span class="sxs-lookup"><span data-stu-id="e7eda-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="e7eda-146">Примечание. это свойство не может быть обновлено для существующего правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="e7eda-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="e7eda-147">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="e7eda-147">-Threshold</span></span>
<span data-ttu-id="e7eda-148">Указывает пороговое значение для правила.</span><span class="sxs-lookup"><span data-stu-id="e7eda-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="e7eda-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="e7eda-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="e7eda-150">Задает оператор агрегирования, который будет применяться к окну времени при вычислении правила.</span><span class="sxs-lookup"><span data-stu-id="e7eda-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="e7eda-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="e7eda-151">-WindowSize</span></span>
<span data-ttu-id="e7eda-152">Задает размер временного интервала для вычисления данных в правиле.</span><span class="sxs-lookup"><span data-stu-id="e7eda-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="e7eda-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7eda-153">-Confirm</span></span>
<span data-ttu-id="e7eda-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7eda-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7eda-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7eda-155">-WhatIf</span></span>
<span data-ttu-id="e7eda-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7eda-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7eda-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7eda-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7eda-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7eda-158">CommonParameters</span></span>
<span data-ttu-id="e7eda-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7eda-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7eda-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7eda-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7eda-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7eda-161">INPUTS</span></span>

### <span data-ttu-id="e7eda-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="e7eda-162">System.TimeSpan</span></span>

### <span data-ttu-id="e7eda-163">Microsoft. Azure. Management. Monitor. Management. Models. ConditionOperator</span><span class="sxs-lookup"><span data-stu-id="e7eda-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="e7eda-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="e7eda-164">System.Double</span></span>

### <span data-ttu-id="e7eda-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e7eda-165">System.String</span></span>

### <span data-ttu-id="e7eda-166">System. Nullable "1 [[Microsoft. Azure. Management. Monitor. Management. TimeAggregationOperator, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="e7eda-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e7eda-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7eda-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e7eda-168">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. RuleAction, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="e7eda-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e7eda-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7eda-169">OUTPUTS</span></span>

### <span data-ttu-id="e7eda-170">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e7eda-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="e7eda-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7eda-171">NOTES</span></span>

## <span data-ttu-id="e7eda-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7eda-172">RELATED LINKS</span></span>

[<span data-ttu-id="e7eda-173">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e7eda-173">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e7eda-174">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e7eda-174">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="e7eda-175">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e7eda-175">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="e7eda-176">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="e7eda-176">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="e7eda-177">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e7eda-177">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="e7eda-178">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e7eda-178">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="e7eda-179">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="e7eda-179">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


