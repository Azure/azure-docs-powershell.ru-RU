---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074963"
---
# <span data-ttu-id="fc62e-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fc62e-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="fc62e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc62e-102">SYNOPSIS</span></span>
<span data-ttu-id="fc62e-103">Создание расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="fc62e-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="fc62e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc62e-104">SYNTAX</span></span>

### <span data-ttu-id="fc62e-105">ByDaily (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc62e-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc62e-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="fc62e-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc62e-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="fc62e-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc62e-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="fc62e-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc62e-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="fc62e-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc62e-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="fc62e-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc62e-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc62e-111">DESCRIPTION</span></span>
<span data-ttu-id="fc62e-112">Командлет **New-AzAutomationSchedule** создает расписание в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fc62e-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="fc62e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc62e-113">EXAMPLES</span></span>

### <span data-ttu-id="fc62e-114">Пример 1: создание одноразового расписания в местном времени</span><span class="sxs-lookup"><span data-stu-id="fc62e-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="fc62e-115">Первая команда получает идентификатор часового пояса из системы и сохраняет ее в переменной $TimeZone.</span><span class="sxs-lookup"><span data-stu-id="fc62e-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="fc62e-116">Вторая команда создает расписание, которое выполняется один раз на текущую дату в 11:00 PM в указанном часовом поясе...</span><span class="sxs-lookup"><span data-stu-id="fc62e-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="fc62e-117">Пример 2: создание повторяющегося расписания</span><span class="sxs-lookup"><span data-stu-id="fc62e-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fc62e-118">Первая команда создает объект Date с помощью командлета **Get-Date** , а затем сохраняет объект в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="fc62e-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="fc62e-119">Укажите время, которое не менее пяти минут в будущем.</span><span class="sxs-lookup"><span data-stu-id="fc62e-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="fc62e-120">Вторая команда создает объект Date с помощью командлета **Get-Date** , а затем сохраняет объект в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="fc62e-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="fc62e-121">Команда задает время в будущем.</span><span class="sxs-lookup"><span data-stu-id="fc62e-121">The command specifies a future time.</span></span>
<span data-ttu-id="fc62e-122">Последняя команда создает ежедневное расписание с именем Schedule02, чтобы оно начиналось с момента, которое хранится в $StartDate и истекает на время, которое хранится в $EndDate.</span><span class="sxs-lookup"><span data-stu-id="fc62e-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="fc62e-123">Пример 3: создание повторяющегося расписания, еженедельно</span><span class="sxs-lookup"><span data-stu-id="fc62e-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fc62e-124">Первая команда создает объект Date с помощью командлета **Get-Date** , а затем сохраняет объект в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="fc62e-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="fc62e-125">Вторая команда создает массив дней недели, включающий понедельник, вторник, среду, четверг и пятницу.</span><span class="sxs-lookup"><span data-stu-id="fc62e-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="fc62e-126">Последняя команда создает ежедневное расписание с именем Schedule03, которое будет запускать понедельник и пятницу в 13:00.</span><span class="sxs-lookup"><span data-stu-id="fc62e-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="fc62e-127">Срок действия расписания никогда не истекает.</span><span class="sxs-lookup"><span data-stu-id="fc62e-127">The schedule will never expire.</span></span>

## <span data-ttu-id="fc62e-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc62e-128">PARAMETERS</span></span>

