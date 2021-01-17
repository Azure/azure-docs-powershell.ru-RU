---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: f857f578ab3f0b8baacd0c5d392659ac09b0790f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419804"
---
# <span data-ttu-id="10a25-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="10a25-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="10a25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a25-102">SYNOPSIS</span></span>
<span data-ttu-id="10a25-103">Создает профиль автомасштаби.</span><span class="sxs-lookup"><span data-stu-id="10a25-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="10a25-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10a25-104">SYNTAX</span></span>

### <span data-ttu-id="10a25-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="10a25-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10a25-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="10a25-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10a25-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="10a25-107">CreateUsingRecurrentScheduling</span></span>
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

## <span data-ttu-id="10a25-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10a25-108">DESCRIPTION</span></span>
<span data-ttu-id="10a25-109">Для создания профиля автомасштаби создается новый профиль **AzAutoscaleProfile.**</span><span class="sxs-lookup"><span data-stu-id="10a25-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="10a25-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10a25-110">EXAMPLES</span></span>

### <span data-ttu-id="10a25-111">Пример 1. Создание отдельного профиля с фиксированной датой</span><span class="sxs-lookup"><span data-stu-id="10a25-111">Example 1: Create single profile with a fixed date</span></span>
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

<span data-ttu-id="10a25-112">Первая команда создает правило авто шкалы с именем "Запросы", а затем сохраняет его в $Rule переменной.</span><span class="sxs-lookup"><span data-stu-id="10a25-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="10a25-113">Вторая команда создает профиль с именем Profile01 с фиксированной датой с помощью правила в $Rule.</span><span class="sxs-lookup"><span data-stu-id="10a25-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="10a25-114">Пример 2. Создание профиля с расписанием</span><span class="sxs-lookup"><span data-stu-id="10a25-114">Example 2: Create a profile with a schedule</span></span>
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

<span data-ttu-id="10a25-115">Первая команда создает правило авто шкалы с именем "Запросы", а затем сохраняет его в $Rule переменной.</span><span class="sxs-lookup"><span data-stu-id="10a25-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="10a25-116">Вторая команда создает профиль с именем SecondProfileName с повторяющимся расписанием, используя правило в $Rule.</span><span class="sxs-lookup"><span data-stu-id="10a25-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="10a25-117">Пример 3. Создание профилей с двумя правилами</span><span class="sxs-lookup"><span data-stu-id="10a25-117">Example 3: Create profiles with two rules</span></span>
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

<span data-ttu-id="10a25-118">Первые две команды создают правила и сохраняют их в переменных $Rule 1 и $Rule 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="10a25-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="10a25-119">Третья команда создает профиль "Имя Профиля" с помощью правил в правилах "Правило1" и "Правило2", а затем сохраняет его в переменной $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="10a25-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="10a25-120">Конечная команда создает профиль SecondProfileName с использованием правил в "Правило1" и "Правило2", а затем сохраняет его в переменной $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="10a25-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="10a25-121">Пример 4. Создание профиля без расписания и фиксированной даты</span><span class="sxs-lookup"><span data-stu-id="10a25-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="10a25-122">Первая команда создает правило авто шкалы с именем "Запросы", а затем сохраняет его в $Rule переменной.</span><span class="sxs-lookup"><span data-stu-id="10a25-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="10a25-123">Вторая команда создает профиль без расписания или фиксированной даты, а затем сохраняет его в переменной $Profile.</span><span class="sxs-lookup"><span data-stu-id="10a25-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="10a25-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10a25-124">PARAMETERS</span></span>

### <span data-ttu-id="10a25-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="10a25-125">-DefaultCapacity</span></span>
<span data-ttu-id="10a25-126">Указывает стандартную емкость.</span><span class="sxs-lookup"><span data-stu-id="10a25-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="10a25-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a25-127">-DefaultProfile</span></span>
<span data-ttu-id="10a25-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="10a25-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10a25-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="10a25-129">-EndTimeWindow</span></span>
<span data-ttu-id="10a25-130">Определяет конец окне.</span><span class="sxs-lookup"><span data-stu-id="10a25-130">Specifies the end of the time window.</span></span>

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

