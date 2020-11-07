---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 575c6e5b210ca47e1904c5174f97b5886b0428b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733277"
---
# <span data-ttu-id="2dee9-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="2dee9-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="2dee9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2dee9-102">SYNOPSIS</span></span>
<span data-ttu-id="2dee9-103">Создает правило автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="2dee9-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dee9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dee9-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dee9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dee9-105">DESCRIPTION</span></span>
<span data-ttu-id="2dee9-106">Командлет **New-AzureRmAutoscaleRule** создает правило автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="2dee9-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="2dee9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2dee9-107">EXAMPLES</span></span>

### <span data-ttu-id="2dee9-108">Пример 1: Создание правила</span><span class="sxs-lookup"><span data-stu-id="2dee9-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="2dee9-109">Эта команда создает правило.</span><span class="sxs-lookup"><span data-stu-id="2dee9-109">This command creates a rule.</span></span>

### <span data-ttu-id="2dee9-110">Пример 2: создание двух правил</span><span class="sxs-lookup"><span data-stu-id="2dee9-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="2dee9-111">Первая команда создает правило для метрики запросов, а затем сохраняет его в переменной $Rule 1.</span><span class="sxs-lookup"><span data-stu-id="2dee9-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="2dee9-112">Вторая команда создает второе правило для метрики запросов, а затем сохраняет его в переменной $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="2dee9-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="2dee9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2dee9-113">PARAMETERS</span></span>

### <span data-ttu-id="2dee9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dee9-114">-DefaultProfile</span></span>
<span data-ttu-id="2dee9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2dee9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="2dee9-116">-MetricName</span></span>
<span data-ttu-id="2dee9-117">Указывает имя метрики.</span><span class="sxs-lookup"><span data-stu-id="2dee9-117">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-118">-MetricResourceId</span><span class="sxs-lookup"><span data-stu-id="2dee9-118">-MetricResourceId</span></span>
<span data-ttu-id="2dee9-119">Указывает идентификатор ресурса метрики.</span><span class="sxs-lookup"><span data-stu-id="2dee9-119">Specifies the metric resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-120">-MetricStatistic</span><span class="sxs-lookup"><span data-stu-id="2dee9-120">-MetricStatistic</span></span>
<span data-ttu-id="2dee9-121">Указывает статистику метрики.</span><span class="sxs-lookup"><span data-stu-id="2dee9-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="2dee9-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2dee9-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2dee9-123">Среднем</span><span class="sxs-lookup"><span data-stu-id="2dee9-123">Average</span></span>
- <span data-ttu-id="2dee9-124">Наименьш</span><span class="sxs-lookup"><span data-stu-id="2dee9-124">Min</span></span>
- <span data-ttu-id="2dee9-125">Развертывания</span><span class="sxs-lookup"><span data-stu-id="2dee9-125">Max</span></span>
- <span data-ttu-id="2dee9-126">Сумма</span><span class="sxs-lookup"><span data-stu-id="2dee9-126">Sum</span></span>

```yaml
Type: MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-127">-Operator</span><span class="sxs-lookup"><span data-stu-id="2dee9-127">-Operator</span></span>
<span data-ttu-id="2dee9-128">Указывает оператор.</span><span class="sxs-lookup"><span data-stu-id="2dee9-128">Specifies the operator.</span></span>
<span data-ttu-id="2dee9-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2dee9-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2dee9-130">Соответствует</span><span class="sxs-lookup"><span data-stu-id="2dee9-130">Equals</span></span>
- <span data-ttu-id="2dee9-131">NotEquals</span><span class="sxs-lookup"><span data-stu-id="2dee9-131">NotEquals</span></span>
- <span data-ttu-id="2dee9-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="2dee9-132">GreaterThan</span></span>
- <span data-ttu-id="2dee9-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="2dee9-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="2dee9-134">LessThan</span><span class="sxs-lookup"><span data-stu-id="2dee9-134">LessThan</span></span>
- <span data-ttu-id="2dee9-135">LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="2dee9-135">LessThanOrEqual</span></span>

```yaml
Type: ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-136">-ScaleActionCooldown</span><span class="sxs-lookup"><span data-stu-id="2dee9-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="2dee9-137">Задает время cooldown действия автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="2dee9-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="2dee9-138">-ScaleActionDirection</span></span>
<span data-ttu-id="2dee9-139">Задает направление действия масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2dee9-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="2dee9-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2dee9-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2dee9-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="2dee9-141">None</span></span>
- <span data-ttu-id="2dee9-142">Освободит</span><span class="sxs-lookup"><span data-stu-id="2dee9-142">Increase</span></span>
- <span data-ttu-id="2dee9-143">Уменьшить</span><span class="sxs-lookup"><span data-stu-id="2dee9-143">Decrease</span></span>

