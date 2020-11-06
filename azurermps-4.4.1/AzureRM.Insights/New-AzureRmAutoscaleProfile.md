---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: a5cea42544f2f24ad6c1f1cc1ce64bf122e53440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568780"
---
# <span data-ttu-id="78c84-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="78c84-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="78c84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78c84-102">SYNOPSIS</span></span>
<span data-ttu-id="78c84-103">Создание профиля автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="78c84-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78c84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78c84-104">SYNTAX</span></span>

### <span data-ttu-id="78c84-105">Параметры для New-AzureRmAutoscaleProfile командлета без запланированного времени</span><span class="sxs-lookup"><span data-stu-id="78c84-105">Parameters for New-AzureRmAutoscaleProfile cmdlet without scheduled times</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78c84-106">Параметры командлета New-AzureRmAutoscaleProfile с использованием расписания Fix Date</span><span class="sxs-lookup"><span data-stu-id="78c84-106">Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78c84-107">Параметры для New-AzureRmAutoscaleProfile командлета с помощью повторного планирования</span><span class="sxs-lookup"><span data-stu-id="78c84-107">Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDays <System.Collections.Generic.List`1[System.String]>
 -ScheduleHours <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinutes <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78c84-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78c84-108">DESCRIPTION</span></span>
<span data-ttu-id="78c84-109">Командлет **New-AzureRmAutoscaleProfile** создает профиль автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="78c84-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="78c84-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78c84-110">EXAMPLES</span></span>

### <span data-ttu-id="78c84-111">Пример 1: создание единого профиля с фиксированной датой</span><span class="sxs-lookup"><span data-stu-id="78c84-111">Example 1: Create single profile with a fixed date</span></span>
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

<span data-ttu-id="78c84-112">Первая команда создает правило автомасштабирования с именем запросы, а затем сохраняет его в переменной $Rule.</span><span class="sxs-lookup"><span data-stu-id="78c84-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="78c84-113">Вторая команда создает профиль с именем Profile01 с фиксированной датой, используя правило в $Rule.</span><span class="sxs-lookup"><span data-stu-id="78c84-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="78c84-114">Пример 2: Создание профиля с расписанием</span><span class="sxs-lookup"><span data-stu-id="78c84-114">Example 2: Create a profile with a schedule</span></span>
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

<span data-ttu-id="78c84-115">Первая команда создает правило автомасштабирования с именем запросы, а затем сохраняет его в переменной $Rule.</span><span class="sxs-lookup"><span data-stu-id="78c84-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="78c84-116">Вторая команда создает профиль с именем SecondProfileName с расписанием повторения с помощью правила в $Rule.</span><span class="sxs-lookup"><span data-stu-id="78c84-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="78c84-117">Пример 3: создание профилей с двумя правилами</span><span class="sxs-lookup"><span data-stu-id="78c84-117">Example 3: Create profiles with two rules</span></span>
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

<span data-ttu-id="78c84-118">Первые две команды создают правила и сохраняют их в переменных $Rule 1 и $Rule 2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="78c84-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="78c84-119">Третья команда создает профиль с именем имя_профиля, используя правила в Rule1 и Rule2, а затем сохраняет его в переменной $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="78c84-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="78c84-120">Последняя команда создает профиль с именем SecondProfileName, используя правила в Rule1 и Rule2, а затем сохраняет его в переменной $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="78c84-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="78c84-121">Пример 4: Создание профиля без расписания или фиксированной даты</span><span class="sxs-lookup"><span data-stu-id="78c84-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="78c84-122">Первая команда создает правило автомасштабирования с именем запросы, а затем сохраняет его в переменной $Rule.</span><span class="sxs-lookup"><span data-stu-id="78c84-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="78c84-123">Вторая команда создает профиль без расписания или фиксированную дату, а затем сохраняет его в переменной $Profile.</span><span class="sxs-lookup"><span data-stu-id="78c84-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="78c84-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78c84-124">PARAMETERS</span></span>

