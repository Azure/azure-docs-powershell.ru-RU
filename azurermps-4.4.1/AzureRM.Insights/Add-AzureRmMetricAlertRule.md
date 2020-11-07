---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734831"
---
# <span data-ttu-id="43d2d-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="43d2d-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="43d2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="43d2d-103">Добавляет или обновляет правило оповещения на основе метрики.</span><span class="sxs-lookup"><span data-stu-id="43d2d-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43d2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43d2d-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43d2d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43d2d-105">DESCRIPTION</span></span>
<span data-ttu-id="43d2d-106">Командлет **Add-AzureRmMetricAlertRule** добавляет или обновляет правило оповещения на основе метрики.</span><span class="sxs-lookup"><span data-stu-id="43d2d-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="43d2d-107">Добавленное правило связано с группой ресурсов и имеет имя.</span><span class="sxs-lookup"><span data-stu-id="43d2d-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="43d2d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43d2d-108">EXAMPLES</span></span>

### <span data-ttu-id="43d2d-109">Пример 1: Добавление правила оповещения метрики на веб-сайт</span><span class="sxs-lookup"><span data-stu-id="43d2d-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="43d2d-110">Эта команда создает правило оповещения метрики для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="43d2d-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="43d2d-111">Пример 2: отключение правила</span><span class="sxs-lookup"><span data-stu-id="43d2d-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="43d2d-112">Эта команда отключает правило.</span><span class="sxs-lookup"><span data-stu-id="43d2d-112">This command disables a rule.</span></span>
<span data-ttu-id="43d2d-113">Если правило не существует, оно будет отключено.</span><span class="sxs-lookup"><span data-stu-id="43d2d-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="43d2d-114">Если правило существует, оно просто отключается.</span><span class="sxs-lookup"><span data-stu-id="43d2d-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="43d2d-115">Пример 3: Добавление правила с действиями</span><span class="sxs-lookup"><span data-stu-id="43d2d-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="43d2d-116">Эта команда создает правило оповещения метрики для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="43d2d-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="43d2d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43d2d-117">PARAMETERS</span></span>

### <span data-ttu-id="43d2d-118">-Actions (действия)</span><span class="sxs-lookup"><span data-stu-id="43d2d-118">-Actions</span></span>
<span data-ttu-id="43d2d-119">Указывает список действий, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="43d2d-119">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="43d2d-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="43d2d-120">-Description</span></span>
<span data-ttu-id="43d2d-121">Задает описание правила.</span><span class="sxs-lookup"><span data-stu-id="43d2d-121">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="43d2d-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="43d2d-122">-DisableRule</span></span>
<span data-ttu-id="43d2d-123">Отключение правила.</span><span class="sxs-lookup"><span data-stu-id="43d2d-123">Disables the rule.</span></span>
<span data-ttu-id="43d2d-124">Если этот параметр не указан, правило разрешено.</span><span class="sxs-lookup"><span data-stu-id="43d2d-124">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="43d2d-125">-Location</span><span class="sxs-lookup"><span data-stu-id="43d2d-125">-Location</span></span>
<span data-ttu-id="43d2d-126">Указывает расположение, в котором определено правило.</span><span class="sxs-lookup"><span data-stu-id="43d2d-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="43d2d-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="43d2d-127">-MetricName</span></span>
<span data-ttu-id="43d2d-128">Указывает имя метрики, которое отслеживает правило.</span><span class="sxs-lookup"><span data-stu-id="43d2d-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="43d2d-129">Указывайте этот параметр только для правил на основе метрик.</span><span class="sxs-lookup"><span data-stu-id="43d2d-129">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="43d2d-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43d2d-130">-Name</span></span>
<span data-ttu-id="43d2d-131">Задает имя правила.</span><span class="sxs-lookup"><span data-stu-id="43d2d-131">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="43d2d-132">-Operator</span><span class="sxs-lookup"><span data-stu-id="43d2d-132">-Operator</span></span>
<span data-ttu-id="43d2d-133">Указывает оператор отношения для условия правила.</span><span class="sxs-lookup"><span data-stu-id="43d2d-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="43d2d-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43d2d-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43d2d-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="43d2d-135">GreaterThan</span></span>
- <span data-ttu-id="43d2d-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="43d2d-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="43d2d-137">LessThan</span><span class="sxs-lookup"><span data-stu-id="43d2d-137">LessThan</span></span>
- <span data-ttu-id="43d2d-138">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="43d2d-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="43d2d-139">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43d2d-139">-ResourceGroup</span></span>
<span data-ttu-id="43d2d-140">Указывает имя группы ресурсов для правила.</span><span class="sxs-lookup"><span data-stu-id="43d2d-140">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="43d2d-141">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="43d2d-141">-TargetResourceId</span></span>
<span data-ttu-id="43d2d-142">Указывает идентификатор ресурса, отслеживаемого правилом.</span><span class="sxs-lookup"><span data-stu-id="43d2d-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="43d2d-143">Примечание. это свойство не может быть обновлено для существующего правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="43d2d-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="43d2d-144">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="43d2d-144">-Threshold</span></span>
<span data-ttu-id="43d2d-145">Указывает пороговое значение для правила.</span><span class="sxs-lookup"><span data-stu-id="43d2d-145">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="43d2d-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="43d2d-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="43d2d-147">Задает оператор агрегирования, который будет применяться к окну времени при вычислении правила.</span><span class="sxs-lookup"><span data-stu-id="43d2d-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="43d2d-148">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="43d2d-148">-WindowSize</span></span>
<span data-ttu-id="43d2d-149">Задает размер временного интервала для вычисления данных в правиле.</span><span class="sxs-lookup"><span data-stu-id="43d2d-149">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="43d2d-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d2d-150">-DefaultProfile</span></span>
<span data-ttu-id="43d2d-151">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43d2d-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43d2d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d2d-152">CommonParameters</span></span>
<span data-ttu-id="43d2d-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43d2d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d2d-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43d2d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d2d-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43d2d-155">INPUTS</span></span>

## <span data-ttu-id="43d2d-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43d2d-156">OUTPUTS</span></span>

### <span data-ttu-id="43d2d-157">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="43d2d-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="43d2d-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="43d2d-158">NOTES</span></span>

## <span data-ttu-id="43d2d-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43d2d-159">RELATED LINKS</span></span>

[<span data-ttu-id="43d2d-160">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="43d2d-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="43d2d-161">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="43d2d-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="43d2d-162">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="43d2d-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="43d2d-163">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="43d2d-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="43d2d-164">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="43d2d-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="43d2d-165">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="43d2d-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="43d2d-166">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="43d2d-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