### <span data-ttu-id="fc62e-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fc62e-129">-AutomationAccountName</span></span>
<span data-ttu-id="fc62e-130">Указывает имя учетной записи автоматизации, для которой этот командлет создает расписание.</span><span class="sxs-lookup"><span data-stu-id="fc62e-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="fc62e-131">-DayInterval</span></span>
<span data-ttu-id="fc62e-132">Указывает интервал (в днях) для расписания.</span><span class="sxs-lookup"><span data-stu-id="fc62e-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="fc62e-133">Если этот параметр не указан и не указан параметр *OneTime* , по умолчанию используется значение One (1).</span><span class="sxs-lookup"><span data-stu-id="fc62e-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="fc62e-134">-DayOfWeek</span></span>
<span data-ttu-id="fc62e-135">Указывает список дней недели для недельного расписания.</span><span class="sxs-lookup"><span data-stu-id="fc62e-135">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="fc62e-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="fc62e-137">Указывает повторение недели в месяце, в котором выполняется расписание.</span><span class="sxs-lookup"><span data-stu-id="fc62e-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="fc62e-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="fc62e-138">psdx_paramvalues</span></span>
- <span data-ttu-id="fc62e-139">1,1</span><span class="sxs-lookup"><span data-stu-id="fc62e-139">1</span></span>
- <span data-ttu-id="fc62e-140">2</span><span class="sxs-lookup"><span data-stu-id="fc62e-140">2</span></span>
- <span data-ttu-id="fc62e-141">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="fc62e-141">3</span></span>
- <span data-ttu-id="fc62e-142">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="fc62e-142">4</span></span>
- <span data-ttu-id="fc62e-143">-1</span><span class="sxs-lookup"><span data-stu-id="fc62e-143">-1</span></span>
- <span data-ttu-id="fc62e-144">Первич</span><span class="sxs-lookup"><span data-stu-id="fc62e-144">First</span></span>
- <span data-ttu-id="fc62e-145">2</span><span class="sxs-lookup"><span data-stu-id="fc62e-145">Second</span></span>
- <span data-ttu-id="fc62e-146">Третьего</span><span class="sxs-lookup"><span data-stu-id="fc62e-146">Third</span></span>
- <span data-ttu-id="fc62e-147">Заканчива</span><span class="sxs-lookup"><span data-stu-id="fc62e-147">Fourth</span></span>
- <span data-ttu-id="fc62e-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="fc62e-148">LastDay</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="fc62e-149">-DaysOfMonth</span></span>
<span data-ttu-id="fc62e-150">Задает список дней месяца для расписания Monthly.</span><span class="sxs-lookup"><span data-stu-id="fc62e-150">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases:
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="fc62e-151">-DaysOfWeek</span></span>
<span data-ttu-id="fc62e-152">Указывает список дней недели для недельного расписания.</span><span class="sxs-lookup"><span data-stu-id="fc62e-152">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc62e-153">-DefaultProfile</span></span>
<span data-ttu-id="fc62e-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fc62e-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc62e-155">-Описание</span><span class="sxs-lookup"><span data-stu-id="fc62e-155">-Description</span></span>
<span data-ttu-id="fc62e-156">Задает описание расписания.</span><span class="sxs-lookup"><span data-stu-id="fc62e-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="fc62e-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="fc62e-157">-ExpiryTime</span></span>
<span data-ttu-id="fc62e-158">Задает время истечения срока действия расписания в качестве объекта **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="fc62e-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="fc62e-159">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="fc62e-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc62e-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="fc62e-161">Указывает, что этот объект расписания будет использоваться для планирования конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="fc62e-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="fc62e-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="fc62e-162">-HourInterval</span></span>
<span data-ttu-id="fc62e-163">Задает интервал в часах для расписания.</span><span class="sxs-lookup"><span data-stu-id="fc62e-163">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="fc62e-164">-MonthInterval</span></span>
<span data-ttu-id="fc62e-165">Указывает интервал в месяцах для расписания.</span><span class="sxs-lookup"><span data-stu-id="fc62e-165">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-166">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc62e-166">-Name</span></span>
<span data-ttu-id="fc62e-167">Задает имя расписания.</span><span class="sxs-lookup"><span data-stu-id="fc62e-167">Specifies a name for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="fc62e-168">-OneTime</span></span>
<span data-ttu-id="fc62e-169">Указывает на то, что командлет создает единовременно разовое расписание.</span><span class="sxs-lookup"><span data-stu-id="fc62e-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc62e-170">-ResourceGroupName</span></span>
<span data-ttu-id="fc62e-171">Указывает имя группы ресурсов, для которой этот командлет создает расписание.</span><span class="sxs-lookup"><span data-stu-id="fc62e-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fc62e-172">-StartTime</span></span>
<span data-ttu-id="fc62e-173">Задает время начала расписания как объект **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="fc62e-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="fc62e-174">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="fc62e-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="fc62e-175">Если указан параметр *TimeZone* , смещение будет проигнорировано и используется указанный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="fc62e-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-176">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="fc62e-176">-TimeZone</span></span>
<span data-ttu-id="fc62e-177">Задает часовой пояс расписания.</span><span class="sxs-lookup"><span data-stu-id="fc62e-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="fc62e-178">Эта строка может быть ИДЕНТИФИКАТОРом IANA или ИДЕНТИФИКАТОРом часового пояса Windows.</span><span class="sxs-lookup"><span data-stu-id="fc62e-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="fc62e-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="fc62e-179">-WeekInterval</span></span>
<span data-ttu-id="fc62e-180">Указывает интервал (в неделях) для расписания.</span><span class="sxs-lookup"><span data-stu-id="fc62e-180">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc62e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc62e-181">CommonParameters</span></span>
<span data-ttu-id="fc62e-182">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc62e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc62e-183">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc62e-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc62e-184">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc62e-184">INPUTS</span></span>

### <span data-ttu-id="fc62e-185">System. String</span><span class="sxs-lookup"><span data-stu-id="fc62e-185">System.String</span></span>

### <span data-ttu-id="fc62e-186">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fc62e-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="fc62e-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc62e-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc62e-188">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc62e-188">OUTPUTS</span></span>

### <span data-ttu-id="fc62e-189">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="fc62e-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="fc62e-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc62e-190">NOTES</span></span>

## <span data-ttu-id="fc62e-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc62e-191">RELATED LINKS</span></span>

[<span data-ttu-id="fc62e-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fc62e-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="fc62e-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fc62e-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="fc62e-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fc62e-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