### <span data-ttu-id="78c84-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="78c84-125">-DefaultCapacity</span></span>
<span data-ttu-id="78c84-126">Указывает емкость по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="78c84-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="78c84-127">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="78c84-127">-EndTimeWindow</span></span>
<span data-ttu-id="78c84-128">Указывает конец временного интервала.</span><span class="sxs-lookup"><span data-stu-id="78c84-128">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c84-129">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="78c84-129">-MaximumCapacity</span></span>
<span data-ttu-id="78c84-130">Указывает максимальную емкость.</span><span class="sxs-lookup"><span data-stu-id="78c84-130">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="78c84-131">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="78c84-131">-MinimumCapacity</span></span>
<span data-ttu-id="78c84-132">Указывает минимальную емкость.</span><span class="sxs-lookup"><span data-stu-id="78c84-132">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="78c84-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78c84-133">-Name</span></span>
<span data-ttu-id="78c84-134">Указывает имя создаваемого профиля.</span><span class="sxs-lookup"><span data-stu-id="78c84-134">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="78c84-135">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="78c84-135">-RecurrenceFrequency</span></span>
<span data-ttu-id="78c84-136">Указывает периодичность повторения.</span><span class="sxs-lookup"><span data-stu-id="78c84-136">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="78c84-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="78c84-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78c84-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="78c84-138">None</span></span>
- <span data-ttu-id="78c84-139">2</span><span class="sxs-lookup"><span data-stu-id="78c84-139">Second</span></span>
- <span data-ttu-id="78c84-140">До</span><span class="sxs-lookup"><span data-stu-id="78c84-140">Minute</span></span>
- <span data-ttu-id="78c84-141">Часовой</span><span class="sxs-lookup"><span data-stu-id="78c84-141">Hour</span></span>
- <span data-ttu-id="78c84-142">Дневных</span><span class="sxs-lookup"><span data-stu-id="78c84-142">Day</span></span>
- <span data-ttu-id="78c84-143">Недели</span><span class="sxs-lookup"><span data-stu-id="78c84-143">Week</span></span>
- <span data-ttu-id="78c84-144">Перехода</span><span class="sxs-lookup"><span data-stu-id="78c84-144">Month</span></span>
- <span data-ttu-id="78c84-145">Year</span><span class="sxs-lookup"><span data-stu-id="78c84-145">Year</span></span>

<span data-ttu-id="78c84-146">Поддерживаются не все из этих значений.</span><span class="sxs-lookup"><span data-stu-id="78c84-146">Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c84-147">-Правила</span><span class="sxs-lookup"><span data-stu-id="78c84-147">-Rules</span></span>
<span data-ttu-id="78c84-148">Указывает список правил, которые нужно добавить к профилю.</span><span class="sxs-lookup"><span data-stu-id="78c84-148">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="78c84-149">-ScheduleDays</span><span class="sxs-lookup"><span data-stu-id="78c84-149">-ScheduleDays</span></span>
<span data-ttu-id="78c84-150">Задает запланированные дни.</span><span class="sxs-lookup"><span data-stu-id="78c84-150">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c84-151">-ScheduleHours</span><span class="sxs-lookup"><span data-stu-id="78c84-151">-ScheduleHours</span></span>
<span data-ttu-id="78c84-152">Задает запланированные часы.</span><span class="sxs-lookup"><span data-stu-id="78c84-152">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c84-153">-ScheduleMinutes</span><span class="sxs-lookup"><span data-stu-id="78c84-153">-ScheduleMinutes</span></span>
<span data-ttu-id="78c84-154">Задает запланированные минуты.</span><span class="sxs-lookup"><span data-stu-id="78c84-154">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c84-155">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="78c84-155">-ScheduleTimeZone</span></span>
<span data-ttu-id="78c84-156">Указывает часовой пояс расписания.</span><span class="sxs-lookup"><span data-stu-id="78c84-156">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c84-157">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="78c84-157">-StartTimeWindow</span></span>
<span data-ttu-id="78c84-158">Задает начало временного интервала.</span><span class="sxs-lookup"><span data-stu-id="78c84-158">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c84-159">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="78c84-159">-TimeWindowTimeZone</span></span>
<span data-ttu-id="78c84-160">Указывает часовой пояс для временного интервала.</span><span class="sxs-lookup"><span data-stu-id="78c84-160">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c84-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c84-161">-DefaultProfile</span></span>
<span data-ttu-id="78c84-162">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78c84-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78c84-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c84-163">CommonParameters</span></span>
<span data-ttu-id="78c84-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78c84-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c84-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c84-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c84-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78c84-166">INPUTS</span></span>

## <span data-ttu-id="78c84-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78c84-167">OUTPUTS</span></span>

### <span data-ttu-id="78c84-168">Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="78c84-168">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="78c84-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="78c84-169">NOTES</span></span>

## <span data-ttu-id="78c84-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78c84-170">RELATED LINKS</span></span>

[<span data-ttu-id="78c84-171">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="78c84-171">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="78c84-172">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="78c84-172">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="78c84-173">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="78c84-173">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="78c84-174">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="78c84-174">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="78c84-175">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="78c84-175">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


