---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: d82e63d21e18b7fb75282da9ac12be7644b0535a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732885"
---
# <span data-ttu-id="95fd9-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="95fd9-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="95fd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="95fd9-103">Создание расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="95fd9-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95fd9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95fd9-104">SYNTAX</span></span>

### <span data-ttu-id="95fd9-105">ByDaily (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95fd9-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fd9-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="95fd9-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95fd9-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="95fd9-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95fd9-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="95fd9-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fd9-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="95fd9-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fd9-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="95fd9-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95fd9-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95fd9-111">DESCRIPTION</span></span>
<span data-ttu-id="95fd9-112">Командлет **New-AzureRmAutomationSchedule** создает расписание в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="95fd9-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="95fd9-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95fd9-113">EXAMPLES</span></span>

### <span data-ttu-id="95fd9-114">Пример 1: создание одноразового расписания в местном времени</span><span class="sxs-lookup"><span data-stu-id="95fd9-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="95fd9-115">Первая команда получает идентификатор часового пояса из системы и сохраняет ее в переменной $TimeZone.</span><span class="sxs-lookup"><span data-stu-id="95fd9-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="95fd9-116">Вторая команда создает расписание, которое выполняется один раз на текущую дату в 11:00 PM в указанном часовом поясе...</span><span class="sxs-lookup"><span data-stu-id="95fd9-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="95fd9-117">Пример 2: создание повторяющегося расписания</span><span class="sxs-lookup"><span data-stu-id="95fd9-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="95fd9-118">Первая команда создает объект Date с помощью командлета **Get-Date** , а затем сохраняет объект в переменной $StartDate.</span><span class="sxs-lookup"><span data-stu-id="95fd9-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="95fd9-119">Укажите время, которое не менее пяти минут в будущем.</span><span class="sxs-lookup"><span data-stu-id="95fd9-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="95fd9-120">Вторая команда создает объект Date с помощью командлета **Get-Date** , а затем сохраняет объект в переменной $EndDate.</span><span class="sxs-lookup"><span data-stu-id="95fd9-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="95fd9-121">Команда задает время в будущем.</span><span class="sxs-lookup"><span data-stu-id="95fd9-121">The command specifies a future time.</span></span>

<span data-ttu-id="95fd9-122">Последняя команда создает ежедневное расписание с именем Schedule01, чтобы оно начиналось с момента, которое хранится в $StartDate и истекает на время, которое хранится в $EndDate.</span><span class="sxs-lookup"><span data-stu-id="95fd9-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="95fd9-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95fd9-123">PARAMETERS</span></span>

### <span data-ttu-id="95fd9-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="95fd9-124">-AutomationAccountName</span></span>
<span data-ttu-id="95fd9-125">Указывает имя учетной записи автоматизации, для которой этот командлет создает расписание.</span><span class="sxs-lookup"><span data-stu-id="95fd9-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="95fd9-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="95fd9-126">-DayInterval</span></span>
<span data-ttu-id="95fd9-127">Указывает интервал (в днях) для расписания.</span><span class="sxs-lookup"><span data-stu-id="95fd9-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="95fd9-128">Если этот параметр не указан и не указан параметр *OneTime* , по умолчанию используется значение One (1).</span><span class="sxs-lookup"><span data-stu-id="95fd9-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="95fd9-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="95fd9-129">-DayOfWeek</span></span>
<span data-ttu-id="95fd9-130">Указывает список дней недели для недельного расписания.</span><span class="sxs-lookup"><span data-stu-id="95fd9-130">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="95fd9-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="95fd9-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="95fd9-132">Указывает повторение недели в месяце, в котором выполняется расписание.</span><span class="sxs-lookup"><span data-stu-id="95fd9-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="95fd9-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="95fd9-133">psdx_paramvalues</span></span>

- <span data-ttu-id="95fd9-134">1,1</span><span class="sxs-lookup"><span data-stu-id="95fd9-134">1</span></span>
- <span data-ttu-id="95fd9-135">2</span><span class="sxs-lookup"><span data-stu-id="95fd9-135">2</span></span>
- <span data-ttu-id="95fd9-136">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="95fd9-136">3</span></span>
- <span data-ttu-id="95fd9-137">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="95fd9-137">4</span></span>
- <span data-ttu-id="95fd9-138">-1</span><span class="sxs-lookup"><span data-stu-id="95fd9-138">-1</span></span>
- <span data-ttu-id="95fd9-139">Первич</span><span class="sxs-lookup"><span data-stu-id="95fd9-139">First</span></span>
- <span data-ttu-id="95fd9-140">2</span><span class="sxs-lookup"><span data-stu-id="95fd9-140">Second</span></span>
- <span data-ttu-id="95fd9-141">Третьего</span><span class="sxs-lookup"><span data-stu-id="95fd9-141">Third</span></span>
- <span data-ttu-id="95fd9-142">Заканчива</span><span class="sxs-lookup"><span data-stu-id="95fd9-142">Fourth</span></span>
- <span data-ttu-id="95fd9-143">LastDay</span><span class="sxs-lookup"><span data-stu-id="95fd9-143">LastDay</span></span>

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

