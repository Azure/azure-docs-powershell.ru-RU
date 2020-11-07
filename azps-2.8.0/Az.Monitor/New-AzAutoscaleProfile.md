---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: b83f7429b326267304536318063b5245031db2c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902637"
---
# <span data-ttu-id="b32eb-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="b32eb-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="b32eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b32eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b32eb-103">Создание профиля автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="b32eb-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="b32eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b32eb-104">SYNTAX</span></span>

### <span data-ttu-id="b32eb-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="b32eb-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b32eb-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="b32eb-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b32eb-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="b32eb-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b32eb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b32eb-108">DESCRIPTION</span></span>
<span data-ttu-id="b32eb-109">Командлет **New-AzAutoscaleProfile** создает профиль автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="b32eb-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="b32eb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b32eb-110">EXAMPLES</span></span>

### <span data-ttu-id="b32eb-111">Пример 1: создание единого профиля с фиксированной датой</span><span class="sxs-lookup"><span data-stu-id="b32eb-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="b32eb-112">Первая команда создает правило автомасштабирования с именем запросы, а затем сохраняет его в переменной $Rule.</span><span class="sxs-lookup"><span data-stu-id="b32eb-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="b32eb-113">Вторая команда создает профиль с именем Profile01 с фиксированной датой, используя правило в $Rule.</span><span class="sxs-lookup"><span data-stu-id="b32eb-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="b32eb-114">Пример 2: Создание профиля с расписанием</span><span class="sxs-lookup"><span data-stu-id="b32eb-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="b32eb-115">Первая команда создает правило автомасштабирования с именем запросы, а затем сохраняет его в переменной $Rule.</span><span class="sxs-lookup"><span data-stu-id="b32eb-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="b32eb-116">Вторая команда создает профиль с именем SecondProfileName с расписанием повторения с помощью правила в $Rule.</span><span class="sxs-lookup"><span data-stu-id="b32eb-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="b32eb-117">Пример 3: создание профилей с двумя правилами</span><span class="sxs-lookup"><span data-stu-id="b32eb-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDay "1" -ScheduleHour 5 -ScheduleMinute 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="b32eb-118">Первые две команды создают правила и сохраняют их в переменных $Rule 1 и $Rule 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="b32eb-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="b32eb-119">Третья команда создает профиль с именем имя_профиля, используя правила в Rule1 и Rule2, а затем сохраняет его в переменной $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="b32eb-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="b32eb-120">Последняя команда создает профиль с именем SecondProfileName, используя правила в Rule1 и Rule2, а затем сохраняет его в переменной $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="b32eb-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="b32eb-121">Пример 4: Создание профиля без расписания или фиксированной даты</span><span class="sxs-lookup"><span data-stu-id="b32eb-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="b32eb-122">Первая команда создает правило автомасштабирования с именем запросы, а затем сохраняет его в переменной $Rule.</span><span class="sxs-lookup"><span data-stu-id="b32eb-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="b32eb-123">Вторая команда создает профиль без расписания или фиксированную дату, а затем сохраняет его в переменной $Profile.</span><span class="sxs-lookup"><span data-stu-id="b32eb-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="b32eb-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b32eb-124">PARAMETERS</span></span>

