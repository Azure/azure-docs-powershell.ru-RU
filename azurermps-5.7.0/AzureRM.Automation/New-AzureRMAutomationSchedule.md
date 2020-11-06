---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: 3528a95e9dab3c92571ec49e9bf5d567012fb5b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568259"
---
# <span data-ttu-id="2fb31-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2fb31-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="2fb31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fb31-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb31-103">Создание расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="2fb31-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fb31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fb31-104">SYNTAX</span></span>

### <span data-ttu-id="2fb31-105">ByDaily (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2fb31-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fb31-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="2fb31-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fb31-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="2fb31-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fb31-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="2fb31-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fb31-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="2fb31-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fb31-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="2fb31-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fb31-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fb31-111">DESCRIPTION</span></span>
<span data-ttu-id="2fb31-112">Командлет **New-AzureRmAutomationSchedule** создает расписание в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2fb31-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="2fb31-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fb31-113">EXAMPLES</span></span>

### <span data-ttu-id="2fb31-114">Пример 1: создание одноразового расписания в местном времени</span><span class="sxs-lookup"><span data-stu-id="2fb31-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="2fb31-115">Первая команда получает идентификатор часового пояса из системы и сохраняет ее в переменной $TimeZone.</span><span class="sxs-lookup"><span data-stu-id="2fb31-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="2fb31-116">Вторая команда создает расписание, которое выполняется один раз на текущую дату в 11:00 PM в указанном часовом поясе...</span><span class="sxs-lookup"><span data-stu-id="2fb31-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="2fb31-117">Пример 2: создание повторяющегося расписания</span><span class="sxs-lookup"><span data-stu-id="2fb31-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2fb31-118">Первая команда создает объект Date с помощью командлета **Get-Date** , а затем сохраняет объект в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="2fb31-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="2fb31-119">Укажите время, которое не менее пяти минут в будущем.</span><span class="sxs-lookup"><span data-stu-id="2fb31-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="2fb31-120">Вторая команда создает объект Date с помощью командлета **Get-Date** , а затем сохраняет объект в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="2fb31-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="2fb31-121">Команда задает время в будущем.</span><span class="sxs-lookup"><span data-stu-id="2fb31-121">The command specifies a future time.</span></span>

<span data-ttu-id="2fb31-122">Последняя команда создает ежедневное расписание с именем Schedule01, чтобы оно начиналось с момента, которое хранится в $StartDate и истекает на время, которое хранится в $EndDate.</span><span class="sxs-lookup"><span data-stu-id="2fb31-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="2fb31-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fb31-123">PARAMETERS</span></span>

### <span data-ttu-id="2fb31-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2fb31-124">-AutomationAccountName</span></span>
<span data-ttu-id="2fb31-125">Указывает имя учетной записи автоматизации, для которой этот командлет создает расписание.</span><span class="sxs-lookup"><span data-stu-id="2fb31-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="2fb31-126">-DayInterval</span></span>
<span data-ttu-id="2fb31-127">Указывает интервал (в днях) для расписания.</span><span class="sxs-lookup"><span data-stu-id="2fb31-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="2fb31-128">Если этот параметр не указан и не указан параметр *OneTime* , по умолчанию используется значение One (1).</span><span class="sxs-lookup"><span data-stu-id="2fb31-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="2fb31-129">-DayOfWeek</span></span>
<span data-ttu-id="2fb31-130">Указывает список дней недели для недельного расписания.</span><span class="sxs-lookup"><span data-stu-id="2fb31-130">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="2fb31-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="2fb31-132">Указывает повторение недели в месяце, в котором выполняется расписание.</span><span class="sxs-lookup"><span data-stu-id="2fb31-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="2fb31-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="2fb31-133">psdx_paramvalues</span></span>

- <span data-ttu-id="2fb31-134">1,1</span><span class="sxs-lookup"><span data-stu-id="2fb31-134">1</span></span>
- <span data-ttu-id="2fb31-135">2</span><span class="sxs-lookup"><span data-stu-id="2fb31-135">2</span></span>
- <span data-ttu-id="2fb31-136">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="2fb31-136">3</span></span>
- <span data-ttu-id="2fb31-137">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="2fb31-137">4</span></span>
- <span data-ttu-id="2fb31-138">-1</span><span class="sxs-lookup"><span data-stu-id="2fb31-138">-1</span></span>
- <span data-ttu-id="2fb31-139">Первич</span><span class="sxs-lookup"><span data-stu-id="2fb31-139">First</span></span>
- <span data-ttu-id="2fb31-140">2</span><span class="sxs-lookup"><span data-stu-id="2fb31-140">Second</span></span>
- <span data-ttu-id="2fb31-141">Третьего</span><span class="sxs-lookup"><span data-stu-id="2fb31-141">Third</span></span>
- <span data-ttu-id="2fb31-142">Заканчива</span><span class="sxs-lookup"><span data-stu-id="2fb31-142">Fourth</span></span>
- <span data-ttu-id="2fb31-143">LastDay</span><span class="sxs-lookup"><span data-stu-id="2fb31-143">LastDay</span></span>

