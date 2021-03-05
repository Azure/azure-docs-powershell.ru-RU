---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 1c3837bffcf5b3cde03623e06ad1233ed833a4c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004835"
---
# <span data-ttu-id="dd41e-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dd41e-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="dd41e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd41e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd41e-103">Создает расписание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="dd41e-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="dd41e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd41e-104">SYNTAX</span></span>

### <span data-ttu-id="dd41e-105">ByDaily (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd41e-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd41e-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="dd41e-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd41e-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="dd41e-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd41e-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="dd41e-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd41e-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="dd41e-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd41e-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="dd41e-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd41e-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd41e-111">DESCRIPTION</span></span>
<span data-ttu-id="dd41e-112">Для создания календарного плана в автоматизации Azure создается календарный план **New-AzAutomationSchedule.**</span><span class="sxs-lookup"><span data-stu-id="dd41e-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="dd41e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd41e-113">EXAMPLES</span></span>

### <span data-ttu-id="dd41e-114">Пример 1. Создание одно расписания в локальное время</span><span class="sxs-lookup"><span data-stu-id="dd41e-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="dd41e-115">Первая команда получает из системы и сохраняет его в переменной $TimeZone часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="dd41e-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="dd41e-116">Вторая команда создает расписание, которое выполняется один раз к текущей дате в 23:00 в указанном часовом поясе.</span><span class="sxs-lookup"><span data-stu-id="dd41e-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="dd41e-117">Пример 2. Создание повторяющегося расписания</span><span class="sxs-lookup"><span data-stu-id="dd41e-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dd41e-118">Первая команда создает объект даты с помощью командлета **Get-Date,** а затем сохраняет его в $StartDate переменной.</span><span class="sxs-lookup"><span data-stu-id="dd41e-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="dd41e-119">Укажите время, которое будет по крайней мере пять минут в будущем.</span><span class="sxs-lookup"><span data-stu-id="dd41e-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="dd41e-120">Вторая команда создает объект даты с помощью командлета **Get-Date,** а затем сохраняет его в $EndDate переменной.</span><span class="sxs-lookup"><span data-stu-id="dd41e-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="dd41e-121">Команда определяет будущее время.</span><span class="sxs-lookup"><span data-stu-id="dd41e-121">The command specifies a future time.</span></span>
<span data-ttu-id="dd41e-122">Конечная команда создает ежедневный календарный план с именем Schedule02, который начинается с того времени, $StartDate и истекает в то время, $EndDate.</span><span class="sxs-lookup"><span data-stu-id="dd41e-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="dd41e-123">Пример 3. Создание еженедельного повторяющегося расписания</span><span class="sxs-lookup"><span data-stu-id="dd41e-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dd41e-124">Первая команда создает объект даты с помощью командлета **Get-Date,** а затем сохраняет его в $StartDate переменной.</span><span class="sxs-lookup"><span data-stu-id="dd41e-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="dd41e-125">Вторая команда создает массив дней недели, содержащий понедельник, вторник, среду, четверг и пятницу.</span><span class="sxs-lookup"><span data-stu-id="dd41e-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="dd41e-126">Конечная команда создает ежедневное расписание "Расписание03", которое будет еженедельно с понедельника по пятницу в 13:00.</span><span class="sxs-lookup"><span data-stu-id="dd41e-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="dd41e-127">Срок действия расписания не истечет.</span><span class="sxs-lookup"><span data-stu-id="dd41e-127">The schedule will never expire.</span></span>

## <span data-ttu-id="dd41e-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd41e-128">PARAMETERS</span></span>

### <span data-ttu-id="dd41e-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd41e-129">-AutomationAccountName</span></span>
<span data-ttu-id="dd41e-130">Указывает имя учетной записи автоматизации, для которой этот cmdlet создает расписание.</span><span class="sxs-lookup"><span data-stu-id="dd41e-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="dd41e-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="dd41e-131">-DayInterval</span></span>
<span data-ttu-id="dd41e-132">Интервал в днях для календарного плана.</span><span class="sxs-lookup"><span data-stu-id="dd41e-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="dd41e-133">Если этот параметр не указан и параметр *OneTime* не задан, по умолчанию будет задано значение 1 (1).</span><span class="sxs-lookup"><span data-stu-id="dd41e-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="dd41e-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="dd41e-134">-DayOfWeek</span></span>
<span data-ttu-id="dd41e-135">Определяет список дней недели для еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="dd41e-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="dd41e-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="dd41e-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="dd41e-137">Определяет, в течение недели ли будет установлено расписание.</span><span class="sxs-lookup"><span data-stu-id="dd41e-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="dd41e-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="dd41e-138">psdx_paramvalues</span></span>
- <span data-ttu-id="dd41e-139">1</span><span class="sxs-lookup"><span data-stu-id="dd41e-139">1</span></span>
- <span data-ttu-id="dd41e-140">2</span><span class="sxs-lookup"><span data-stu-id="dd41e-140">2</span></span>
- <span data-ttu-id="dd41e-141">3</span><span class="sxs-lookup"><span data-stu-id="dd41e-141">3</span></span>
- <span data-ttu-id="dd41e-142">4</span><span class="sxs-lookup"><span data-stu-id="dd41e-142">4</span></span>
- <span data-ttu-id="dd41e-143">-1</span><span class="sxs-lookup"><span data-stu-id="dd41e-143">-1</span></span>
- <span data-ttu-id="dd41e-144">First</span><span class="sxs-lookup"><span data-stu-id="dd41e-144">First</span></span>
- <span data-ttu-id="dd41e-145">Second</span><span class="sxs-lookup"><span data-stu-id="dd41e-145">Second</span></span>
- <span data-ttu-id="dd41e-146">Третий</span><span class="sxs-lookup"><span data-stu-id="dd41e-146">Third</span></span>
- <span data-ttu-id="dd41e-147">Fourth</span><span class="sxs-lookup"><span data-stu-id="dd41e-147">Fourth</span></span>
- <span data-ttu-id="dd41e-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="dd41e-148">LastDay</span></span>

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