### <span data-ttu-id="95fd9-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="95fd9-144">-DaysOfMonth</span></span>
<span data-ttu-id="95fd9-145">Задает список дней месяца для расписания Monthly.</span><span class="sxs-lookup"><span data-stu-id="95fd9-145">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="95fd9-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="95fd9-146">-DaysOfWeek</span></span>
<span data-ttu-id="95fd9-147">Указывает список дней недели для недельного расписания.</span><span class="sxs-lookup"><span data-stu-id="95fd9-147">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="95fd9-148">-Описание</span><span class="sxs-lookup"><span data-stu-id="95fd9-148">-Description</span></span>
<span data-ttu-id="95fd9-149">Задает описание расписания.</span><span class="sxs-lookup"><span data-stu-id="95fd9-149">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="95fd9-150">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="95fd9-150">-ExpiryTime</span></span>
<span data-ttu-id="95fd9-151">Задает время истечения срока действия расписания как объект **DateTimeOffest** .</span><span class="sxs-lookup"><span data-stu-id="95fd9-151">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="95fd9-152">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="95fd9-152">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="95fd9-153">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="95fd9-153">-HourInterval</span></span>
<span data-ttu-id="95fd9-154">Задает интервал в часах для расписания.</span><span class="sxs-lookup"><span data-stu-id="95fd9-154">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="95fd9-155">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="95fd9-155">-MonthInterval</span></span>
<span data-ttu-id="95fd9-156">Указывает интервал в месяцах для расписания.</span><span class="sxs-lookup"><span data-stu-id="95fd9-156">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="95fd9-157">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95fd9-157">-Name</span></span>
<span data-ttu-id="95fd9-158">Задает имя расписания.</span><span class="sxs-lookup"><span data-stu-id="95fd9-158">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="95fd9-159">-OneTime</span><span class="sxs-lookup"><span data-stu-id="95fd9-159">-OneTime</span></span>
<span data-ttu-id="95fd9-160">Указывает на то, что командлет создает единовременно разовое расписание.</span><span class="sxs-lookup"><span data-stu-id="95fd9-160">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="95fd9-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95fd9-161">-ResourceGroupName</span></span>
<span data-ttu-id="95fd9-162">Указывает имя группы ресурсов, для которой этот командлет создает расписание.</span><span class="sxs-lookup"><span data-stu-id="95fd9-162">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="95fd9-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="95fd9-163">-StartTime</span></span>
<span data-ttu-id="95fd9-164">Задает время начала расписания как объект **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="95fd9-164">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="95fd9-165">Вы можете указать строку, которую можно преобразовать в допустимый тип **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="95fd9-165">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="95fd9-166">.</span><span class="sxs-lookup"><span data-stu-id="95fd9-166">.</span></span> <span data-ttu-id="95fd9-167">Если указан параметр *TimeZone* , смещение будет проигнорировано и используется указанный часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="95fd9-167">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="95fd9-168">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="95fd9-168">-TimeZone</span></span>
<span data-ttu-id="95fd9-169">Задает часовой пояс расписания.</span><span class="sxs-lookup"><span data-stu-id="95fd9-169">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="95fd9-170">Эта строка может быть ИДЕНТИФИКАТОРом IANA или ИДЕНТИФИКАТОРом часового пояса Windows.</span><span class="sxs-lookup"><span data-stu-id="95fd9-170">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="95fd9-171">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="95fd9-171">-WeekInterval</span></span>
<span data-ttu-id="95fd9-172">Указывает интервал (в неделях) для расписания.</span><span class="sxs-lookup"><span data-stu-id="95fd9-172">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="95fd9-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fd9-173">-DefaultProfile</span></span>
<span data-ttu-id="95fd9-174">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95fd9-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95fd9-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fd9-175">CommonParameters</span></span>
<span data-ttu-id="95fd9-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95fd9-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fd9-177">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95fd9-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fd9-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95fd9-178">INPUTS</span></span>

## <span data-ttu-id="95fd9-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95fd9-179">OUTPUTS</span></span>

### <span data-ttu-id="95fd9-180">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="95fd9-180">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="95fd9-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="95fd9-181">NOTES</span></span>

## <span data-ttu-id="95fd9-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95fd9-182">RELATED LINKS</span></span>

[<span data-ttu-id="95fd9-183">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="95fd9-183">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="95fd9-184">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="95fd9-184">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="95fd9-185">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="95fd9-185">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