```yaml
Type: DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="2fb31-144">-DaysOfMonth</span></span>
<span data-ttu-id="2fb31-145">Задает список дней месяца для расписания Monthly.</span><span class="sxs-lookup"><span data-stu-id="2fb31-145">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases: 
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="2fb31-146">-DaysOfWeek</span></span>
<span data-ttu-id="2fb31-147">Указывает список дней недели для недельного расписания.</span><span class="sxs-lookup"><span data-stu-id="2fb31-147">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: ByWeekly
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb31-148">-DefaultProfile</span></span>
<span data-ttu-id="2fb31-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2fb31-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fb31-150">-Описание</span><span class="sxs-lookup"><span data-stu-id="2fb31-150">-Description</span></span>
<span data-ttu-id="2fb31-151">Задает описание расписания.</span><span class="sxs-lookup"><span data-stu-id="2fb31-151">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-152">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2fb31-152">-ExpiryTime</span></span>
<span data-ttu-id="2fb31-153">Задает время истечения срока действия расписания как объект **DateTimeOffest** .</span><span class="sxs-lookup"><span data-stu-id="2fb31-153">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="2fb31-154">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="2fb31-154">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-155">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="2fb31-155">-HourInterval</span></span>
<span data-ttu-id="2fb31-156">Задает интервал в часах для расписания.</span><span class="sxs-lookup"><span data-stu-id="2fb31-156">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-157">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="2fb31-157">-MonthInterval</span></span>
<span data-ttu-id="2fb31-158">Указывает интервал в месяцах для расписания.</span><span class="sxs-lookup"><span data-stu-id="2fb31-158">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-159">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fb31-159">-Name</span></span>
<span data-ttu-id="2fb31-160">Задает имя расписания.</span><span class="sxs-lookup"><span data-stu-id="2fb31-160">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-161">-OneTime</span><span class="sxs-lookup"><span data-stu-id="2fb31-161">-OneTime</span></span>
<span data-ttu-id="2fb31-162">Указывает на то, что командлет создает единовременно разовое расписание.</span><span class="sxs-lookup"><span data-stu-id="2fb31-162">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fb31-163">-ResourceGroupName</span></span>
<span data-ttu-id="2fb31-164">Указывает имя группы ресурсов, для которой этот командлет создает расписание.</span><span class="sxs-lookup"><span data-stu-id="2fb31-164">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2fb31-165">-StartTime</span></span>
<span data-ttu-id="2fb31-166">Задает время начала расписания как объект **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="2fb31-166">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="2fb31-167">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="2fb31-167">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="2fb31-168">.</span><span class="sxs-lookup"><span data-stu-id="2fb31-168">.</span></span> <span data-ttu-id="2fb31-169">Если указан параметр *TimeZone* , смещение будет проигнорировано и используется указанный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="2fb31-169">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-170">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="2fb31-170">-TimeZone</span></span>
<span data-ttu-id="2fb31-171">Задает часовой пояс расписания.</span><span class="sxs-lookup"><span data-stu-id="2fb31-171">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="2fb31-172">Эта строка может быть ИДЕНТИФИКАТОРом IANA или ИДЕНТИФИКАТОРом часового пояса Windows.</span><span class="sxs-lookup"><span data-stu-id="2fb31-172">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-173">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="2fb31-173">-WeekInterval</span></span>
<span data-ttu-id="2fb31-174">Указывает интервал (в неделях) для расписания.</span><span class="sxs-lookup"><span data-stu-id="2fb31-174">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByWeekly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fb31-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb31-175">CommonParameters</span></span>
<span data-ttu-id="2fb31-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fb31-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb31-177">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fb31-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb31-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fb31-178">INPUTS</span></span>

### <span data-ttu-id="2fb31-179">Ничего</span><span class="sxs-lookup"><span data-stu-id="2fb31-179">None</span></span>
<span data-ttu-id="2fb31-180">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2fb31-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2fb31-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fb31-181">OUTPUTS</span></span>

### <span data-ttu-id="2fb31-182">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="2fb31-182">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="2fb31-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fb31-183">NOTES</span></span>

## <span data-ttu-id="2fb31-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fb31-184">RELATED LINKS</span></span>

[<span data-ttu-id="2fb31-185">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2fb31-185">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="2fb31-186">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2fb31-186">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="2fb31-187">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2fb31-187">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