### <span data-ttu-id="dd41e-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="dd41e-149">-DaysOfMonth</span></span>
<span data-ttu-id="dd41e-150">Определяет список дней месяца для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="dd41e-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="dd41e-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="dd41e-151">-DaysOfWeek</span></span>
<span data-ttu-id="dd41e-152">Определяет список дней недели для еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="dd41e-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="dd41e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd41e-153">-DefaultProfile</span></span>
<span data-ttu-id="dd41e-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd41e-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd41e-155">-Description</span><span class="sxs-lookup"><span data-stu-id="dd41e-155">-Description</span></span>
<span data-ttu-id="dd41e-156">Описание расписания.</span><span class="sxs-lookup"><span data-stu-id="dd41e-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="dd41e-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="dd41e-157">-ExpiryTime</span></span>
<span data-ttu-id="dd41e-158">Время окончания срока действия календарного плана в качестве объекта **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="dd41e-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="dd41e-159">Вы можете указать строку, которую можно преобразовать в допустимый **набор DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="dd41e-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="dd41e-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd41e-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="dd41e-161">Указывает на то, что объект расписания будет использоваться для планирования конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="dd41e-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="dd41e-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="dd41e-162">-HourInterval</span></span>
<span data-ttu-id="dd41e-163">Интервал в часах для календарного плана.</span><span class="sxs-lookup"><span data-stu-id="dd41e-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="dd41e-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="dd41e-164">-MonthInterval</span></span>
<span data-ttu-id="dd41e-165">Интервал в месяцах для календарного плана.</span><span class="sxs-lookup"><span data-stu-id="dd41e-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="dd41e-166">-Name</span><span class="sxs-lookup"><span data-stu-id="dd41e-166">-Name</span></span>
<span data-ttu-id="dd41e-167">Название расписания.</span><span class="sxs-lookup"><span data-stu-id="dd41e-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="dd41e-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="dd41e-168">-OneTime</span></span>
<span data-ttu-id="dd41e-169">Указывает на то, что с его 24-го на 1-е время создается разовая расписания.</span><span class="sxs-lookup"><span data-stu-id="dd41e-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="dd41e-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd41e-170">-ResourceGroupName</span></span>
<span data-ttu-id="dd41e-171">Указывает имя группы ресурсов, для которой этот cmdlet создает расписание.</span><span class="sxs-lookup"><span data-stu-id="dd41e-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="dd41e-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dd41e-172">-StartTime</span></span>
<span data-ttu-id="dd41e-173">Время начала расписания в качестве объекта **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="dd41e-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="dd41e-174">Вы можете указать строку, которую можно преобразовать в допустимый **набор DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="dd41e-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="dd41e-175">Если *задан* параметр часового пояса, смещение будет игнорироваться, а используемый часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="dd41e-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="dd41e-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="dd41e-176">-TimeZone</span></span>
<span data-ttu-id="dd41e-177">Определяет часовой пояс для расписания.</span><span class="sxs-lookup"><span data-stu-id="dd41e-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="dd41e-178">Эта строка может быть ИД IANA или часовой пояс Windows.</span><span class="sxs-lookup"><span data-stu-id="dd41e-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="dd41e-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="dd41e-179">-WeekInterval</span></span>
<span data-ttu-id="dd41e-180">Интервал в неделях для календарного плана.</span><span class="sxs-lookup"><span data-stu-id="dd41e-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="dd41e-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd41e-181">CommonParameters</span></span>
<span data-ttu-id="dd41e-182">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd41e-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd41e-183">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd41e-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd41e-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd41e-184">INPUTS</span></span>

### <span data-ttu-id="dd41e-185">System.String</span><span class="sxs-lookup"><span data-stu-id="dd41e-185">System.String</span></span>

### <span data-ttu-id="dd41e-186">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dd41e-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="dd41e-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dd41e-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dd41e-188">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd41e-188">OUTPUTS</span></span>

### <span data-ttu-id="dd41e-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="dd41e-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="dd41e-190">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd41e-190">NOTES</span></span>

## <span data-ttu-id="dd41e-191">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd41e-191">RELATED LINKS</span></span>

[<span data-ttu-id="dd41e-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dd41e-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="dd41e-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dd41e-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="dd41e-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="dd41e-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


