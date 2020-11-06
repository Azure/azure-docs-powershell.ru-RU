---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: 44273f05793e8f84b28e6dc68f8cc12633fadf0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561800"
---
# <span data-ttu-id="dbd24-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="dbd24-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="dbd24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dbd24-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd24-103">Создание профиля автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="dbd24-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbd24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dbd24-104">SYNTAX</span></span>

### <span data-ttu-id="dbd24-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="dbd24-105">CreateWithoutScheduledTimes</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String> -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbd24-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="dbd24-106">CreateWithFixedDateScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbd24-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="dbd24-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbd24-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbd24-108">DESCRIPTION</span></span>
<span data-ttu-id="dbd24-109">Командлет **New-AzureRmAutoscaleProfile** создает профиль автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="dbd24-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="dbd24-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dbd24-110">EXAMPLES</span></span>

### <span data-ttu-id="dbd24-111">Пример 1: создание единого профиля с фиксированной датой</span><span class="sxs-lookup"><span data-stu-id="dbd24-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="dbd24-112">Первая команда создает правило автомасштабирования с именем запросы, а затем сохраняет его в переменной $Rule.</span><span class="sxs-lookup"><span data-stu-id="dbd24-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="dbd24-113">Вторая команда создает профиль с именем Profile01 с фиксированной датой, используя правило в $Rule.</span><span class="sxs-lookup"><span data-stu-id="dbd24-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="dbd24-114">Пример 2: Создание профиля с расписанием</span><span class="sxs-lookup"><span data-stu-id="dbd24-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="dbd24-115">Первая команда создает правило автомасштабирования с именем запросы, а затем сохраняет его в переменной $Rule.</span><span class="sxs-lookup"><span data-stu-id="dbd24-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="dbd24-116">Вторая команда создает профиль с именем SecondProfileName с расписанием повторения с помощью правила в $Rule.</span><span class="sxs-lookup"><span data-stu-id="dbd24-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="dbd24-117">Пример 3: создание профилей с двумя правилами</span><span class="sxs-lookup"><span data-stu-id="dbd24-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="dbd24-118">Первые две команды создают правила и сохраняют их в переменных $Rule 1 и $Rule 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="dbd24-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="dbd24-119">Третья команда создает профиль с именем имя_профиля, используя правила в Rule1 и Rule2, а затем сохраняет его в переменной $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="dbd24-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="dbd24-120">Последняя команда создает профиль с именем SecondProfileName, используя правила в Rule1 и Rule2, а затем сохраняет его в переменной $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="dbd24-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="dbd24-121">Пример 4: Создание профиля без расписания или фиксированной даты</span><span class="sxs-lookup"><span data-stu-id="dbd24-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="dbd24-122">Первая команда создает правило автомасштабирования с именем запросы, а затем сохраняет его в переменной $Rule.</span><span class="sxs-lookup"><span data-stu-id="dbd24-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="dbd24-123">Вторая команда создает профиль без расписания или фиксированную дату, а затем сохраняет его в переменной $Profile.</span><span class="sxs-lookup"><span data-stu-id="dbd24-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="dbd24-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dbd24-124">PARAMETERS</span></span>

### <span data-ttu-id="dbd24-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="dbd24-125">-DefaultCapacity</span></span>
<span data-ttu-id="dbd24-126">Указывает емкость по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dbd24-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="dbd24-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd24-127">-DefaultProfile</span></span>
<span data-ttu-id="dbd24-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dbd24-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbd24-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="dbd24-129">-EndTimeWindow</span></span>
<span data-ttu-id="dbd24-130">Указывает конец временного интервала.</span><span class="sxs-lookup"><span data-stu-id="dbd24-130">Specifies the end of the time window.</span></span>

