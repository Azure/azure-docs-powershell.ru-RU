---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076219"
---
# <span data-ttu-id="19f0d-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19f0d-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="19f0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19f0d-102">SYNOPSIS</span></span>

<span data-ttu-id="19f0d-103">Создание расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="19f0d-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="19f0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19f0d-104">SYNTAX</span></span>

### <span data-ttu-id="19f0d-105">ByDaily (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19f0d-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="19f0d-106">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="19f0d-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19f0d-107">ByHourly</span><span class="sxs-lookup"><span data-stu-id="19f0d-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="19f0d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19f0d-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="19f0d-109">Командлет **New-AzureAutomationSchedule** создает расписание в службе автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="19f0d-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="19f0d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19f0d-110">EXAMPLES</span></span>

### <span data-ttu-id="19f0d-111">Пример 1: создание одноразового расписания</span><span class="sxs-lookup"><span data-stu-id="19f0d-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="19f0d-112">Следующая команда создает расписание, которое выполняется один раз в текущую дату на 11:00 PM.</span><span class="sxs-lookup"><span data-stu-id="19f0d-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="19f0d-113">Пример 2: создание повторяющегося расписания</span><span class="sxs-lookup"><span data-stu-id="19f0d-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="19f0d-114">Следующие команды создают новое расписание, которое запускается в 1:00 PM ежедневно для одного года, начиная с текущего дня.</span><span class="sxs-lookup"><span data-stu-id="19f0d-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="19f0d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19f0d-115">PARAMETERS</span></span>

### <span data-ttu-id="19f0d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="19f0d-116">-AutomationAccountName</span></span>
<span data-ttu-id="19f0d-117">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="19f0d-117">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="19f0d-118">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="19f0d-118">-DayInterval</span></span>
<span data-ttu-id="19f0d-119">Указывает интервал (в днях) для расписания.</span><span class="sxs-lookup"><span data-stu-id="19f0d-119">Specifies an interval, in days, for the schedule.</span></span>

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

### <span data-ttu-id="19f0d-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="19f0d-120">-Description</span></span>
<span data-ttu-id="19f0d-121">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="19f0d-121">Specifies a description.</span></span>

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

### <span data-ttu-id="19f0d-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="19f0d-122">-ExpiryTime</span></span>
<span data-ttu-id="19f0d-123">Указывает время истечения срока действия расписания.</span><span class="sxs-lookup"><span data-stu-id="19f0d-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="19f0d-124">Строка может быть указана, если ее можно преобразовать в допустимый **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="19f0d-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f0d-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="19f0d-125">-HourInterval</span></span>
<span data-ttu-id="19f0d-126">Задает интервал в часах для расписания.</span><span class="sxs-lookup"><span data-stu-id="19f0d-126">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="19f0d-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19f0d-127">-Name</span></span>
<span data-ttu-id="19f0d-128">Задает имя расписания.</span><span class="sxs-lookup"><span data-stu-id="19f0d-128">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="19f0d-129">-OneTime</span><span class="sxs-lookup"><span data-stu-id="19f0d-129">-OneTime</span></span>
<span data-ttu-id="19f0d-130">Указывает на то, что эта операция создает единовременно разовое расписание.</span><span class="sxs-lookup"><span data-stu-id="19f0d-130">Indicates that this operation creates a one-time schedule.</span></span>

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

### <span data-ttu-id="19f0d-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="19f0d-131">-Profile</span></span>
<span data-ttu-id="19f0d-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="19f0d-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19f0d-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19f0d-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19f0d-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="19f0d-134">-StartTime</span></span>
<span data-ttu-id="19f0d-135">Указывает время начала расписания.</span><span class="sxs-lookup"><span data-stu-id="19f0d-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="19f0d-136">Строка может быть указана, если ее можно преобразовать в допустимый **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="19f0d-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19f0d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19f0d-137">CommonParameters</span></span>
<span data-ttu-id="19f0d-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19f0d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19f0d-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19f0d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19f0d-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19f0d-140">INPUTS</span></span>

## <span data-ttu-id="19f0d-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19f0d-141">OUTPUTS</span></span>

### <span data-ttu-id="19f0d-142">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="19f0d-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="19f0d-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="19f0d-143">NOTES</span></span>

## <span data-ttu-id="19f0d-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19f0d-144">RELATED LINKS</span></span>

[<span data-ttu-id="19f0d-145">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19f0d-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="19f0d-146">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19f0d-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="19f0d-147">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="19f0d-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