```yaml
Type: ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="2dee9-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="2dee9-145">Указывает тип шкалы.</span><span class="sxs-lookup"><span data-stu-id="2dee9-145">Specifies the scale type.</span></span>
<span data-ttu-id="2dee9-146">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2dee9-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2dee9-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="2dee9-147">ChangeSize</span></span>
- <span data-ttu-id="2dee9-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="2dee9-148">ChangeCount</span></span>
- <span data-ttu-id="2dee9-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="2dee9-149">PercentChangeCount</span></span>
- <span data-ttu-id="2dee9-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="2dee9-150">ExactCount</span></span>

```yaml
Type: ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="2dee9-151">-ScaleActionValue</span></span>
<span data-ttu-id="2dee9-152">Задает значение действия.</span><span class="sxs-lookup"><span data-stu-id="2dee9-152">Specifies the action value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-153">— Threshold (порог)</span><span class="sxs-lookup"><span data-stu-id="2dee9-153">-Threshold</span></span>
<span data-ttu-id="2dee9-154">Указывает порог значения метрики.</span><span class="sxs-lookup"><span data-stu-id="2dee9-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="2dee9-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="2dee9-156">Указывает оператор агрегата времени.</span><span class="sxs-lookup"><span data-stu-id="2dee9-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="2dee9-157">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2dee9-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2dee9-158">Среднем</span><span class="sxs-lookup"><span data-stu-id="2dee9-158">Average</span></span>
- <span data-ttu-id="2dee9-159">Минимум</span><span class="sxs-lookup"><span data-stu-id="2dee9-159">Minimum</span></span>
- <span data-ttu-id="2dee9-160">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dee9-160">Maximum</span></span>
- <span data-ttu-id="2dee9-161">Времени</span><span class="sxs-lookup"><span data-stu-id="2dee9-161">Last</span></span>
- <span data-ttu-id="2dee9-162">Итого, количество</span><span class="sxs-lookup"><span data-stu-id="2dee9-162">Total, Count</span></span>

```yaml
Type: TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-163">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="2dee9-163">-TimeGrain</span></span>
<span data-ttu-id="2dee9-164">Указывает промежуток времени.</span><span class="sxs-lookup"><span data-stu-id="2dee9-164">Specifies the time grain.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="2dee9-165">-TimeWindow</span></span>
<span data-ttu-id="2dee9-166">Указывает окно времени.</span><span class="sxs-lookup"><span data-stu-id="2dee9-166">Specifies the time window.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dee9-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dee9-167">CommonParameters</span></span>
<span data-ttu-id="2dee9-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2dee9-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dee9-169">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dee9-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dee9-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2dee9-170">INPUTS</span></span>

### <span data-ttu-id="2dee9-171">Ничего</span><span class="sxs-lookup"><span data-stu-id="2dee9-171">None</span></span>
<span data-ttu-id="2dee9-172">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2dee9-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2dee9-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dee9-173">OUTPUTS</span></span>

### <span data-ttu-id="2dee9-174">Microsoft. Azure. Management. Monitor. Management. Models. ScaleRule</span><span class="sxs-lookup"><span data-stu-id="2dee9-174">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="2dee9-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="2dee9-175">NOTES</span></span>

## <span data-ttu-id="2dee9-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dee9-176">RELATED LINKS</span></span>

[<span data-ttu-id="2dee9-177">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dee9-177">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="2dee9-178">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="2dee9-178">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="2dee9-179">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dee9-179">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="2dee9-180">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="2dee9-180">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="2dee9-181">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="2dee9-181">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