```yaml
Type: DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd24-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="dbd24-131">-MaximumCapacity</span></span>
<span data-ttu-id="dbd24-132">Указывает максимальную емкость.</span><span class="sxs-lookup"><span data-stu-id="dbd24-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="dbd24-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="dbd24-133">-MinimumCapacity</span></span>
<span data-ttu-id="dbd24-134">Указывает минимальную емкость.</span><span class="sxs-lookup"><span data-stu-id="dbd24-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="dbd24-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dbd24-135">-Name</span></span>
<span data-ttu-id="dbd24-136">Указывает имя создаваемого профиля.</span><span class="sxs-lookup"><span data-stu-id="dbd24-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="dbd24-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="dbd24-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="dbd24-138">Указывает периодичность повторения.</span><span class="sxs-lookup"><span data-stu-id="dbd24-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="dbd24-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="dbd24-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dbd24-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="dbd24-140">None</span></span>
- <span data-ttu-id="dbd24-141">2</span><span class="sxs-lookup"><span data-stu-id="dbd24-141">Second</span></span>
- <span data-ttu-id="dbd24-142">До</span><span class="sxs-lookup"><span data-stu-id="dbd24-142">Minute</span></span>
- <span data-ttu-id="dbd24-143">Часовой</span><span class="sxs-lookup"><span data-stu-id="dbd24-143">Hour</span></span>
- <span data-ttu-id="dbd24-144">Дневных</span><span class="sxs-lookup"><span data-stu-id="dbd24-144">Day</span></span>
- <span data-ttu-id="dbd24-145">Недели</span><span class="sxs-lookup"><span data-stu-id="dbd24-145">Week</span></span>
- <span data-ttu-id="dbd24-146">Перехода</span><span class="sxs-lookup"><span data-stu-id="dbd24-146">Month</span></span>
- <span data-ttu-id="dbd24-147">Year</span><span class="sxs-lookup"><span data-stu-id="dbd24-147">Year</span></span>

<span data-ttu-id="dbd24-148">Поддерживаются не все из этих значений.</span><span class="sxs-lookup"><span data-stu-id="dbd24-148">Not all of these values are supported.</span></span>

```yaml
Type: RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd24-149">-Правило</span><span class="sxs-lookup"><span data-stu-id="dbd24-149">-Rule</span></span>
<span data-ttu-id="dbd24-150">Указывает список правил, которые нужно добавить к профилю.</span><span class="sxs-lookup"><span data-stu-id="dbd24-150">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases: Rules

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd24-151">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="dbd24-151">-ScheduleDay</span></span>
<span data-ttu-id="dbd24-152">Задает запланированные дни.</span><span class="sxs-lookup"><span data-stu-id="dbd24-152">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleDays

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd24-153">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="dbd24-153">-ScheduleHour</span></span>
<span data-ttu-id="dbd24-154">Задает запланированные часы.</span><span class="sxs-lookup"><span data-stu-id="dbd24-154">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleHours

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd24-155">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="dbd24-155">-ScheduleMinute</span></span>
<span data-ttu-id="dbd24-156">Задает запланированные минуты.</span><span class="sxs-lookup"><span data-stu-id="dbd24-156">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleMinutes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd24-157">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="dbd24-157">-ScheduleTimeZone</span></span>
<span data-ttu-id="dbd24-158">Указывает часовой пояс расписания.</span><span class="sxs-lookup"><span data-stu-id="dbd24-158">Specifies the time zone of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd24-159">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="dbd24-159">-StartTimeWindow</span></span>
<span data-ttu-id="dbd24-160">Задает начало временного интервала.</span><span class="sxs-lookup"><span data-stu-id="dbd24-160">Specifies the start of the time window.</span></span>

```yaml
Type: DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd24-161">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="dbd24-161">-TimeWindowTimeZone</span></span>
<span data-ttu-id="dbd24-162">Указывает часовой пояс для временного интервала.</span><span class="sxs-lookup"><span data-stu-id="dbd24-162">Specifies the time zone of the time window.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbd24-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd24-163">CommonParameters</span></span>
<span data-ttu-id="dbd24-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dbd24-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd24-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd24-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd24-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dbd24-166">INPUTS</span></span>

### <span data-ttu-id="dbd24-167">Ничего</span><span class="sxs-lookup"><span data-stu-id="dbd24-167">None</span></span>
<span data-ttu-id="dbd24-168">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="dbd24-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dbd24-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbd24-169">OUTPUTS</span></span>

### <span data-ttu-id="dbd24-170">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="dbd24-170">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="dbd24-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="dbd24-171">NOTES</span></span>

## <span data-ttu-id="dbd24-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbd24-172">RELATED LINKS</span></span>

[<span data-ttu-id="dbd24-173">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="dbd24-173">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="dbd24-174">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="dbd24-174">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="dbd24-175">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="dbd24-175">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="dbd24-176">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="dbd24-176">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="dbd24-177">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="dbd24-177">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