### <span data-ttu-id="10a25-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="10a25-131">-MaximumCapacity</span></span>
<span data-ttu-id="10a25-132">Указывает максимальную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="10a25-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="10a25-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="10a25-133">-MinimumCapacity</span></span>
<span data-ttu-id="10a25-134">Минимальная пропускная способность.</span><span class="sxs-lookup"><span data-stu-id="10a25-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="10a25-135">-Name</span><span class="sxs-lookup"><span data-stu-id="10a25-135">-Name</span></span>
<span data-ttu-id="10a25-136">Указывает имя созда создаемого профиля.</span><span class="sxs-lookup"><span data-stu-id="10a25-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="10a25-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="10a25-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="10a25-138">Определяет частоту повторения.</span><span class="sxs-lookup"><span data-stu-id="10a25-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="10a25-139">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="10a25-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="10a25-140">Нет</span><span class="sxs-lookup"><span data-stu-id="10a25-140">None</span></span>
- <span data-ttu-id="10a25-141">Second</span><span class="sxs-lookup"><span data-stu-id="10a25-141">Second</span></span>
- <span data-ttu-id="10a25-142">Минуты</span><span class="sxs-lookup"><span data-stu-id="10a25-142">Minute</span></span>
- <span data-ttu-id="10a25-143">Часы</span><span class="sxs-lookup"><span data-stu-id="10a25-143">Hour</span></span>
- <span data-ttu-id="10a25-144">День</span><span class="sxs-lookup"><span data-stu-id="10a25-144">Day</span></span>
- <span data-ttu-id="10a25-145">Неделя</span><span class="sxs-lookup"><span data-stu-id="10a25-145">Week</span></span>
- <span data-ttu-id="10a25-146">Месяц</span><span class="sxs-lookup"><span data-stu-id="10a25-146">Month</span></span>
- <span data-ttu-id="10a25-147">Поддерживаются не все из этих значений.</span><span class="sxs-lookup"><span data-stu-id="10a25-147">Year Not all of these values are supported.</span></span>

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

### <span data-ttu-id="10a25-148">-Правило</span><span class="sxs-lookup"><span data-stu-id="10a25-148">-Rule</span></span>
<span data-ttu-id="10a25-149">Список правил, которые нужно добавить в профиль.</span><span class="sxs-lookup"><span data-stu-id="10a25-149">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="10a25-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="10a25-150">-ScheduleDay</span></span>
<span data-ttu-id="10a25-151">Определяет запланированные дни.</span><span class="sxs-lookup"><span data-stu-id="10a25-151">Specifies the scheduled days.</span></span>

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

### <span data-ttu-id="10a25-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="10a25-152">-ScheduleHour</span></span>
<span data-ttu-id="10a25-153">Определяет запланированные часы.</span><span class="sxs-lookup"><span data-stu-id="10a25-153">Specifies the scheduled hours.</span></span>

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

### <span data-ttu-id="10a25-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="10a25-154">-ScheduleMinute</span></span>
<span data-ttu-id="10a25-155">Определяет запланированные минуты.</span><span class="sxs-lookup"><span data-stu-id="10a25-155">Specifies the scheduled minutes.</span></span>

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

### <span data-ttu-id="10a25-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="10a25-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="10a25-157">Определяет часовой пояс расписания.</span><span class="sxs-lookup"><span data-stu-id="10a25-157">Specifies the time zone of the schedule.</span></span>

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

### <span data-ttu-id="10a25-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="10a25-158">-StartTimeWindow</span></span>
<span data-ttu-id="10a25-159">Указывает начало окне.</span><span class="sxs-lookup"><span data-stu-id="10a25-159">Specifies the start of the time window.</span></span>

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

### <span data-ttu-id="10a25-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="10a25-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="10a25-161">Определяет часовой пояс в часовом окне.</span><span class="sxs-lookup"><span data-stu-id="10a25-161">Specifies the time zone of the time window.</span></span>

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

### <span data-ttu-id="10a25-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a25-162">CommonParameters</span></span>
<span data-ttu-id="10a25-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a25-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a25-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10a25-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a25-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10a25-165">INPUTS</span></span>

### <span data-ttu-id="10a25-166">System.String</span><span class="sxs-lookup"><span data-stu-id="10a25-166">System.String</span></span>

### <span data-ttu-id="10a25-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="10a25-167">System.DateTime</span></span>

### <span data-ttu-id="10a25-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="10a25-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="10a25-169">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10a25-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="10a25-170">System.Collections.Generic.List `1[[System.Nullable` 1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10a25-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="10a25-171">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="10a25-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="10a25-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10a25-172">OUTPUTS</span></span>

### <span data-ttu-id="10a25-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="10a25-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="10a25-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10a25-174">NOTES</span></span>

## <span data-ttu-id="10a25-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10a25-175">RELATED LINKS</span></span>

[<span data-ttu-id="10a25-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="10a25-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="10a25-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="10a25-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="10a25-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="10a25-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="10a25-179">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="10a25-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="10a25-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="10a25-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