### <span data-ttu-id="b32eb-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="b32eb-125">-DefaultCapacity</span></span>
<span data-ttu-id="b32eb-126">Указывает емкость по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b32eb-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="b32eb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b32eb-127">-DefaultProfile</span></span>
<span data-ttu-id="b32eb-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b32eb-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b32eb-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="b32eb-129">-EndTimeWindow</span></span>
<span data-ttu-id="b32eb-130">Указывает конец временного интервала.</span><span class="sxs-lookup"><span data-stu-id="b32eb-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32eb-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="b32eb-131">-MaximumCapacity</span></span>
<span data-ttu-id="b32eb-132">Указывает максимальную емкость.</span><span class="sxs-lookup"><span data-stu-id="b32eb-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="b32eb-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="b32eb-133">-MinimumCapacity</span></span>
<span data-ttu-id="b32eb-134">Указывает минимальную емкость.</span><span class="sxs-lookup"><span data-stu-id="b32eb-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="b32eb-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b32eb-135">-Name</span></span>
<span data-ttu-id="b32eb-136">Указывает имя создаваемого профиля.</span><span class="sxs-lookup"><span data-stu-id="b32eb-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="b32eb-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="b32eb-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="b32eb-138">Указывает периодичность повторения.</span><span class="sxs-lookup"><span data-stu-id="b32eb-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="b32eb-139">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b32eb-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b32eb-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="b32eb-140">None</span></span>
- <span data-ttu-id="b32eb-141">2</span><span class="sxs-lookup"><span data-stu-id="b32eb-141">Second</span></span>
- <span data-ttu-id="b32eb-142">До</span><span class="sxs-lookup"><span data-stu-id="b32eb-142">Minute</span></span>
- <span data-ttu-id="b32eb-143">Часовой</span><span class="sxs-lookup"><span data-stu-id="b32eb-143">Hour</span></span>
- <span data-ttu-id="b32eb-144">Дневных</span><span class="sxs-lookup"><span data-stu-id="b32eb-144">Day</span></span>
- <span data-ttu-id="b32eb-145">Недели</span><span class="sxs-lookup"><span data-stu-id="b32eb-145">Week</span></span>
- <span data-ttu-id="b32eb-146">Перехода</span><span class="sxs-lookup"><span data-stu-id="b32eb-146">Month</span></span>
- <span data-ttu-id="b32eb-147">Year не все из этих значений поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b32eb-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32eb-148">-Правило</span><span class="sxs-lookup"><span data-stu-id="b32eb-148">-Rule</span></span>
<span data-ttu-id="b32eb-149">Указывает список правил, которые нужно добавить к профилю.</span><span class="sxs-lookup"><span data-stu-id="b32eb-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32eb-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="b32eb-150">-ScheduleDay</span></span>
<span data-ttu-id="b32eb-151">Задает запланированные дни.</span><span class="sxs-lookup"><span data-stu-id="b32eb-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32eb-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="b32eb-152">-ScheduleHour</span></span>
<span data-ttu-id="b32eb-153">Задает запланированные часы.</span><span class="sxs-lookup"><span data-stu-id="b32eb-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32eb-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="b32eb-154">-ScheduleMinute</span></span>
<span data-ttu-id="b32eb-155">Задает запланированные минуты.</span><span class="sxs-lookup"><span data-stu-id="b32eb-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32eb-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="b32eb-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="b32eb-157">Указывает часовой пояс расписания.</span><span class="sxs-lookup"><span data-stu-id="b32eb-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32eb-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="b32eb-158">-StartTimeWindow</span></span>
<span data-ttu-id="b32eb-159">Задает начало временного интервала.</span><span class="sxs-lookup"><span data-stu-id="b32eb-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32eb-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="b32eb-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="b32eb-161">Указывает часовой пояс для временного интервала.</span><span class="sxs-lookup"><span data-stu-id="b32eb-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b32eb-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b32eb-162">CommonParameters</span></span>
<span data-ttu-id="b32eb-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b32eb-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b32eb-164">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b32eb-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b32eb-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b32eb-165">INPUTS</span></span>

### <span data-ttu-id="b32eb-166">System. String</span><span class="sxs-lookup"><span data-stu-id="b32eb-166">System.String</span></span>

### <span data-ttu-id="b32eb-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="b32eb-167">System.DateTime</span></span>

### <span data-ttu-id="b32eb-168">Microsoft. Azure. Management. Monitor. Management. Models. RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="b32eb-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="b32eb-169">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b32eb-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b32eb-170">System. Collections. Generic. List `1[[System.Nullable` 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]], System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b32eb-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b32eb-171">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. ScaleRule; Microsoft. Azure. PowerShell. командлеты. Monitor, версия = 1.0.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="b32eb-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b32eb-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b32eb-172">OUTPUTS</span></span>

### <span data-ttu-id="b32eb-173">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="b32eb-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="b32eb-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="b32eb-174">NOTES</span></span>

## <span data-ttu-id="b32eb-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b32eb-175">RELATED LINKS</span></span>

[<span data-ttu-id="b32eb-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b32eb-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="b32eb-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="b32eb-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="b32eb-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b32eb-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="b32eb-179">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="b32eb-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="b32eb-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b32eb-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


